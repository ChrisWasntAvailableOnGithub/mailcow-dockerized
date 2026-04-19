# mailcow: dockerized - 🐮 + 🐋 = 💕

[![Translation status](https://translate.mailcow.email/widgets/mailcow-dockerized/-/translation/svg-badge.svg)](https://translate.mailcow.email/engage/mailcow-dockerized/)
[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/mailcow_email.svg?style=social&label=Follow%20%40mailcow_email)](https://twitter.com/mailcow_email)
![Mastodon Follow](https://img.shields.io/mastodon/follow/109388212176073348?domain=https%3A%2F%2Fmailcow.social&label=Follow%20%40doncow%40mailcow.social&link=https%3A%2F%2Fmailcow.social%2F%40doncow)


## Want to support mailcow?

Please [consider a support contract with Servercow](https://www.servercow.de/mailcow?lang=en#support) to support further development. _We_ support _you_ while _you_ support _us_. :)

You can also [get a SAL](https://www.servercow.de/mailcow?lang=en#sal) which is a one-time payment with no liabilities or returning fees.

Or just spread the word: moo.

## Many thanks to our GitHub Sponsors ❤️
A big thank you to everyone supporting us on GitHub Sponsors—your contributions mean the world to us! Special thanks to the following amazing supporters:

### 100$/Month Sponsors
  <a href="https://www.colba.net/" target=_blank><img
    src="https://avatars.githubusercontent.com/u/204464723" height="58"
  /></a>
  <a href="https://www.maehdros.com/" target=_blank><img
    src="https://avatars.githubusercontent.com/u/173894712" height="58"
  /></a>

### 50$/Month Sponsors
  <a href="https://github.com/vnukhr" target=_blank><img
    src="https://avatars.githubusercontent.com/u/7805987?s=52&v=4" height="58"
  /></a>

## Info, documentation and support

Please see [the official documentation](https://docs.mailcow.email/) for installation and support instructions. 🐄

🐛 **If you found a critical security issue, please mail us to [info at servercow.de](mailto:info@servercow.de).**

## ApolloMC branding

1. Log in as **admin** and open **System > Configuration > Customization**.
2. In **UI labels and texts**, set:
   - Title name: `ApolloMC Mail`
   - Main name: `ApolloMC Mail`
   - Apps name: `ApolloMC Apps` (optional)
3. In the same page, upload your ApolloMC light/dark logos in the logo section and save.

## Quick setup tutorial

1. Open **Email > mailcow Configuration** and in the **Domains** tab add your domain (example: `example.com`).
2. In your DNS provider, add these records for that domain:
   - `MX` -> your mail host (example: `mail.example.com`)
   - `A/AAAA` for `mail.example.com` -> your server IP
   - `TXT` SPF (example): `v=spf1 mx -all`
   - `TXT` DKIM -> copy from **Configuration > DKIM**
   - `TXT` DMARC (example): `v=DMARC1; p=quarantine; rua=mailto:postmaster@example.com`
   - `CNAME` autodiscover/autoconfig -> `mail.example.com` (optional but recommended)
3. Wait for DNS propagation, then verify records from the DNS information/check tools in the **Domains** area (or with `dig`/external DNS checkers).
4. In the same page, open the **Mailboxes** tab and create accounts:
   - Click add mailbox
   - Set local part (e.g. `info`)
   - Select domain
   - Set password/quota and save
5. Test login in webmail (SOGo) and with an email client:
   - IMAP: port 993 (SSL/TLS)
   - SMTP submission: port 587 (STARTTLS) or 465 (TLS)
   - Username: full email address
6. Send a test mail to/from an external mailbox and confirm SPF/DKIM/DMARC pass in message headers.
7. Optional hardening: enforce 2FA for admins and review spam/ratelimit settings after first successful delivery.

## Cowmunity

[mailcow community](https://community.mailcow.email)

[Telegram mailcow channel](https://telegram.me/mailcow)

[Telegram mailcow Off-Topic channel](https://t.me/mailcowOfftopic)

[Official 𝕏 (Twitter) Account](https://twitter.com/mailcow_email)

[Official Mastodon Account](https://mailcow.social/@doncow)

Telegram desktop clients are available for [multiple platforms](https://desktop.telegram.org). You can search the groups history for keywords.

## Misc

**Important**: mailcow makes use of various open-source software. Please assure you agree with their license before using mailcow.
Any part of mailcow itself is released under **GNU General Public License, Version 3**.

mailcow is a registered word mark of The Infrastructure Company GmbH, Parkstr. 42, 47877 Willich, Germany.

The project is managed and maintained by The Infrastructure Company GmbH.

Originated from @andryyy (André)
