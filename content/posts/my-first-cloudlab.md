---
title: "My DevOps cloud lab in AWS with Terraform"
date: 2022-10-23T11:50:11+01:00
draft: false
---
_First edition._

A lot of /r/homelab users setup servers and neworking equipment at home.
I admire that and it is good for learning hardware. But I aint got
any of those at my home for reasons I described in my pervious post about
havimg my own homelab. Instead, I have some DevOps'y
scripts to setup and tear down cloud infrastructure for my experiments.

So lets have a look at what have I done so far.

Terraform is popular choice and easy tool for defining infrastructure in
AWS/GCP/Azure, you can even use it for your self hosted LXD nodes or clusters.

- [github.com/invizus/terraform-aws-vpc](https://github.com/invizus/terraform-aws-vpc)

Above repository is for a reusable terraform module. It will setup a simple
VPC for you with subnets. In previous editions of this module I have also had setup
NAT gateways, but those proved to be too expensive for development and
experiments.

The module is done following same standard as most popular open sourced modules.

- [github.com/invizus/cloud-lab](https://github.com/invizus/cloud-lab)

In this repo I will store my infrastructure that I deploy in AWS. This is where
I also use above VPC module. The only project there at the moment is for setting
up few VMs (EC2 instances) where I plan to install and configure my self-
hosted Kubernetes cluster. Later on that repository will contain ansible
code as well.
## Benefits

What benefits does the above work give me? When I need a place to setup and
experiment some new system, be it opensource or my own, I can spin up some
virtual infra and setup there. On top of that, it is additional learning
experience and proof of my skills.

## Future plans
In my spare time I am thinking what sort of modern application can I make,
something that can utilise all popular AWS components, cost effective
and defined as IaC.
