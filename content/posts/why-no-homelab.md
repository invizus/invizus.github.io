---
title: "Thoughts on having my own homelab"
date: 2022-10-23T11:00:19+01:00
draft: false
---
Have you even been browsing /r/homelab on reddit? A lot of people there like
to  fiddle with hardware. And I mean some of them setup actual server rack
in their own home! And they fill it up with patch panels, cables, network
equipment and even servers.

But it takes a lot of space, produces good amount of noise and burns electricity.

I was lucky to work as a sysadmin and get my hands on all that stuff, and
even design and set it up myself.
My favourite kit is HPE DL 360. Not too expensive and is good for general purpose.
Good engineering behind it.
I also worked with c7000 chassis, variety of firewalls, some storage, switches,
fibre optics.

But I admire those who probably did not get to experience this and work with
such hardware, and we need sysadmins. We especially need sysamins because
majority of hosting is now in the cloud such as AWS, GCP or Azure. Or somewhere
else. But what happens if we run out of actual network admins, sysadmins of
real servers, and so on?

Even though I did it for living for some time, as of year 2022 I still have some
more to achieve.

Below are my thoughts on having a homelab and where to start.

## Servers
Sometimes I see someone is asking online about an old model of server they
bought somewhere for cheap.# Software

### Software
 Sometimes a modern gaming desktop can provide
much more resources for a small development environment. If you only need
to run few virtual machines, learn kubernetes, etc. a virtual machine on
your desktop or in the cloud would be enough for such a task.

Things to learn: virtualisation, fiddle with linux systems.

Things difficult to learn: replication, network storage, clusters.

In production it is important to have redundancy, so you would want to have your
virtual machines or containers replciated, set up in a cluster, or maybe even
accessed via network storage.

### Server hardware
Some old server you found online? Get it, but do not expect much from it. They
are big, heavy and noisy, and old models do not even provide enough performance.
They are good, because servers can accept a lot of memory and CPU cores. This
type of hardware is designed to provide a lot of resources and run 24/7.

Things to learn: hot swap hardware parts like power supply units or disks.

## Network equipment
Getting few network switches may actually be worth it and I consider myself
from time to time. But what I actually want to learn would cost me a fortune.
I want to learn QinQ, LACP over fibre or DAC coper cables, spine and leaf.
This is high performance datacentre stuff and cost a lot of money.

But you can still learn some basics at home with few managed layer 3 switches.

Tings to learn: VLANs. If lucky, SFP modules.

### Patch panels
I suppose you should learn it. Patch panels offer basic structured cabling. It
is quite important to understand how to organise cables, it is easy to neglect it
and very soon it will become a spaghetti nightmare. Lern it, tick the box. Done.

Personally, I have done it and would avoid. I have worked with some horrible RJ45
patch panels before, keystones fall back to 10Mbit/100Mbit or even stop working.

Get the patch panel with punch at the back. These are less flexible but stable.

In datacentres I would try to use DAC or fibre with TOR switches. Server to switch.
Do not bother with patch panels too much.

## Storage
I am not big on the storage. I actually have enterprise storage such as HP MSA.
Why? Just had a bad experience. And they are insanely expensive. If it was me,
I would setup something like ZFS and use consumer grade NVME, or other opensource
linux storage system. You can even setup the replication and deduplication. This
is fun. I will do this whenever I have the opportunity. TODO.

### Other kind of homelab
Get few raspberry pi's and cheap L2 switch, or a small factor PC, such as old
Ubiquity NVR or small lenovo the size of a pencil. Those are fun and don't take
much space or electricity.

## Conclusion
Homelab can be fun but expensive and takes space. It has its limits especially
datacentre networking or storage requires big investment. For small things
like virtualisation or you could use a desktop computer. But it gets more expensive
when you want to setup a production grade cluster for virtualisation.
