---
title: Preparation
date: 2024-12-16
draft: false
description: |
  The _preparation_ phase is for actions which can be carried out in advance of any traffic, to prepare the repository for dealing with requests. In this phase the repository service determines the types of visitors it wishes to welcome or make unwelcome. It then declares this through the medium of a robots.txt file, Terms of Service, firewall configurations etc.
weight: 10
strategies:
  robots-txt: |
    Configure and deploy a `robots.txt` file for your repository system
  tos: |
    Write and publish some Terms of Service and ensure that licensing is clearly articulated.
  upgrade-repository: |
    Upgrade your repository system if necessary, and consider increasing the hardware resources available to it.
  network-firewall: |
    Configure a firewall for the local network within which your repository system is hosted, to block IP addresses of known bad bots.
  waf: |
    Configure a Web Application Firewall (WAF) to block known bad bots by identifying them from their user-agent strings (or other characteristics)
---

The _preparation_ phase is for actions which can be carried out in advance of any traffic, to prepare the repository for dealing with requests.

In this phase the repository service determines the types of visitors it wishes to welcome or make unwelcome. As a rule, the _raison d'être_ for a repository is to provide wide and open access to its content - both to human visitors, and to well-behaved bots. Some example actions which might be undertaken in this phase include:

- Creating and deploying a [robots.txt](/strategies/robots-txt/) file
- Writing and publishing some [Terms of Service](/strategies/tos/) and ensuring that licensing is clearly articulated
- [Upgrade your repository](/strategies/upgrade-repository/) system if necessary, and consider increasing the hardware resources available to it.
- Configuring a [network firewall](/strategies/network-firewall/)  to block certain IP addresses (or ranges of addresses)
- Configuring a Web Application Firewall (WAF) to inspect HTTP headers and filter traffic according to certain criteria such as "User Agent".