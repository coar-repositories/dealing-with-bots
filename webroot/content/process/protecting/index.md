---
title: Protection
date: 2024-12-16
draft: false
description: |
  The *protection* phase is for actions carried out in response to particular requests, or patterns of requests. This involves monitoring traffic (e.g. through inspection of web logs). A busy repository deals with a continuous flow of incoming HTTP GET requests for its resources. These requests need to be evaluated to determine if the visitor is welcome, and to decide whether or not its behaviour is acceptable. The repository then needs to react, by deciding what action to take. 
weight: 20
tools:
  - "robots-txt"
  - "network-firewall"
  - "waf"
  - "monitoring"
  - "captcha"
  - "cdn"
---

The *protection* phase is for actions carried out in response to particular requests, or patterns of requests. This involves monitoring traffic (e.g. through inspection of web logs).

A busy repository deals with a continuous flow of incoming HTTP GET requests for its resources. These requests need to be evaluated to determine if the visitor is welcome, and to decide whether or not its behaviour is acceptable. The repository then needs to react, by deciding what action to take.

This involves the following steps:

1. For incoming traffic, distinguish between welcome and unwelcome visitors.
2. For bot traffic, evaluate the behaviour of the bot.
3. Take further action as necessary.

### 1. For incoming traffic, distinguish between welcome and unwelcome visitors

This step in the process depends upon the repository's ability to identify visitors to the extent that they can be recognised as welcome or unwelcome. Various techniques for achieving this can be used.

Until relatively recently, the difficulty of distinguishing between incoming human and bot Web traffic ranged from straightforward to challenging but was generally manageable. This situation has changed with the advent of AI bots that, at times, use very sophisticated techniques to access web sites while often masquerading as other visitors.

A paper by four Belgian researchers from KU Leuven, _[Balancing Security and Privacy: Web Bot Detection, Privacy Challenges, and Regulatory Compliance under the GDPR and AI Act](https://doi.org/10.12688/openreseurope.19347.1)_, covers the security and privacy aspects of identifying bad bots. It states that the techniques which could potentially be used to identify visitors closely resemble those of trackers used in surveillance industries. Using such techniques would, therefore, almost certainly raise a range of privacy regulation aspects that repositories would be eager to avoid.

Bearing this in mind - together with the findings from the previously mentioned Imperva report about the nature of bot behaviour in the "education sector" - the approach could - at this point - focus on dealing with less sophisticated bots and postpone dealing with bots that are hard to identify/handle (e.g. swarms of headless javascript-capable browsers) at a later stage. This approach has the advantage of keeping the technical requirements for repository managers under control.

### 2. For bot traffic, evaluate the behaviour of the bot

At this stage, the visitor has been identified as a bot and, based on available information such as its origin network address and its self-declared software "agent", its welcomeness has been ascertained.

An unwelcome bot which has attempted to access the repository is, according to the model, badly-behaved. Note that all bots should be welcome to access certain resources - notably the repository's robots.txt file - so an attempt to access such a resource does not constitute bad behaviour.

It is worth noting that a bot which is initially welcome may still exhibit bad-behaviour. For example, a bot which is permitted access to particular resources according to the repository's robots.txt file might still overwhelm the repository with "aggressive" rates of retrieval.

