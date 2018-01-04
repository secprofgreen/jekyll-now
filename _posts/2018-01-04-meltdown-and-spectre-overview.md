---
layout: post
title: Quick rundown of the Meltdown and Spectre vulnerabilities
published: true
categories: [blog]
tags: [vulnerabilities]
date: 2018-01-04
---

Yesterday, news broke about two new vulnerabilities, dubbed "Meltdown" and "Spectre".  The vulnerabilities are present in CPU chips produced by Intel, AMD, and ARM.  To give you an understanding of the scope of the problem, almost every computing device you own - desktop computer, laptop computer, tablet computer, and even cell phone - relies on one of these chips.  The "Meltdown" vulnerability is present only in Intel chips, while the "Spectre" vulnerability is present in all three chipsets.

The vulnerabilities are different in attack vectors, but the end result is nearly identical.  "Meltdown" takes advantage of a privilege escalation flaw in the Intel chip, which allows access to sensitive memory locations.  "Spectre" works by getting CPUs to run a set of instructions, which ultimately gives access to sensitive memory locations.

Folks, this is about as bad as things can get. When memory can be read, the end result is that anything residing in memory can be copied and used by an adversary. Think credentials for your most sensitive and valuable accounts - banking, financial, medical, password manager - all of that, and more, is vulnerable.

These vulnerabilities cannot be patched, as they reside inside the CPU itself - this is a design flaw. If you read the solution section of [yesterday's CERT update](https://www.kb.cert.org/vuls/id/584653){:target="_blank"}, you'll see that the only way to remove the vulnerability is to replace your chip.

Operating system and software vendors will be releasing software patches to try and lessen the threat posed by these vulnerabilities. However, the threat cannot be removed completely without a basic, fundamental change to CPU architecture by chip manufacturers.  These patches will most likely cause a performance slowdown for impacted systems, although there is some disagreement on the degree to which impacted systems will be slowed down by these patches.

I suggest the following steps for you to follow:

1 - immediately install any patches released by your operating system vendor (Windows, Apple MacOs and iphone IOS), Android, etc.)

2 - immediately install any patches released for any web browser you use (Chrome, Firefox, Safari, Microsoft's Internet Explorer or Edge)

3 - immediately upgrade your web browser if a newer version is released

4 - immediately install any software patch released for any piece of software you have on your system

Tip of the hat to Daniel Miessler ([@DanielMiessler](https://twitter.com/DanielMiessler/){:target="_blank"} on Twitter) for his excellent writeup - found [here](https://danielmiessler.com/blog/simple-explanation-difference-meltdown-spectre/){:target="_blank"} which helped make sense of a lot of this for me!
