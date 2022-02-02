---
title: "How to set up a simple Wireguard VPN"
date: "2020-02-15"
categories: 
  - "geekices"
tags: 
  - "arch"
  - "debian"
  - "howto"
  - "tips"
  - "vpn"
  - "wireguard"
---

![](images/network-1572617_1920.jpg)

## Install [Wireguard](https://www.wireguard.com/quickstart/)

I'm using a Debian virtual machine for the server. In Debian 10, you'll need to install the following two packages:

apt install wireguard-dkms wireguard-tools

## Set up keys

First, navigate to `/etc/wireguard` (If not created, run `mkdir /etc/wireguard` as root) and then run the following commands as root:

wg genkey | tee laptop-private.key |  wg pubkey > laptop-public.key
wg genkey | tee server-private.key |  wg pubkey > server-public.key

The first line is for the public and private keys of the client, named laptop because, well, it'll be used on a laptop. But you can choose any other name.

## Configure the Wireguard server

First, enable IP forwarding. Since we're only using IPv4, edit the `/etc/sysctl.conf` file as root, locate the `net.ipv4.ip_forward` line, uncomment it and change the value to 1.

Now, you need to create the `/etc/wireguard/wg0.conf`. This will be both the name of the connection interface and the configuration file for that interface. I'm using just one for a simple setup.

\[Interface\]
Address = 10.200.200.1/24
ListenPort = 51820
PrivateKey = <copy private key from server-private.key>
PostUp   = iptables -A FORWARD -i %i -j ACCEPT; iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE
PostDown = iptables -D FORWARD -i %i -j ACCEPT; iptables -t nat -D POSTROUTING -o eth0 -j MASQUERADE

\[Peer\]
# laptop
PublicKey = <copy public key from laptop-public.key>
AllowedIPs = 10.200.200.2/32

Now you are ready to start the Wireguard daemon, so it can accept connections. Just run:

wg-quick up wg0

### Some things to know

#### \[Interface\]

**Address:** the private IPv4 addresses (you can also use IPv6 addresses) for the Wireguard server subnet. In this example, clients connection to the server will be assigned IPs ranging from 10.200.200.1 to 10.200.200.254.

**ListenPort**: the port where Wireguard will listen. Don't forget to open it in your firewall.

**PrivateKey**: the content from server-private.key.

**PostUp and PostDown**: defines steps to be run after the interface is turned on or off, respectively. In this case, iptables is used to set IP masquerade rules to allow all the clients to share the server’s IPv4 address. The rules will then be cleared once the tunnel is down. Don't forget to change `eth0` to your server's network device.

#### \[Peer\]

**PublicKey**: the content from laptop-public.key.

**AllowedIPs**: the subnet IP assigned to that client when it connects to the server

## Set up the client

On the client side, you'll also have to install Wireguard. If you're using Debian, Ubuntu or any distribution based on the previous two, the command will be the same (I'm assuming Ubuntu uses the same package names. If not, change it to your needs). In Arch, the distribution I'm currently using, you can install packages with:

pacman -Syuv wireguard-dkms wireguard-tools

### Configure the Wireguard client

Create the `/etc/wireguard/wg0.conf` file and populate it with the following content:

\[Interface\]
Address = 10.200.200.2/24
PrivateKey = <copy private key from laptop-private.key>

\[Peer\]
PublicKey = <copy public key from server-public.key>
AllowedIPs = 0.0.0.0/0
Endpoint = xxx.xxx.xxx.xxx:51820 
PersistentKeepalive = 25

### Some things to know

#### \[Interface\]

**Addresss**: the client's IP address in Wiregard's subnet.

**PrivateKey**: the content from laptop-private.key.

#### \[Peer\]

**PublicKey**: the content from server-public.key.

**AllowedIPs**: set it to 0.0.0.0/0 to forward all IPv4 traffic through Wireguard.

**Endpoint**: the server IP address, followed by the port to connect to.

**PersistentKeepalive**: the number of seconds you wish the client sends a keepalive packet to the server. This is useful if the client is behind NAT or a firewall

## Test the connection

On the client side, run `wg-quick up wg0`. You should now have a working Wireguard connection just like any VPN.

If you found a typo or an error, please use the comment box to report it. Also, if you found the post useful, please share it on social media, so it can reach a larger audience.
