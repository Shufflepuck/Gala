---
layout: docs
title: ADPassMon
permalink: /docs/adpassmon/
---
![adpassmon icon](https://github.com/macmule/ADPassMon/wiki/images/icon_256x256.png)

## Overview
ADPassMon is a small menu bar application that shows the number of days remaining until your Active Directory password expires. ADPassMon features:

* support for Mac OS X 10.8 through 10.11
* optional Notification Center notifications with adjustable warning period
* integrated Kerberos ticket renewal
* Keychain password synchronization
* Change Password menu item, with optional password requirements reminder
* offline functionality via cached expiry information
* MCX support for ease of administration. ([Read more here](./Customization))

This software is released under the [MIT license](./License).

## Why ADPassMon?
Most Active Directory sites require users to change their passwords at regular intervals – such as every 30, 60, 90, or 180 days. Unless you write your password expiration date on a calendar or set some other sort of reminder, it’s possible that your password will expire before you’ve had a chance to change it.

Mac OS X’s AD integration does a decent job mitigating this issue. Since Mac OS 10.4, users with impending password expirations will be notified when they log in. If their password is set to expire within 24 hours, they will be forced to change their password before being allowed to log in. Administrators can adjust how long before password expiration to start showing these login screen warnings, but this is not a foolproof solution. If users don’t regularly log out of their computers, they might go weeks without visiting the login screen, completely missing the warning period.

ADPassMon was designed to keep users informed about upcoming password expirations regardless of their computer use habits.

## Features

**ADPassMon**, short for Active Directory Password Monitor, places an item in the menu bar that shows the number of days remaining until the password expires, simply and unobtrusively. Here it is on the left side.

![menubar item](https://github.com/macmule/ADPassMon/wiki/images/menu.png)

Hovering your cursor over the icon reveals more precise information in a tooltip.

![tooltip](https://github.com/macmule/ADPassMon/wiki/images/menu_tooltip.png)

Clicking on the menu item reveals some additional features, which I’ll discuss further below.

![menu items](https://github.com/macmule/ADPassMon/wiki/images/menu_down.png)

Selecting the Preferences item reveals the program’s configuration options. Note the message area at the top of the window. It will normally display the full password expiration information, but if can also display errors or other messages affecting use of the application.

![prefs window](https://github.com/macmule/ADPassMon/wiki/images/prefs1.png)

### Auto or Manual Mode

By default, ADPassMon attempts to automatically acquire all the information it needs to calculate your password expiration information. This will not work in all environments, so the option to set the maximum password age manually is provided. If Auto mode results in an incorrect or negative password expiration value, then you should use Manual mode and provide your site’s maximum password age in days.

### Notification Center Alerts ###

ADPassMon can optionally send you notifications of impending password expirations using OS X's Notification Center alerts. Check the **Enable Notifications** box and enter the number of days before the password expires that you want the warnings to start appearing. Warnings will appear every 12 hours after the threshold is reached. Each warning will resemble the following:

![notification](https://github.com/macmule/ADPassMon/wiki/images/menu_notification.png)

Clicking the **Change** button will bring up the [Change Password dialog](https://github.com/macmule/ADPassMon/wiki#change-password).

### Kerberos Tickets

ADPassMon can also acquire and/or renew Kerberos tickets for you. In OS 10.6, Apple buried the graphical Kerberos ticket management tool — Ticket Viewer.app — inside the /System/Library/CoreServices folder. ADPassMon lets you request a new ticket or renew an existing ticket right from its menu. (A Kerberos ticket is required if you’re using Auto mode, so you’ll be prompted to obtain a ticket if you launch ADPassMon and don’t have a ticket.) This menu item will be disabled if the app cannot communicate with your AD domain.

### KerbMinder Integration

If you have [KerbMinder](https://github.com/pmbuko/KerbMinder) installed, ADPassMon will show an extra menu option that lets you enable and disable it.

### Change Password

ADPassMon lets you choose between two methods of changing your account passwords:

**Native OS**, which uses the standard password change window found in the Users & Groups preference pane.

![os password method](https://github.com/macmule/ADPassMon/wiki/images/change_pass1.png)

**ADPassMon**, which uses ADPassMon's own dialog box to change the password and automatically sync the keychain password at the same time.

![ADPassMon password method](https://github.com/macmule/ADPassMon/wiki/images/change_pass2.png)

### Check Keychain at launch

When this option is enabled, ADPassMon will check to see if the user's keychain is locked when it launches. This is performed by trying to unlock the user's keychain. If it cannot unlock the keychain, the user is prompted to update their keychain password.

### App Reset

If you’re experiencing trouble with ADPassMon, you can clear the settings and return the application to defaults by selecting the Reset tab in the Preferences window and clicking the Revert to Defaults button.

![prefs reset](https://github.com/macmule/ADPassMon/wiki/images/prefs2.png)
