---
title: "Anubis"
date: 2024-12-16
draft: false
---

[Anubis](https://anubis.techaro.lol) is an open-source Web Application Firewall (WAF) designed to protect web applications from various types of attacks. It is designed to be deployed in front of a web application - such as a repository - to filter and monitor incoming HTTP requests. It is smart enough to distinguish between browsers and bots on the one hand, and simpler, low-level processes (such as RSS readers) on the other.

Anubis is primarily focused on blocking bots which are mimicking the behaviour of browsers, and which may be attempting to scrape content, perform brute-force attacks, or exploit vulnerabilities in the web application. Essentially, when it identifies a request as potentially coming from a bot, it challenges the requester to prove that it is a human user - optionally by completing a [CAPTCHA](/strategies/captcha). If the requester successfully completes the challenge, it is allowed to proceed to the web application; otherwise, the request is blocked. This means that Anubis may block even well-behaved bots, if they have not been identified as welcome (in robots.txt for example).

Anubis is highly configurable and can be tailored to the specific needs of a repository. If you have already defined your [robots.txt](/strategies/robots-txt/) file (which you ought to have done!), Anubis provides a tool - [robots2policy](https://anubis.techaro.lol/docs/admin/robots2policy/) - to automatically generate some starting rules based on your robots.txt file.