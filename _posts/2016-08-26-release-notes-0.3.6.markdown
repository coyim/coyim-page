---
layout: post
title:  "Release notes for CoyIM 0.3.6"
date:   2016-08-26 01:01:04
categories: coyim update
---

# Release notes for CoyIM 0.3.6

We are very proud to finally release CoyIM 0.3.6!

This is a small release that primarily fixes some issues and adds notification support for all platforms.

New features:

- Add support for notifications on OS X and Windows
- \#268 - Add support for manually testing connection
- \#335 - Make it possible to save password when entering it
- \#350 - Add support for setting display name of local account
- \#304 - Make it configurable to show empty groups

Bug fixes:

- Changes to notification settings should take effect immediately
- Only show relevant notification settings for the platform in question
- \#280 - Clarify several of the status messages to improve understanding of encryption changes
- \#345 - Don't hide people that are initially away
- \#346 - Display communication window when OTR failures happen
- \#347 - Remove race condition in password entry

