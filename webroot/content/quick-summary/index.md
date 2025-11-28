---
title: "Quick Summary: Recommended Steps"
date: 2024-12-16
draft: false
menu:
  main:
    name: Quick-Summary
    weight: 80
---

The following steps can be followed to mitigate the effects of badly behaved bots on your repository. These steps are grouped into three phases: _Preparation_, _Protection_, and _Mitigation_, as defined in
the [Process for Managing Bots](/process/).

## Preparation

1. [Upgrade your repository](/tools-and-strategies/upgrade-repository/) system if necessary, and consider increasing the hardware resources available to it.
2. Configure and deploy a [robots.txt](/tools-and-strategies/robots-txt/) file for your repository system
3. Write and publish some [Terms of Service](/tools-and-strategies/tos/) and ensure that licensing is clearly articulated.
4. Configure a firewall for the local network within which your repository system is hosted, to block IP addresses of known bad bots.
5. Configure a [Web Application Firewall (WAF)](/tools-and-strategies/waf/) to block known bad bots by identifying them from their user-agent strings (or other characteristics)

## Protection

1. [Monitor the incoming traffic](/tools-and-strategies/monitoring/) to your repository system.
2. Adjust your [network firewall](/tools-and-strategies/network-firewall/) to block network locations of emerging threats from bad bots
3. Adjust your [Web Application Firewall (WAF)](/tools-and-strategies/waf/) to block user-agent strings (or other characteristics) of newly identified bad bots

## Mitigation

1. Configure [rate-limiting](/tools-and-strategies/rate-limiting/) software to intercede when traffic from bots exceeds a certain threshold.
2. Consider [upgrading your repository hardware](/tools-and-strategies/upgrade-repository/) further to provide additional resources for dealing with high volumes of traffic.
3. Update your [robots.txt](/tools-and-strategies/robots-txt/) file to block bots newly identified as "unwelcome"