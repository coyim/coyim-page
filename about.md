---
layout: page
title: About
permalink: /about/
---

CoyIM is a standalone chat client with a focus on safety and security. It is a self contained program that runs on Windows, Linux and OS X. CoyIM only supports one chat protocol - XMPP (which is sometimes known as Jabber). The goal of CoyIM is not to have every feature under the sun. Instead we want to carefully pick and choose the features that are necessary to create a good chat experience, while keeping the attack surface of the system to a minimum.

In addition to choosing features carefully, we have also built in support for Tor, OTR and TLS. The Tor support allows users to become anonymous when chatting. OTR makes end-to-end encryption of communication possible. And TLS adds another layer of encryption to the communication with the chat servers. We have built these features to be core parts of the application - they are not plugins or extras in any way.

CoyIM is implemented in Golang. We made this choice to make it easier to protect our users. Many other implementation languages open up the door for a large number of attacks. We try to minimize those risks by using Golang.

Finally, we want CoyIM to be safe from the moment you start it up. We want it to be possible to just start using the application and everything will be done the right way. In some cases you can turn off the safe defaults, but you will not have to configure anything extra to get all the protection we can give you.

Features that set us apart
===

CoyIM have lots of features that exist in most other chat clients as well - however, there are some things we do differently that most other clients don't do. These are some of the features that set us apart:

* CoyIM has support for the latest version of OTR (a protocol for doing encrypted chat) built in at the core
* CoyIM will automatically detect Tor if it is installed and use it to connect
* It will also automatically use a Tor Onion Service if one is known for the server in question
* It will also use separate Tor circuits for each account, in order to make it harder to tie the accounts together
* If more than one account is configured, when connecting CoyIM will insert random delays before connecting to each account, in order to make fingerprinting of connections between accounts harder
* If Tor is available, CoyIM will do the SRV lookup for the server over Tor
* CoyIM can import both account settings, OTR settings, fingerprints and private keys from other clients such as Pidgin, Adium, Gajim and xmpp-client
* CoyIM can save all your configuration, including OTR fingerprints and keys, in an encrypted configuration file.

Features we want to have
==

Because CoyIM is a young project, there are many things we would like to add that we just haven't had time to add yet. There are many of these, and if you want the full list, the Github issue tracker is your best bet. However, here I wanted to highlight a few things that are very important to us.

* We want CoyIM to be available in many different languages. We currently have basic support in the code for it, but we don't really have any translations yet. We might wait with adding translations until the user interface is less in flux and we have most of the features we want to have.
* We would like to make it possible for CoyIM to create a new anonymous random account for the user with one single option - such that you ask for it, and a few seconds later you have a new account all set up and working. Because of how important compartmentalization is for security, making the setup of new account in a secure way as safe as possible should be as simple as one choice.
* In order to make sure that the CoyIM binaries we are distributing actually come from the source that is in the repository, and nothing else was added, we would like to support complete reproducible builds, so we can easily provide signatures from many different people on the same binary. We have some support for this already, but it needs a lot more work.
* We want to have a way of communicating how secure the current connection is in a simple and nice way, that opens the door for helping users to make the right security choices. We will try doing this using a unified security rating that combines several different measures of security into one number.

Features we probably won't have
==

Creating a program that encourages safe and secure behaviors can sometimes be hard. One thing that contributes is to avoid adding to many features. Features also have a tendency to make for a larger code base - and the larger the code base the more likely it is there will be bugs in the program. Because of this, there are many features other chat clients have that we will probably never have.

* The browser is one of the largest attack surfaces imaginable. And even though vendors are spending a lot of time and money on sandboxing and fixing bugs, it is still risky to do high-security things in a browser. Even though it would make things easier and could make CoyIM look much better, we will never use a browser view to render content inside CoyIM, in order to minimize the risk of successful attacks. For the same reason, we will not support rendering of HTML.
* A related point to the above is links. One of the primary ways attacks are first executed against a user is by fooling them to click a link. For security sensitive situations we need to stop using hyperlinks. CoyIM will not contain any clickable links for this reason.
* CoyIM will not contain emoticons or other kinds of extra graphical features. Adding these things increase the attack surface and make it hard to make sure everything is secure, so we will simply avoid having these features in the first place.
* In order to make things safe and secure, we want the default settings of CoyIM to be safe and secure. User research also show that the more configuration options exist in a program the more confusing it is to users - and the harder it is to make good and safe choices. So from that perspective we might not expose many configuration options.
* Having safe and secure conversations will not always be compatible with the idea of logging. In CoyIM we have decided to not do any logging whatsoever - and if we ever change our minds and implement logging, it will still not be the default - you will have to turn it on manually.

