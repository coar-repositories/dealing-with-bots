---
title: "Process: Quick Summary"
date: 2024-12-16
draft: false
menu:
  main:
    name: Quick-Summary
    weight: 50
---

The following steps can be followed in mitigating the effects of badly behaved bots on your repository.

## Preparation
1. Configure and deploy a [robots.txt](/tools/robots-txt) file for your repository system
2. [Upgrade your repository](/tools/upgrade-repository) system if necessary, and consider increasing the hardware resources available to it.
3. Write and publish some [Terms of Service](/tools/tos) and ensure that licensing is clearly articulated.
4. Configure a [network firewall](/tools/network-firewall) to block network addresses of known bad bots
5. Configure a [Web Application Firewall (WAF)](/tools/waf) to block known bad bots by identifying them from their user-agent strings (or other characteristics)

## Protection
1. [Monitor the incoming traffic](/tools/monitoring) to your repository system.
2. Adjust your [network firewall](/tools/network-firewall) to block network locations of emerging threats from bad bots
3. Adjust your [Web Application Firewall (WAF)](/tools/waf) to block user-agent strings (or other characteristics) of newly identified bad bots

## Mitigation
1. Configure [rate-limiting](/tools/rate-limiting) software to intercede when traffic from bots exceeds a certain threshold.
2. Consider [upgrading your repository hardware](/tools/upgrade-repository) further to provide additional resources for dealing with high volumes of traffic.
3. Update your [robots.txt](/tools/robots-txt) file to block bots newly identified as "unwelcome"