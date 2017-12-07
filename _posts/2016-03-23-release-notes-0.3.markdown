---
layout: post
title:  "Release notes for CoyIM 0.3"
date:   2016-03-23 01:01:01
TAG: "note"
categories: coyim update

---

# Release notes for CoyIM 0.3

We are very proud to release CoyIM 0.3 with a lot of interesting new features and important bug fixes!

New features:

- Improved configuration options
- Alternative single view layout
- Allow associating (local) nicknames and groups with peers
- Allow for flexible handling of TLS certificates, including pinning
- Support Tor over Unix domain socket
- Support for configuring require encryption per peer
- Allow for turning on or off encryption of the configuration file
- Remove older conversation content
- Change conversation text input to allow for multiple lines
- Support arbitrary servers for registration
- Improve registration flow to make it clear what is happening
- Improve setup screen to allow importing, adding or registering accounts
- Better behavior for checking whether we are using Tor or not
- Choose what private key to import when importing from a file with several keys

Bug fixes:

- \#276 - Don't strip out HTML from text
- Fix broken tests on Go 1.6
- \#261 - Allow for trying to send messages while connecting, without crashing
- Invoking the program twice will now open up the original window
- \#257 - When disconnecting on purpose, we shouldn't try to reconnect
- \#223 - Don't pop up more than one password dialog
- \#232 - We shouldn't crash on Windows

Other changes:

- Allow for more TLS cipher suites when connecting
- Better feedback on failure in various situations
- Improve the add contact dialog, and add more functionality
- Display version from the command line
- Several new known servers with onion services
