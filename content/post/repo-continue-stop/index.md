---
title: "Deciding to continue or end my third-party Arch Linux repository"
summary: "My third-party Arch Linux repository went offline. The fix is trivial, but the hosting provider is on its last breath."
description: "My third-party Arch Linux repository went offline. The fix is trivial, but the hosting provider is on its last breath."
date: 2023-02-22
categories:
  - "geekices"
tags:
  - "userrepository"
  - "repository"
  - "Arch Linux"
  - "personal project"
  - "tough decidions"
cover:
  image: "post/repo-continue-stop/images/mike-enerio-H58bnmnedTc-unsplash.webp"
  alt: "Aerial view of a crossroad"
---

Up to this point, the hosting for my third-party Arch Linux repository was done by Fosshost, where I also volunteered since the late 2020s. Fosshost has been crumbling for over a year, and the last months have been terrible for the project. Even so, the server hosting my repository has been working OK, despite having incredibly slow I/O performance. That allowed me to keep the repository running.

On Monday night, after a kernel update, I rebooted the VM. It never came back up. The server where the virtual machine is located runs Proxmox, and this is a known issue of that Proxmox version. When I tried to log in to the backend, I discovered that the authentication system in front of Proxmox was down. Also, the hardware supporting that authentication system was shut down, apparently due to lack of payment, and no one from the team has a way to fix that.

I knew this would eventually happen. Regardless, I hoped I had time to find a new home for the repo that was cheap enough to afford, given my particularly shitty circumstances. I may have found one, but I would have to pay for three months each time.

Now, I'm faced with a choice: either pay for the new hosting, postpone bringing it back up until I can afford it, or pull the plug on the project. If it weren't for fibromyalgia and how it turned my life upside down, this would be a no-brainer, and I would even subscribe to one of that provider's _root server_ plans because it has excellent prices. But the situation isn't a "perfect scenario" one, and a choice needs to be made.

For my project, the bare minimum resources are slightly high: 200 GB of disk space, 6 GB of RAM, and 6 vCPUs. Having to compile over 2000 packages gets you there, trust me, especially if you have a few kernels, NodeJS software with its dependency hell, and so on and so forth.

The provider I'm looking into has a plan with 6 vCPUs, 8 GB of RAM, and 160 GB of disk space for €11,44/month with no contract period, but bills every three months. Also, the disk space is tight. I could likely make do with it, but adding new packages would be out of the question until I could find a way to work around that.

They have another plan close to what I can afford per month. It costs €15,68/month and has 8 vCPUs, 12 GB of RAM, and 360 GB of disk space. This plan, however, is also billed every three months.

If they billed every month, I could accommodate the cost, even if I had to skip my meds a few days every month to postpone the medication expense as much as possible. Having to pay three months upfront, however, is difficult. Keep in mind that I'm on paid sick leave that doesn't even reach €260/month, there are other expenses besides medication, and fibromyalgia isn't my only health issue that requires medication.

I don't know what to do. I really want to keep the repository running, but paying three months each time would put me in a situation where, every three months, I couldn't afford at least most of my medication for a month. If you've read my fibromyalgia blog or know me in real life, you know that the fibromyalgia medication doesn't stop the pain, but at least it prevents it from being even more intense. With the meds, the pain level baseline is high (or violent, as a rheumatologist, with whom I had medical appointments, described it); without them, the baseline is an insane pain level that keeps me from getting out of bed.

Whatever the decision, I'll have to take it until the end of the week.

<small>Photo from [Unsplash](https://unsplash.com/pt-br/fotografias/H58bnmnedTc)</small>
