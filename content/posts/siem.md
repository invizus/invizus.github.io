---
title: "SIEM. Why scoping environment is important."
date: 2022-10-02T23:52:56+01:00
draft: false
---
SIEM stands for Security Information and Event Management. Log management and
notifications is a part of PCI DSS requirements and not optional in case of
SAQ D. 

Activity on your network should be logged and sent to SIEM for analysis. Such
activity includes user activity on workstations and servers, also various system
events on your network - servers, firewalls, switches. Logs from your network can
be used in event of breach to rebuild a picture what was happening. These logs can
be sent to SIEM system for analysis and alerting.

An example: someone can install a virus on your network for the purpose of stealing
data. With SIEM it is possible to narrow down to where did such event happen, whose
credentials were used and on which workstation. This is theoretical example but in
reality will depend on your setup.

SIEM system can be quote sophisticated and requires a lot of resources such as time,
funding, and may require management approval. For some it can be quite difficult to
comprehend the whole system but once setup, maintaining it can be somewhat easier task.
SIEM, like all the security, is not the type of "setup and forget" system, continuous
maintenance and monitoring+review would be needed. Daily in the beginning, but as you
configure and polish it, it would need less attention. Log reviews on the other hand
is important.

There are different vendors out there, and may have various licencing models. One example
is the volume of logs received.

The more computers you have on your network the more activity will be logged. However it
is possible to minimize this: computers having access to your CDE can be moved into a
separate network which would be called "PCI environment" (or CDE). Computers (or staff)
who do not need to have access to the system which holds card data, they can be considered
outside of scope. The process is called: segmentation.

Reducing the scope, or if put this different way - having less computers with access to
your business system, would mean:

- Lower SIEM solution cost
- Less activity logged which means less to review daily, less alerts and easier management
- Lower risk of breach
- Proper scoping of environment would not only cost cheaper, but would also involve less
maintenance and reduce the risk for your business.
