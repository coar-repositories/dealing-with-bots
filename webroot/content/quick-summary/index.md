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

1. [Upgrade your repository](/strategies/upgrade-repository/) system if necessary, and consider increasing the hardware resources available to it.
2. Configure and deploy a [robots.txt](/strategies/robots-txt/) file for your repository system
3. Write and publish some [Terms of Service](/strategies/tos/) and ensure that licensing is clearly articulated.
4. Configure a firewall for the local network within which your repository system is hosted, to block IP addresses of known bad bots.

[//]: # (5. Configure a [Web Application Firewall &#40;WAF&#41;]&#40;/strategies/waf/&#41; to block known bad bots by identifying them from their user-agent strings &#40;or other characteristics&#41;)

## Protection

1. Monitor the incoming traffic to your repository system.
2. Adjust your [network firewall](/strategies/network-firewall/) to block network locations of emerging threats from bad bots

[//]: # (3. Adjust your [Web Application Firewall &#40;WAF&#41;]&#40;/strategies/waf/&#41; to block user-agent strings &#40;or other characteristics&#41; of newly identified bad bots)

## Mitigation

1. Configure [rate-limiting](/strategies/rate-limiting/) software to intercede when traffic from bots exceeds a certain threshold.
2. Consider [upgrading your repository hardware](/strategies/upgrade-repository/) further to provide additional resources for dealing with high volumes of traffic.
3. Update your [robots.txt](/strategies/robots-txt/) file to block bots newly identified as "unwelcome"