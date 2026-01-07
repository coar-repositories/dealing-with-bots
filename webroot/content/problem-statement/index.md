---
title: Problem Statement
date: 2024-12-16
draft: false
menu:
  main:
    name: "Problem-Statement"
    weight: 30
    parent: Background
---

There are two, inter-related, problems:

## Problem 1 - Overwhelming traffic from badly-behaved bots
Open Access repositories are reporting a rapid increase in traffic from badly-behaved bots that try to aggressively collect content, and, as a result, overwhelming them with an unreasonably high volume of network requests.There are already reports of repositories having been brought down by such activity.

## Problem 2 - Counter-measures adversely affecting or impeding welcome traffic
Some of the measures which might reasonably be taken by a repository to defend against badly-behaved bots have the potential to cause "collateral damage" - that is, to impede legitimate access to the repository by well behaved bots - or even by human users.

## Related Challenges
Addressing these problems is surprisingly challenging, because:

1. The Robots Exclusion Protocol (robots.txt) designed to control or mitigate machine access to web systems such as repositories is being circumvented or ignored by a growing number of bots. 
2. It is sometimes difficult to differentiate between human users and bots; this latter point is actually a feature of Web systems which aim to treat human and machine users equivalently - but it can increase the challenge of defending against badly-behaved bots. Differentiating between human and machine users is getting harder as badly-behaved bots increasingly mimic human access patterns. 
3. This difficulty in differentiation between human users and bots also affects the collection and analysis of metrics or web usage statistics, which are important for repositories to understand how their content is being used.
4. There is an emergent "arms race" between those designing badly-behaved bots and those attempting to defend against them.
