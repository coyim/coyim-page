---
layout: post
title:  "Release notes for CoyIM 0.3.8"
date:   2017-06-03 01:01:05
TAG: "note"
categories: coyim update

---

# Release notes for CoyIM 0.3.8

We are very proud to release CoyIM 0.3.8!

This is a small release that primarily fixes some issues and adds smaller features. The last release was meant to be the last in the 0.3 series, but delivery of 0.4 have taken longer than expected. However, this release is not compatible with Golang 1.4 or 1.5.

New features:

- Support new Golang vendoring
- Support reproducible builds for Linux
- \#396 - Support hiding waiting contacts
- Support automatic installation of icons and desktop files
- \#274 - Make it possible to sort by status instead of name
- \#372 - Display pending messages in a clearer way
- \#392 - Give a notification when we verify the fingerprint of a peer
- \#303 - Remember which groups/accounts have been collapsed or not
- \#313 - Make it possible to send messages to offline users

Bug fixes:

- \#390 - Fingerprint missing in "Encryption" tab during account creation
- \#393 - Contact's fingerprints menu does not show the known fingerprints as advertised
- \#389 - Clarify when a password has been saved in the configuration file
- \#237 - Automatically generate author list
- \#399 - If someone cancels entering master password when turning on encryption, we should turn off encryption again
- \#408 - Problem with setting transient on latest Fedora
- \#412 - Inserting a newline with shift-enter should insert that newline where the cursor is, not at the end
- \#400 - We should be better at differentiating connection failures and authentication failures
- Make it possible to press enter to submit a master password
- \#348 - In unified view make it clear which conversation is the current one
- \#413 - Making sure the i18n subsystem is initialized for CLI
- \#423 - Unescape br tags when receiving encrypted content
- \#428 - Remove dukgo.com as possible server
- \#430 and \#431 - Fix several data races
- \#432 - Fix orphaned identity warning
