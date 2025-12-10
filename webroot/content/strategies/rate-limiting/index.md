---
title: "Implement Rate Limiting"
date: 2024-12-16
draft: false
description: |
  Configure rate-limiting software to intercede when traffic from bots exceeds a certain threshold.
weight: 600
---

Traffic rate limiting is a strategy which restricts the number of requests a client can make to a server within a specific time period. When applied to HTTP traffic, when a limit is exceeded, the server may respond with a "429 Too Many Requests" HTTP status code, effectively blocking further requests (perhaps temporarily).

Preferred rates of access can be indicated to clients in [robots.txt](/strategies/robots-txt/).

There are tools available which will enforce rate-limiting, either universally, or on a per-client basis. More sophisticated tools will impose rate limiting on clients which have crossed a configured threshold of requests-per-second.

Different approaches to rate-limiting include (but are not limited to):

1. **Fixed Window Counter:** This allows a maximum number of requests in a fixed time period. Once a client exceeds the limit within that period, further requests are blocked until the next period begins.
2. **Sliding Window Counter:** This logs the timestamps of each request and allows a certain number of requests within a defined duration of time.
3. **Token Bucket:** This allocates "tokens" to a "bucket" at a regular rate and requests consume these tokens. If the bucket runs out of tokens, new requests are denied until the bucket has more tokens to allocate.

