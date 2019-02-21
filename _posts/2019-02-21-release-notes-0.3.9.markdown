---
layout: post
title:  "Release notes for CoyIM 0.3.9"
date:   2019-02-21 01:01:05
TAG: "note"
categories: coyim update 0.3.9

---

# Release notes for CoyIM 0.3.9

We are very proud to release CoyIM 0.3.9!

It's been a longer time than expected, but this release has finally arrived, with a lot of great bug fixes and some new features as well - among those support for SMP and file and directory transfer. Compatibility has also been bumped up to Golang 1.7. Finally, we took the decision to remove the command-line interface, since it was draining resources and didn't seem to have much uptake.

New features:

- [#23](http://github.com/coyim/coyim/issues/23) - Implementation of SMP, with simplified GUI
- [#328](http://github.com/coyim/coyim/issues/328) - Open conversations with specific resources
- [#18](http://github.com/coyim/coyim/issues/18), [#382](http://github.com/coyim/coyim/issues/382) - Transfer files and directories
- [#433](http://github.com/coyim/coyim/issues/433) - Better integration with Tor
- Added more well known Tor Onion Services for XMPP servers
- [#485](http://github.com/coyim/coyim/issues/485) - Prioritize peer name in window title

Bug fixes:

- [#189](http://github.com/coyim/coyim/issues/189) - Button freeze when hover on OS X
- [#391](http://github.com/coyim/coyim/issues/391) - Working search box on OS X
- [#411](http://github.com/coyim/coyim/issues/411) - Mishandled brackets in message text
- [#436](http://github.com/coyim/coyim/issues/436) - Fix OS X accelerators
- [#438](http://github.com/coyim/coyim/issues/438) - Fix registration crash
- [#439](http://github.com/coyim/coyim/issues/439) - Show notifications on latest OS X
- [#441](http://github.com/coyim/coyim/issues/441) - Fix spurious warning
- [#443](http://github.com/coyim/coyim/issues/443) - Don't show menu items that don't make sense without accounts
- [#444](http://github.com/coyim/coyim/issues/444) - Fix hot keys for unified conversations
- [#445](http://github.com/coyim/coyim/issues/445) - Render errors properly when adding accounts
- [#446](http://github.com/coyim/coyim/issues/446) - Search should search nicknames as well
- [#450](http://github.com/coyim/coyim/issues/450) - Unexpected dylib warnings on OS X
- [#464](http://github.com/coyim/coyim/issues/464) - XML console opens multiple times for the same account
- [#465](http://github.com/coyim/coyim/issues/465) - Change how denied subscription requests show up
- [#497](http://github.com/coyim/coyim/issues/497) - Fix Unified view menus
- [#505](http://github.com/coyim/coyim/issues/505) - Fix several issues for Debian packaging

Other changes:

- [#483](http://github.com/coyim/coyim/issues/483) - Remove the CLI
- [#452](http://github.com/coyim/coyim/issues/452) - Improve installation instructions
- [#481](http://github.com/coyim/coyim/issues/481) - Refactor JID handling completely
- Work started on Multi-User Chat
- [#500](http://github.com/coyim/coyim/issues/500) - Updated screenshots on website and in README


