---
title: Mitigation
date: 2024-12-16
draft: false
description: |
  If a bot is well-behaved then it should be allowed to access the resources it is requesting.
  If a bot is badly-behaved, then the repository (and/or any other components such as network firewalls, CDNs etc.) should take appropriate action. The model allows for badly-behaved (but previously welcome) bots to be declared as unwelcome - especially if the bad-behaviour is perceived to be persistent.
weight: 30
strategies:
  network-firewall: |
    Review and adjust your network firewall to block network locations of emerging threats from bad bots
  waf: |
    Review and adjust your Web Application Firewall (WAF) to block user-agent strings (or other characteristics) of newly identified bad bots
  rate-limiting: |
    Configure rate-limiting software to intercede when traffic from bots exceeds a certain threshold.
  cdn: |
    Consider using emergency measures that may be provided by your Content Delivery Network (CDN)
  upgrade-repository: |
    Consider increasing the hardware resources available to your repository.
---

If a bot is well-behaved then it should be allowed to access the resources it is requesting.

If a bot is badly-behaved, then the repository (and/or any other components such as network firewalls, CDNs etc.) should take appropriate action. The model allows for badly-behaved (but previously welcome) bots to be declared as unwelcome - especially if the bad-behaviour is perceived to be persistent.