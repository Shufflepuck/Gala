---
layout: docs
title: PyMacAd
permalink: /docs/pymacad/
---

PyMacAd is the common module. It is written in Python + Objective-C (PyObjc). When possible, it uses Apple Public APIs, otherwise it uses the command-line tools. To maintain forward compatibility, we decided not to use Apple's Private APIs.

It has different submodules:

* **ad** - for Active Directory (and Open Directory).
* **kerberos** - to initialize, renew and destroy Kerberos tickets. 
* **keychain** - to create and delete entries in the Keychain.

