---
title: "Um SMS estranho que me levou a um endereço que copia o site dos CTT"
date: "2020-08-13"
categories: 
  - "geekices"
tags: 
  - "seguranca"
  - "sms"
---

**Caso tenham inserido os dados do vosso cartão de crédito, peçam o cancelamento da subscrição à VodMood através do endereço [customersupport@vodmood.com](mailto:customersupport@vodmood.com)**

Hoje de manhã, ainda não eram 8h30, a esposa recebeu um _SMS_ de um número estranho (5819PT). Ela pediu-me para ver a mensagem porque está a aguardar a receção de documentação através de uma transportadora e queria saber o estado do envio.

Quando vi a mensagem, reparei que o endereço é estranho e não é um que eu tenha visto ser usado pelos _CTT_ ou alguma transportadora. Este endereço, _ajoruc.com_, é "coruja" escrito ao contrário e com um erro ortográfico. Isto pode ser apenas coincidência, mas fez-me desconfiar ainda mais.

Também reparei que não havia acentuação na mensagem, o que pode ser expectável mas não desejável, e que o texto mencionava que o endereço para a entrega não estava confirmado.

Primeiro tentei aceder diretamente ao domínio, que me encaminhou automaticamente para uma página de "_opt-out_". Se já estava bastante desconfiado, ainda fiquei mais.

O passo seguinte foi aceder diretamente à _link_ da mensagem. Quando acedo, encaminha-me para outro endereço, _battser.com_, que é uma cópia do site dos _CTT_. Tentei carregar em várias links e nenhuma funciona, à exceção do botão para pesquisar o suposto "_tracking-code_", que depois de clicado mostra outro botão a pedir para pagar €2.

Quando carreguei neste segundo botão, encaminhou-me novamente para outro endereço estranho, _saferadioplanet.com_, onde pedem vários dados, tais como

- nome
- apelido
- email
- morada
- contacto

Não segui mais qualquer passo depois disto, já que esta situação está tão cheia de _red flags_. Mas como a minha curiosidade ainda não estava satisfeita, tentei ver a informação do primeiro domínio, _ajoruc.com_:

```
Domain Name: AJORUC.COM
Registry Domain ID: 2550042809_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.namecheap.com
Registrar URL: http://www.namecheap.com
Updated Date: 2020-07-31T20:10:44Z
Creation Date: 2020-07-31T20:10:40Z
Registry Expiry Date: 2021-07-31T20:10:40Z
Registrar: NameCheap, Inc.
Registrar IANA ID: 1068
Registrar Abuse Contact Email: abuse@namecheap.com
Registrar Abuse Contact Phone: +1.6613102107
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Name Server: DNS1.REGISTRAR-SERVERS.COM
Name Server: DNS2.REGISTRAR-SERVERS.COM
DNSSEC: unsigned

[...]

Domain name: ajoruc.com                                                                                                                                                                          
Registry Domain ID: 2550042809_DOMAIN_COM-VRSN                                                                                                                                                   
Registrar WHOIS Server: whois.namecheap.com                                                                                                                                                      
Registrar URL: http://www.namecheap.com                                                                                                                                                          
Updated Date: 0001-01-01T00:00:00.00Z                                                                                                                                                            
Creation Date: 2020-07-31T20:10:40.00Z                                                                                                                                                           
Registrar Registration Expiration Date: 2021-07-31T20:10:40.00Z                                                                                                                                  
Registrar: NAMECHEAP INC                                                                                                                                                                         
Registrar IANA ID: 1068                                                                                                                                                                          
Registrar Abuse Contact Email: abuse@namecheap.com                                                                                                                                               
Registrar Abuse Contact Phone: +1.6613102107                                                                                                                                                     
Reseller: NAMECHEAP INC                                                                                                                                                                          
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited                                                                                                           
Domain Status: addPeriod https://icann.org/epp#addPeriod                                                                                                                                         
Registry Registrant ID:                                                                                                                                                                          
Registrant Name: WhoisGuard Protected                                                                                                                                                            
Registrant Organization: WhoisGuard, Inc.                                                                                                                                                        
Registrant Street: P.O. Box 0823-03411                                                                                                                                                           
Registrant City: Panama                                                                                                                                                                          
Registrant State/Province: Panama
Registrant Postal Code: 
Registrant Country: PA
Registrant Phone: +507.8365503
Registrant Phone Ext: 
Registrant Fax: +51.17057182
Registrant Fax Ext: 
Registrant Email: a054ac166e73468694c17ffccea0a1a2.protect@whoisguard.com
Registry Admin ID: 
Admin Name: WhoisGuard Protected
Admin Organization: WhoisGuard, Inc.
Admin Street: P.O. Box 0823-03411 
Admin City: Panama
Admin State/Province: Panama
Admin Postal Code: 
Admin Country: PA
Admin Phone: +507.8365503
Admin Phone Ext: 
Admin Fax: +51.17057182
Admin Fax Ext: 
Admin Email: a054ac166e73468694c17ffccea0a1a2.protect@whoisguard.com
Registry Tech ID: 
Tech Name: WhoisGuard Protected
Tech Organization: WhoisGuard, Inc.
Tech Street: P.O. Box 0823-03411 
Tech City: Panama
Tech State/Province: Panama
Tech Postal Code: 
Tech Country: PA
Tech Phone: +507.8365503
Tech Phone Ext: 
Tech Fax: +51.17057182
Tech Fax Ext: 
Tech Email: a054ac166e73468694c17ffccea0a1a2.protect@whoisguard.com
Name Server: dns1.registrar-servers.com
Name Server: dns2.registrar-servers.com
DNSSEC: unsigned
```

Isto serviu de pouco mas deu para ver que o domínio tem poucos dias.

Com o segundo domínio, a mesma coisa:

```
Domain Name: BATTSER.COM                                                                                                                                                                      
Registry Domain ID: 2548005649_DOMAIN_COM-VRSN                                                                                                                                                
Registrar WHOIS Server: whois.namecheap.com                                                                                                                                                   
Registrar URL: http://www.namecheap.com                                                                                                                                                       
Updated Date: 2020-07-23T14:00:43Z                                                                                                                                                            
Creation Date: 2020-07-23T09:29:17Z                                                                                                                                                           
Registry Expiry Date: 2021-07-23T09:29:17Z                                                                                                                                                    
Registrar: NameCheap, Inc.                                                                                                                                                                    
Registrar IANA ID: 1068                                                                                                                                                                       
Registrar Abuse Contact Email: abuse@namecheap.com                                                                                                                                            
Registrar Abuse Contact Phone: +1.6613102107                                                                                                                                                  
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited                                                                                                        
Name Server: RAJEEV.NS.CLOUDFLARE.COM                                                                                                                                                         
Name Server: ROMINA.NS.CLOUDFLARE.COM                                                                                                                                                         
DNSSEC: unsigned                                                                                                                                                                              

[...]

Domain name: battser.com                                                                                                                                                                         
Registry Domain ID: 2548005649_DOMAIN_COM-VRSN                                                                                                                                                   
Registrar WHOIS Server: whois.namecheap.com                                                                                                                                                      
Registrar URL: http://www.namecheap.com                                                                                                                                                          
Updated Date: 0001-01-01T00:00:00.00Z                                                                                                                                                            
Creation Date: 2020-07-23T09:29:17.00Z                                                                                                                                                           
Registrar Registration Expiration Date: 2021-07-23T09:29:17.00Z                                                                                                                                  
Registrar: NAMECHEAP INC                                                                                                                                                                         
Registrar IANA ID: 1068                                                                                                                                                                          
Registrar Abuse Contact Email: abuse@namecheap.com                                                                                                                                               
Registrar Abuse Contact Phone: +1.6613102107                                                                                                                                                     
Reseller: NAMECHEAP INC                                                                                                                                                                          
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited                                                                                                           
Registry Registrant ID:                                                                                                                                                                          
Registrant Name: WhoisGuard Protected                                                                                                                                                            
Registrant Organization: WhoisGuard, Inc.                                                                                                                                                        
Registrant Street: P.O. Box 0823-03411                                                                                                                                                           
Registrant City: Panama                                                                                                                                                                          
Registrant State/Province: Panama
Registrant Postal Code: 
Registrant Country: PA
Registrant Phone: +507.8365503
Registrant Phone Ext: 
Registrant Fax: +51.17057182
Registrant Fax Ext: 
Registrant Email: c006a1d8ccf94247aefb21eda0fa4eac.protect@whoisguard.com
Registry Admin ID: 
Admin Name: WhoisGuard Protected
Admin Organization: WhoisGuard, Inc.
Admin Street: P.O. Box 0823-03411 
Admin City: Panama
Admin State/Province: Panama
Admin Postal Code: 
Admin Country: PA
Admin Phone: +507.8365503
Admin Phone Ext: 
Admin Fax: +51.17057182
Admin Fax Ext: 
Admin Email: c006a1d8ccf94247aefb21eda0fa4eac.protect@whoisguard.com
Registry Tech ID: 
Tech Name: WhoisGuard Protected
Tech Organization: WhoisGuard, Inc.
Tech Street: P.O. Box 0823-03411 
Tech City: Panama
Tech State/Province: Panama
Tech Postal Code: 
Tech Country: PA
Tech Phone: +507.8365503
Tech Phone Ext: 
Tech Fax: +51.17057182
Tech Fax Ext: 
Tech Email: c006a1d8ccf94247aefb21eda0fa4eac.protect@whoisguard.com
Name Server: rajeev.ns.cloudflare.com
Name Server: romina.ns.cloudflare.com
DNSSEC: unsigned
```

A história não foi diferente no terceiro domínio:

```
Domain Name: SAFERADIOPLANET.COM                                                                                                                                                              
Registry Domain ID: 2509049755_DOMAIN_COM-VRSN                                                                                                                                                
Registrar WHOIS Server: whois.namecheap.com                                                                                                                                                   
Registrar URL: http://www.namecheap.com                                                                                                                                                       
Updated Date: 2020-03-31T12:35:19Z                                                                                                                                                            
Creation Date: 2020-03-30T11:32:35Z                                                                                                                                                           
Registry Expiry Date: 2021-03-30T11:32:35Z                                                                                                                                                    
Registrar: NameCheap, Inc.                                                                                                                                                                    
Registrar IANA ID: 1068                                                                                                                                                                       
Registrar Abuse Contact Email: abuse@namecheap.com                                                                                                                                            
Registrar Abuse Contact Phone: +1.6613102107                                                                                                                                                  
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited                                                                                                        
Name Server: CASH.NS.CLOUDFLARE.COM                                                                                                                                                           
Name Server: JANET.NS.CLOUDFLARE.COM                                                                                                                                                          
DNSSEC: unsigned                                                                                                                                                                              

[...]

Domain name: saferadioplanet.com                                                                                                                                                                 
Registry Domain ID: 2509049755_DOMAIN_COM-VRSN                                                                                                                                                   
Registrar WHOIS Server: whois.namecheap.com                                                                                                                                                      
Registrar URL: http://www.namecheap.com                                                                                                                                                          
Updated Date: 0001-01-01T00:00:00.00Z                                                                                                                                                            
Creation Date: 2020-03-30T11:32:35.00Z                                                                                                                                                           
Registrar Registration Expiration Date: 2021-03-30T11:32:35.00Z                                                                                                                                  
Registrar: NAMECHEAP INC                                                                                                                                                                         
Registrar IANA ID: 1068                                                                                                                                                                          
Registrar Abuse Contact Email: abuse@namecheap.com                                                                                                                                               
Registrar Abuse Contact Phone: +1.6613102107                                                                                                                                                     
Reseller: NAMECHEAP INC                                                                                                                                                                          
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited                                                                                                           
Registry Registrant ID:                                                                                                                                                                          
Registrant Name: WhoisGuard Protected                                                                                                                                                            
Registrant Organization: WhoisGuard, Inc.                                                                                                                                                        
Registrant Street: P.O. Box 0823-03411                                                                                                                                                           
Registrant City: Panama                                                                                                                                                                          
Registrant State/Province: Panama
Registrant Postal Code: 
Registrant Country: PA
Registrant Phone: +507.8365503
Registrant Phone Ext: 
Registrant Fax: +51.17057182
Registrant Fax Ext: 
Registrant Email: 1101df4e23a9474a8ee40938ad2d3b1f.protect@whoisguard.com
Registry Admin ID: 
Admin Name: WhoisGuard Protected
Admin Organization: WhoisGuard, Inc.
Admin Street: P.O. Box 0823-03411 
Admin City: Panama
Admin State/Province: Panama
Admin Postal Code: 
Admin Country: PA
Admin Phone: +507.8365503
Admin Phone Ext: 
Admin Fax: +51.17057182
Admin Fax Ext: 
Admin Email: 1101df4e23a9474a8ee40938ad2d3b1f.protect@whoisguard.com
Registry Tech ID: 
Tech Name: WhoisGuard Protected
Tech Organization: WhoisGuard, Inc.
Tech Street: P.O. Box 0823-03411 
Tech City: Panama
Tech State/Province: Panama
Tech Postal Code: 
Tech Country: PA
Tech Phone: +507.8365503
Tech Phone Ext: 
Tech Fax: +51.17057182
Tech Fax Ext: 
Tech Email: 1101df4e23a9474a8ee40938ad2d3b1f.protect@whoisguard.com
Name Server: cash.ns.cloudflare.com
Name Server: janet.ns.cloudflare.com
DNSSEC: unsigned
```

Ainda tentei ver se o [crimeflare.org](http://www.crimeflare.org:82/cfs.html) tinha algum destes domínios listado, mas não tive sorte.

Perguntei no _Twitter_ e no _Slack_ do [_AADM_](https://abertoatedemadrugada.com/) sobre este tipo de mensagens e parece que esta é uma prática relativamente comum.

Por [sugestão do Tomahock](https://twitter.com/tomahock/status/1293821947432894466), reportei isto ao _Centro Nacional de Cibersegurança_ e talvez siga a [dica do @rafaelraposo](https://twitter.com/rafaelraposo/status/1293851500205268992) e reporte também a situação à empresa que fornece o alojamento e/ou domínios usados nisto.

Alguns _screenshots_ [estão nesta _thread_ no _Twitter_](https://twitter.com/brunomiguel/status/1293818511857459201).

_**Update #1:**_ reportei os domínios à _Namecheap_, mas o _ticket_ ainda não tem qualquer _feedback_ da empresa

_**Update #2:**_ a Namecheap já respondeu e está a averiguar a situação do lado deles
