---
title: "go-away"
date: 2024-12-16
draft: false
source: https://git.gammaspectra.live/git/go-away
---

_go-away_ is described as providing "Self-hosted abuse detection and rule enforcement against low-effort mass AI scraping and bots. Uses conventional non-nuclear options."

It works in a very similar way to [Anubis](/tools/anubis) in that it acts as a Web Application Firewall (WAF) in front of your repository, filtering and monitoring incoming HTTP requests and challenging suspicious requests.

According to the documentation:

> The tool is designed highly flexible so the operator can minimize impact to legit users, while surgically targeting heavy endpoints or scrapers.

> Challenges can be transparent (not shown to user, depends on backend or other logic), non-JavaScript (challenges common browser properties), or custom JavaScript (from Proof of Work to fingerprinting or Captcha is supported)