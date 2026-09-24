<a href="https://mail.svilenkovic.com/"><img src="media/cover.jpg" alt="Svilenkovic Mail, home page on a laptop and a phone" width="100%"></a>

# Svilenkovic Mail

Webmail for my own mailbox and the client mailboxes I host, with threads, push notifications, scheduled sending and an Android app.

**[mail.svilenkovic.com](https://mail.svilenkovic.com/)** · [Srpski](README.sr.md)

> [!NOTE]
> My own product. The source code is private. This page describes what it does and how it is built.

<table>
  <tr><td><b>Client</b></td><td>Own product</td></tr>
  <tr><td><b>Industry</b></td><td>Webmail for hosted mailboxes</td></tr>
  <tr><td><b>Location</b></td><td>Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Webmail (PWA) with an Android app</td></tr>
  <tr><td><b>My role</b></td><td>Design, development, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>PHP, IMAP/SMTP, MariaDB, WebSocket, PWA, TWA</td></tr>
</table>

## About the project

Svilenkovic Mail is the webmail I use every day, and the one clients use for the mailboxes I host for them. It shows mail as conversation threads, sends push notifications, can hold a message and send it later, and installs on Android like a regular app.

The Android app is a Trusted Web Activity around the same PWA, so there is one codebase and no second client to keep in step. The service worker caches the app shell but never the mail itself. Tapping a notification opens the inbox, or brings an open window to the front. People who prefer a mail app on the desktop or phone do not have to type in settings: every hosted domain answers autoconfiguration requests, so the app finds the server from the address.

## What I built

- Conversation threads that keep replies to the same message together
- Push notifications that open the inbox, or focus it when it is already open
- Scheduled sending: write a message now and let it go out later
- An Android app as a TWA around the PWA, with home screen shortcuts for the inbox and a new message
- Autoconfiguration on every hosted domain, so desktop and phone mail apps set themselves up
- PHP over IMAP and SMTP, with MariaDB and a separate WebSocket service

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Svilenkovic Mail, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Svilenkovic Mail, home page on a phone"></td>
  </tr>
</table>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
