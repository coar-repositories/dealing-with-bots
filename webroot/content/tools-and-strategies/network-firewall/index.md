---
title: Network Firewall
date: 2024-12-16
draft: false
recommended: true
weight: 111
---

#### Filtering by Network Origin (IP Address)

The most common measure reported by the community which repositories have employed to mitigate the effect of badly-behaved bots is to use network or server [firewalls](https://en.wikipedia.org/w/index.php?title=Firewall_(computing)) to block access from bots according to their origin IP address.

These kinds of firewalls are ubiquitous in networks and servers and are effective in blocking remote systems so long as the origin IP address is known and stable. However, unscrupulous actors deploying bots at scale are able to utilise large numbers of IP addresses to launch "swarms" of bots, where it becomes very difficult to track and block particular IP addresses.

This approach then becomes one of reacting to a continually changing picture of the network origins of badly-behaved bots, where new IP addresses must be identified and filtered. To help manage this aspect, some respondents to the COAR Survey reported blocking large ranges of IP addresses, in some cases based on those used by popular cloud-based computing infrastructure and, in other cases, based on IP address ranges associated with geographic locations. Some extreme examples of the latter effectively blocked any access from entire countries.

##### Allow-listing and disallow-listing

Sometimes termed "white-listing" and "black-listing" respectively, these terms describe opposite approaches to providing lists of IP addresses for firewalls. With the allow-listing approach, the firewall is configured to block IP addresses by default, allowing only those listed in the allow-list. With the disallow-list approach the opposite applies: the default is to allow all IP addresses except those on the disallow-list.

The disallow-list is the more common approach, especially in an open-access domain.

By using explicit lists, there is an opportunity to share the burden of curation across the community.

##### Potential to adversely affect welcome & well-behaved visitors

Blocking access from particular IP addresses (or ranges of addresses) to repositories has the potential to block well-behaved bots, and even human users. The relationship between a given IP address and a particular client is temporary at best, and IP addresses are routinely re-allocated from one user to another. Furthermore, in the majority of cases it is not possible to associate a particular *type* of visitor - e.g. a user-agent, with particular network addresses.

In particular, the blocking of ranges of addresses has the potential to be indiscriminate, and the larger the range, the more likely it is that legitimate visitors may be blocked.