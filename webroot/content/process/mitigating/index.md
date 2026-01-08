---
title: Mitigation
date: 2024-12-16
draft: false
description: |
  The _mitigation_ phase is for actions carried out to reduce the impact of badly-behaved bots on the repository system, especially when the protection measures are unable to prevent overload or denial of service.
weight: 30
strategies:
  upgrade-infrastructure:
    id: upgrade-infrastructure
    order: 1
    description: |
      Consider upgrading the infrastructure (e.g. server hardware, network resources etc.) supporting your repository platform to increase its resilience under load.
  rate-limiting:
    id: rate-limiting
    order: 2
    description: |
      Configure rate-limiting software to intercede when traffic from bots exceeds a certain threshold.
  proof-of-work:
    id: proof-of-work
    order: 5
    description: |
      Implement a "proof-of-work" CAPTCHA or similar to require the visitor to perform a modest amount of computational work before being granted access.
---

Some mitigation measures may be temporary, responding to specific events or periods of high bot activity. Others may be longer-term adjustments to the repository's infrastructure or configuration.

The model allows for badly-behaved (but previously welcome) bots to be declared as unwelcome - especially if the bad-behaviour is perceived to be persistent. In such cases, the various places where unwelcome bots can be identified (e.g. robots.txt) and blocked (e.g. network firewall, WAF, CDN) should be updated accordingly.