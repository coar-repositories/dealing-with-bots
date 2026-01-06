---
title: Context
date: 2024-12-16
draft: false
menu:
  main:
    weight: 20
    parent: Background
  document:
    weight: 10
---

## Introduction
In this website we refer to "bots" as a widely-recognised shorthand term to refer to automated Web clients.

Bots take various forms, but generally they have certain characteristics in common:

* They use HTTP (mostly HTTP GET requests) to retrieve resources in remote systems
* They may retrieve one or many resources from a given system
* They will typically access/retrieve resources from more than one system

Some bots are quite generalised - or even indiscriminate - in the systems and the resources which they access. Others are more specialised, focussing on certain types of resource. Furthermore, some bots simply access the general web interfaces of remote systems - i.e. primarily human-facing websites, while others are directed at APIs that are solely intended for machine interaction.

Historically, bots have been used to catalogue and index Web resources (artefacts made available via URLs), often in service of search engines and aggregating systems. Other purposes might include Web/data "scraping" for specific information, instrumentation/performance benchmarking, as well as more nefarious purposes, such as probing for security vulnerabilities.

There is nothing intrinsically "good" or "bad" about the use of bots to retrieve Web resources. It is important to bear in mind that, although much of this document is concerned with helping repository managers to understand and mitigate a threat from badly-behaved bots, COAR recognises and re-affirms that there are many positive and welcome uses for well-behaved bots accessing repositories.

At the heart of the efforts by the *Dealing With Bots COAR Task Group* to advise repository managers lies an apparent contradiction: COAR continues to advocate that repositories engage as openly as possible with remote systems, while at the same time needing to protect themselves from the worst excesses of a large and growing subset of those remote systems.

## COAR's Vision for Machine-Accessible Repositories
Repositories are dedicated to providing open access to information. For some years, [COAR (The Confederation of Open Access Repositories)](https://coar-repositories.org/ ) has encouraged repositories to ensure that this access is open not only to human users, but also to machine users (bots), through through support of interfaces based on open technologies and standards such as (but not limited to) [OAI-PMH](https://www.openarchives.org/pmh/), [Signposting](https://signposting.org/conventions/) and [COAR Notify](https://coar-notify.net/ ).

The concept of "machine-access" encapsulates access to repositories by software and networked services which directly interact with repositories. COAR considers such machine users (bots) to be "first order" users of repository systems - alongside human users.

## Web Traffic in 20224

In March 2025, Imperva (a subsidiary of Thales) published a report which has been much commented on in trade and mainstream media: _[BAD BOT REPORT: The Rapid Rise of Bots and the Unseen Risk for Business](https://www.imperva.com/resources/resource-library/reports/2025-bad-bot-report/)_. Bad behaviour is defined in broad terms and includes data scraping, brute force login attempts, scalping (automating buying or reserving products), DoS, spamming etc. The graph below is taken from that report.
![](/images/bad-bots-report-screenshot.png)

The headline findings are that **automated-client-generated Web traffic (at 51%) has overtaken human-generated Web traffic** for the first time, and that **"bad bot" traffic, as a proportion of all Web traffic, is rising** - at the expense of both "good bot" and human-generated Web traffic.

## A Growing Threat to Repositories from Badly Behaved Bots
The report from Imperva - especially the startling figure that "bad bots" make up 37% of Web traffic - is borne out by the experiences reported by many repository managers in recent months.

Responding to a sense that this was becoming a community-wide problem, COAR conducted a survey in early 2025 to assess the extent to which repositories were being affected by this. _[The impact of AI bots and crawlers on open repositories: Results of a COAR survey, April 2025](https://coar-repositories.org/wp-content/uploads/2025/06/Report-of-the-COAR-Survey-on-AI-Bots-June-2025-1.pdf)_ - was published in June 2025.

The report found that most repositories were experiencing a significant increase in traffic from bots and that the effects of these bots on repository services was significant. The impact of bot traffic ranged from regular service slow downs through to some instances of major service outages.

The report goes into more detail about the nature and extent of service disruption - and outlines some of the mitigations being employed to try to protect repository services.

It seems apparent that some, perhaps most of this relatively recent growth in "bad bots" is concerned with retrieving web resources at enormous scale, in service of the training and operation of so-called "generative AI" services. However, this website is not concerned with the _purpose_ of badly-behaved bots but is, instead, concerned with the _effect_ of them on the systems which they access.

The increase in the bad behaviour of bots is characterised by Eric Hellman in his blog post, _[AI bots are destroying Open Access](https://go-to-hellman.blogspot.com/2025/03/ai-bots-are-destroying-open-access.html)_:

> The old style bots were rarely a problem. They respected robot exclusions and "nofollow" warnings. [...] Occasionally there would be a malicious bot like a card-tester or a registration spammer. You'd often have to block these based on IP address. It was part of the landscape, not the dominant feature.

> The current generation of bots is mindless. They use as many connections as you have room for. If you add capacity, they just ramp up their requests. They use randomly generated user-agent strings. They come from large blocks of IP addresses.[...] They use up server resources…
