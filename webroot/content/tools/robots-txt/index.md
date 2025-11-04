---
title: Robots.txt
date: 2024-12-16
draft: false
menu:
  tools:
    name: Robots.txt
    weight: 10
---

The [Robots Exclusion Protocol](https://doi.org/10.17487/RFC9309) is a web standard, implemented via a [robots.txt](https://www.robotstxt.org/ ) file, which instructs bots about which resources in the repository they may or may not access.

The robots.txt file is a potentially very effective way to *declare* to bots their welcomeness to access the repository, or specific resources in the repository. Its use is nearly ubiquitous in websites in general, and it is very widely understood. Having said that, its effectiveness is somewhat limited by the fact that the Robots Exclusion Protocol does not include any provision for its enforcement. Insofar as repositories enforce this at all, they must do so using various measures such as network-level filtering and Web Application Firewalls.

One COAR Survey respondent described how, in 2019, they had suffered a service outage due to traffic from Google's official web crawler. They were able to prevent this from recurring by carefully configuring their robots.txt file, and their expectation is that they will be able to do the same for the latest generation of what they call "AI bots". However, as we have seen, the growing proportion of "bad bots" implies that robots.txt files may increasingly be ignored.

##### Potential to adversely affect welcome or well-behaved visitors

The Robots Exclusion Protocol, if implemented correctly, is able to be selective and precise in the bots which it declares to be welcome or unwelcome. However, legitimate services which honour the directives in robots.txt files which they encounter when visiting repositories report that these files are frequently badly configured. There is some anecdotal evidence of legitimate, well-behaved bots being turned away by over-zealously configured robots.txt files.

==TODO: Guidance on well written robots.txt file (+ examples?)==