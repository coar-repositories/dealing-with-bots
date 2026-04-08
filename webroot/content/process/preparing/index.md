---
title: Preparation
date: 2024-12-16
draft: false
description: |
  The _preparation_ phase is for actions which can be carried out in advance of any traffic, to prepare the repository for dealing with requests. In this phase the repository service determines the types of visitors it wishes to welcome or make unwelcome.
weight: 10
strategies:
  upgrade-repository: 
    id: upgrade-repository
    order: 1
    description: |
      Upgrade your repository system if necessary, and consider increasing the hardware resources available to it.
  robots-txt:
    id: robots-txt
    order: 2
    description: |
      Configure and deploy a `robots.txt` file for your repository system
  tos:
    id: tos
    order: 3
    description: |
      Write and publish some Terms of Service and ensure that licensing is clearly articulated.
  network-firewall:
    id: network-firewall
    order: 4
    description: |
      Configure a firewall for the local network within which your repository system is hosted, to block IP addresses of known bad bots.
  waf:
    id: waf
    order: 5
    description: |
      Configure a Web Application Firewall (WAF) to block known bad bots by identifying them from their user-agent strings (or other characteristics)
  upgrade-infrastructure:
    id: upgrade-infrastructure
    order: 6
    description: |
      Evaluate the infrastructure (e.g. server hardware, network resources etc.) supporting your repository platform to determine its likely resilience under anticipated load.
---

Some example actions which might be undertaken in this phase include:

- Creating and deploying a [robots.txt](/strategies/robots-txt/) file
- Writing and publishing some [Terms of Service](/strategies/tos/) and ensuring that licensing is clearly articulated
- [Upgrade your repository](/strategies/upgrade-repository/) system if necessary, and consider increasing the hardware resources available to it.
- Configuring a [network firewall](/strategies/network-firewall/)  to block certain IP addresses (or ranges of addresses)
- Configuring a Web Application Firewall (WAF) to inspect HTTP headers and filter traffic according to certain criteria such as "User Agent".