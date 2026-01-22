---
title: Proof of Work
date: 2024-12-16
draft: false
description: |
  Require the visitor to perform a modest amount of computational work before being granted access
weight: 900
github_issue: "https://github.com/coar-repositories/dealing-with-bots/issues/17"
tools:
  - anubis
  - go-away
  - cloudflare
---

Proof of Work (PoW) is a technique which requires visitors to perform a modest amount of computational work before being granted access to a resource. This approach can help deter bots by making it costly for them to access the resource, or even block them by posing a challenge that they cannot meet, while still allowing human users to access the resource.

While proof-of-work can be an effective deterrent against badly-behaved bots, it can be indiscriminate, adversely affecting legitimate bot access. For this reason, it is often best used in conjunction with other bot management strategies, and perhaps as a last resort in situations where the risk of bot abuse is particularly high.
