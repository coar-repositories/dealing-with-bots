---
title: "Apache Module: mod_ratelimit"
date: 2024-12-16
draft: false
source: https://httpd.apache.org/docs/current/mod/mod_ratelimit.html
---

This is a module which can be added to the widely-use Apache web server. Many repositories use Apache as their webserver.

According to [the documentation](https://httpd.apache.org/docs/current/mod/mod_ratelimit.html), the module provides a filter named RATE_LIMIT to limit client bandwidth. The throttling is applied to each HTTP response while it is transferred to the client, and not aggregated at IP/client level. The connection speed to be simulated is specified, in KiB/s, using the environment variable rate-limit. Optionally, an initial amount of burst data, in KiB, may be configured to be passed at full speed before throttling to the specified rate limit. This value is optional, and is set using the environment variable rate-initial-burst.