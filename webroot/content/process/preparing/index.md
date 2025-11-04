---
title: Preparation
date: 2024-12-16
draft: false
description: |
  The _preparation_ phase is for actions which can be carried out in advance of any traffic, to prepare the repository for dealing with requests. In this phase the repository service determines the types of visitors it wishes to welcome or make unwelcome. It then declares this through the medium of a robots.txt file, Terms of Service, firewall configurations etc.
weight: 10
tools:
  - "robots-txt"
  - "tos"
  - "upgrade-repository"
  - "network-firewall"
  - "waf"
---

The _preparation_ phase is for actions which can be carried out in advance of any traffic, to prepare the repository for dealing with requests.

In this phase the repository service determines the types of visitors it wishes to welcome or make unwelcome. As a rule, the _raison d'être_ for a repository is to provide wide and open access to its content - both to human visitors, and to well-behaved bots. Some example actions which might be undertaken in this phase include:

- Creating and deploying a [robots.txt](/tools/robots-txt) file
- Writing and publishing some [Terms of Service](/tools/tos) and ensuring that licensing is clearly articulated
- [Upgrade your repository](/tools/upgrade-repository) system if necessary, and consider increasing the hardware resources available to it.
- Configuring a [network firewall](/tools/network-firewall)  to block certain IP addresses (or ranges of addresses)
- Configuring a Web Application Firewall (WAF) to inspect HTTP headers and filter traffic according to certain criteria such as "User Agent".