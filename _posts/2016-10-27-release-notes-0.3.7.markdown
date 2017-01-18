---
layout: post
title:  "Release notes for CoyIM 0.3.7"
date:   2016-10-27 01:01:04
TAG: "note"
categories: coyim update

---

# Release notes for CoyIM 0.3.7

We are very proud to release CoyIM 0.3.7!

This is a small release that primarily fixes some issues and adds smaller features.

It is worth noting that this release is the last release in the 0.3 series, and the final release that will be compatible with Golang 1.4 and 1.5.
From 0.4 we will only support Golang 1.6 and up.

New features:

- Change color scheme for outgoing text
- Small spelling fixes in error messages
- \#307 - Implement rendering of /me
- \#385 - Show contacts that have been asked but not confirmed in the roster
- \#342 - Make it possible to use Emacs style keyboard shortcuts
- \#375 - Implement "disconnect all"
- \#275 - Warn when we see a new OTR fingerprint
- \#321 - Implement an XMPP console for debugging
- \#370 - Give feedback when "secure chat" button is pressed
- Add coyim.desktop template for Linux

Bug fixes:

- \#368 - Fix issues when switching between unified and multiple windows
- \#376 - Allow reducing the size of the conversation window in the unified view
- \#341 - Make ctrl-w in unified view close the current view
- \#363 - Allow importing Pidgin-style private keys from Yahoo or other types of accounts
- \#168 - Notify a user when Google is stopping them from logging in
- \#273 - Add more documentation about the libotr file format
- Make sure we are only showing going offline notifications when the peer is actually going offline
- \#371 - Fix a bug with starting a new secure conversation after we have ended an old one
- \#367 - Stop crash when switching between unified and multiple view
- Fix problem in OTR when too many messages caused a stuck condition
- Fix problem where delayed messages got lost
- Fix problem with duplicated ending notifications
- Fix problem with resending of delayed messages
- \#359 - We don't want to crash if we can't start the notification subsystem on Linux

