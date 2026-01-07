---
title: Web Application Firewall
date: 2024-12-16
draft: true
description: |
  Configure a Web Application Firewall (WAF) to block known bad bots by identifying them from their user-agent strings (or other characteristics).
weight: 500
tools:
  - anubis
---

A Web Application Firewall (WAF) is a specific kind of firewall which filters and optionally blocks HTTP traffic to a web application such as a repository. A WAF can be configured to block known bad bots by identifying them from their user-agent strings (or other characteristics).

Unlike network firewalls which focus on network-level threats, a WAF understands HTTP and can therefore examnine the content of requests. It uses a combination of pattern-matching (recognising known attack characteristics) and behavioural analysis (identifying unusual activity) to make decisions about which requests to allow and which to block. Most WAFs can be customised with specific rules with options to completely block suspicious requests, require additional verification, or just log them.