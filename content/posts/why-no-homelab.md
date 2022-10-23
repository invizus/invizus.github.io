---
title: "Thoughts on having my own homelab"
date: 2022-10-23T11:00:19+01:00
draft: true
---
A lot of folks in /r/homelab have their own homelab at their homes.
Servers, storage, patch panels, and so on.

Luckily in my past jobs I had some hands on experience with enterprise
servers like HP DL360, c7000 chassis, network equipment and firewalls and
some more. I even got a chance to participate in designing infrastructure
in a new datacentre. That covers the experience bit with hardware. Fiddling
with hardware is great part of experience, but it does not require that
much time as the software part of system and infrastructure administratrion.

### Servers
I think that some of the reasons why some folks in /r/homelab do this:
either to achieve same experience for their CV/resume, or just as a hobby.
Myself, I simply do not have space for that much stuff, on top fo that
servers are very noisy and consume a lot of electricity. I like my servers
and systems 24/7, that would cost a lot.

Some time in past I did buy a 1U old generation Dell server and some cheap
Cisco switches and router from eBay. They were noisy, not powerful, network
equipment was not suitable for my internet setup and I did not have much
infrastructure to play with. But I tried.

Servers are good if you need a lot of CPU and RAM, I am talking 50+ CPU or
256GB RAM. Howver, if you only need to run few virtual machines or containers,
a modern gaming desktop would sufficient.

However if you still want a rack server at home, you can get below benefits:

- Servers can offer more CPU and Memory than a desktop. Imagine you could
have 56 CPUs and 256GB RAM? Cannot do it with desktop PC.
- Hardware experience. In my opinion, HP servers hardware design is amazing,
it is easy and pleasure to work with. A lot of business grade servers support
hot swappable PSU and disks, hardware disk raid, iLO/DRAC or other remote
management.
- Enterprise or ZFS storage
- But other than that, you do not need a powerful server for your
home to spin up some network management, storage or even a small gaming
server. Dell should be good too, don't have experience with others.
- Netowrking. If you have few good L3 switches, you could try and setup
something like spine-leaf or non blocking redundant nework, and in that
case your two interfaces on your server would be useful to setup in LACP
mode. For experience, but you do not need this level of redundancy at home.

### Networking
Networking equipment, on the other hand, has different set of features that
servers do not offer. This is where having homelab will benefit. Imagine
setting up storage VLAN, fibre cables and customer VLANS? Things to learn:
- various SPF module types
- various cabling like fibre, DAC, ethernet
- Various VLANS: C-VLAN and Q-inQ
- Topologies like spine and leaf

But this tipe of equipment is expensive and you would not do with just
one piece to get the most out of it. This is something I would do at
my home given the opportunity, unless I do it for clients.

### Patch panels
Horrible. I have done some in past. The patch panels with RJ45 keystones
from both sides, so you could connect trunk cables easily - these are the
worst. I have seen them fail often, downgrading to 100Mbit. Maybe it is just
me?

The patch panels that you have to terminate at the back with TIA 568 A/B
standard, I believe they are more stable.

Do you always need a patch panel? For datacentre I would avoid, besides in
datacentres, with powerfull servers which can virtualise a lot of workload
and servers that pass a lot of traffic, Ethernet is no longer enough. You
shold consider 10Gbit network, DAC cables or fibre. So in this case, if
possible, connect your equpiment directly to switches.

For home? Definitely. Go with the patch panel where you can terminate cables
behind.

### Other kind of homelab
I have seen quite often people setup small Raspberry Pi clusters, small
L2 switches. Yeah this stuff is more enthusiastic and fun. Sometimes they
can be enough for small services like running a web server, VPN, secure
DNS, backups and automation scripts, and so on. These things are also
small, not noisy and do not consume much electricity.

## Conclusion
If I had an opportunity, I would have setup a whole rack of equipment,
ranging from few DL360, commodity ZFS storage, or even NVME storage,
spine and leaf networking, firewalls, fibre and dac cables, but that
would cost a lot of money, electiricty and what would I do with it? 

Not logical.

What will I do one day: few raspberry pi's and a netgear switch.

What am I doing now: check out my next post about cloud lab.
