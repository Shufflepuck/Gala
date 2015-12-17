Gala is comprised of five elements:

* The GUI
* [pymacad](https://github.com/Shufflepuck/pymacad)
* [KerbMinder](https://github.com/pmbuko/KerbMinder)
* [ADPassmon](https://github.com/macmule/ADPassMon)
* [ShareMounter](https://github.com/kylecrawshaw/ShareMounter)

These elements have each an history of their own. As they share a lot of code, we decided to regroup them.

# PyMacAd

PyMacAd is the common module. It is written in Python + Objective-C (PyObjc). When possible, it uses Apple Public APIs, otherwise it uses the command-line tools. To maintain forward compatibility, we decided not to use Apple's Private APIs.

It has different submodules:

* **ad** - for Active Directory (and Open Directory).
* **kerberos** - to initialize, renew and destroy Kerberos tickets. 
* **keychain** - to create and delete entries in the Keychain.

[Read more…](pymacad.md)