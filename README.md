# Dealing With Bots
This repository contains a collection of resources, coordinated by the *[Dealing With Bots COAR Task Group](./Task%20Group/)*, to aid repository managers in dealing with an emergent problem. The primary output is a website (see _Website_ section below).

## Context

Repositories are dedicated to providing open access to information, and we want to encourage legitimate access to this information - **both by human users and machines alike** - in a spirit of mutual benefit.

This is increasingly challenged by the recent and explosive growth of the activity of (often badly behaved) web crawling systems.

## Problem Statement

The encouragement of repositories to support machine-access is increasingly challenged by the recent and explosive growth of badly behaved bots.

There are, therefore, two inter-related, problems:

## Problem 1 - Overwhelming traffic from bad bots
Open Access repositories are reporting a rapid increase in traffic from bad bots that try to aggressively collect content, and, as a result, overwhelming them with an unreasonably high volume of network requests.There are already reports of repositories having been brought down by such activity.

## Problem 2 - Counter-measures adversely affecting or impeding welcome traffic
Some of the measures which might reasonably be taken by a repository to defend against bad bots have the potential to cause "collateral damage" - that is, to impede legitimate access to the repository by well behaved bots - or even by human users.

## Related Challenges
Addressing these problems is surprisingly challenging, because:

1. The Robots Exclusion Protocol (robots.txt) designed to control or mitigate machine access to web systems such as repositories is being circumvented or ignored by a growing number of bots.
2. It is sometimes difficult to differentiate between human users and bots; this latter point is actually a feature of Web systems which aim to treat human and machine users equivalently - but it can increase the challenge of defending against bad bots. Differentiating between human and machine users is getting harder as bad bots increasingly mimic human access patterns.
3. There is an emergent "arms race" between those designing badly-behaved bots and those attempting to defend against them.

## Website
The primary output of the Dealing With Bots COAR Task Group is a [website](https://dealing-with-bots.coar-repositories.org) used to document the problem and possible solutions or mitigations.

The sources for the website are managed in this repository in the `./webroot` folder. These sources are designed to be run or compiled with Hugo.

To run and view this website on a local server:

1. [Install Hugo](https://gohugo.io/getting-started/installing/)
2. `cd ./webroot`
3. `hugo server`
4. Point your browser at: [http://localhost:1313](http://localhost:1313)
