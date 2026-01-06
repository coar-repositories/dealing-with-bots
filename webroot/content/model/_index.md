---
title: A Model for Characterising Bots
date: 2024-12-16
draft: false
menu:
  main:
    name: A Model for Characterising Bots
    weight: 40
    parent: Background
---

It is clear that, in this rapidly changing internet environment, repository services face a challenge in deciding how to deal with bots as a majority subset of their visitors. The following model is intended to help repository managers understand and respond to this challenge.

Before we turn to characterising bots, it should be remembered that incoming traffic from bots is interleaved with traffic from *human* users. It is not always easy to differentiate between these, and the model needs to take account of this. While the model is primarily focussed on bots, it uses the term *visitors* when covering traffic from both humans and bots.

Any decision-making process for dealing with bots needs to recognise that access from bots can be desirable or undesirable. Much of the commentary around this issue uses the terms "good bots" and "bad bots". However this dichotomy is, perhaps, a little too simplistic to underpin a decision-making process.

In this model, we characterise bots according to two criteria:

1. Whether the bot is **welcome** or **unwelcome** to access the repository (or certain resources in the repository).
2. Whether the bot exhibits **good behaviour** or **bad behaviour** in its interactions with the repository.

An interesting affordance of this model is that a bot can be *welcome*, but also be *badly-behaved*. In such a case, a repository might indicate in advance that a bot is welcome to access its resources, but then need to take measures to deal with its unanticipated bad-behaviour. And, of course, a previously welcome bot which displays bad behaviour might become unwelcome as a result.

This distinction between *welcomeness* and *behaviour* allows us to make clearer recommendations about how to deal with bots in general. For example, some actions which a repository service might wish to take are *pro-active* and concerned with welcomeness, while others are *re-active* and largely about responding, in real-time, to bad-behaviour.

## Welcomeness

The welcomeness of a visitor to a repository is a matter of policy for that repository. Any practical steps that repositories might take to express welcomeness and, crucially, convey this to visitors are, therefore, necessarily *proactive*.

This model describes bots (and indeed all visitors) as either welcome or unwelcome. In the domain in question - that of open-access repositories - it is assumed that visitors are, by default, welcome. Additionally, while it may become the case that an increasing number of bots are unwelcome, it is further assumed that all human users are welcome.

In this model, the welcomeness of visitors is established through various identifying characteristics. For example:

- will the visitor be a human user or a bot?
- will the visitor come from a particular network location (e.g. an IP address or range of addresses)?
- will the bot declare itself to be from a list of known "agents"?

Welcomeness may be further refined to apply to specific resources, rather than to the whole repository system.

## Behaviour

The behaviour of a bot is assessed at the time that the bot interacts with the repository. Any practical steps that repositories might make to identify, assess and (optionally) mitigate the behaviour of bots are, therefore, necessarily *reactive*.

We can broadly assess different behaviours of bots as either "good" or "bad".

### Good Behaviour

The IETF's Network Working Group has a draft document, *[Crawler Best Practices](https://datatracker.ietf.org/doc/draft-illyes-aipref-cbcp-00)*, which describes "best practices for web crawlers", summarised thus:

1. Crawlers must support and respect the Robots Exclusion Protocol.
2. Crawlers must be easily identifiable through their user agent string.
3. Crawlers must not interfere with the regular operation of a site.
4. Crawlers must support caching directives.
5. Crawlers must expose the IP ranges they are crawling from in a standardised format.
6. Crawlers must expose a page that explains how the crawled data is used and how it can be blocked.

This is a useful list of good behaviours and can be applied to the interactions of bots, in general, with repositories.

In general, bots which exhibit these behaviours ensure that they identify themselves and their source systems' network locations reliably, which provides the target system (repository) with the opportunity to deny access to them. In addition, they comply with directives from the target system about which resources may be accessed.

### Bad Behaviour

It follows, therefore, that bots which do not adhere to these good practices are exhibiting bad behaviour. Badly behaved bots might be placed in one of two categories, depending on whether or not the harm being done is *intentional* or not:

1. Bots which are used to intentionally harm the "target" system. These might include bots which seek and exploit known security vulnerabilities in commonly used systems, or bots deployed (often in numbers) to effect a "[Denial of Service Attack](https://en.wikipedia.org/w/index.php?title=Denial-of-service_attack)" against a target system.
2. Bots which as a side-effect of their interaction with a remote system cause *unintentional* harm to that system. Such harm is often in terms of overloading the remote system such that it becomes less responsive, or even crashes.

The first of these categories has been common for some time and, to an extent, web services have evolved to mitigate this direct threat. However, as previously noted, the Web has seen a recent and rapid growth of the second of these categories.

Most of the bad behaviour identified by repository managers in the COAR survey relates to a failure to observe two of the good-practices identified above:

**Crawler Best Practice #1: Crawlers must support and respect the Robots Exclusion Protocol**

The Robots Exclusion Protocol (robots.txt) is the primary mechanism by which repositories can explicitly declare the welcomeness of a bot. Bots which ignore directives expressed through this mechanism are considered to be badly-behaved. **It follows that bots which have been explicitly declared unwelcome but which, nonetheless, attempt to access a repository are, by definition, badly-behaved.**

**Crawler Best Practice #2: Crawlers must not interfere with the regular operation of a site**

The most common problem reported in the COAR survey is of repository services being overwhelmed by the rate and volume of traffic from particular bots - either acting singly or in "swarms". Where the rate or volume of traffic from a bot causes the degradation of the repository service - in terms of performance or stability - then that bot can be considered to be badly behaved.