# tabaartrading.com

Basic company website for Tabaar Trading: home page (about, services, WhatsApp notice, contact) and privacy policy.
Plain HTML/CSS, no build step. Needed for Meta business verification (the website must show the same legal name,
address and phone as the documents) and as the privacy-policy URL of the WhatsApp app.

Separate from the Deduction Bot (`D:\whatsapp-deduction-bot`, served at bot.tabaartrading.com).

## Company details on the site

Tabaar Trading · Main Sheikhupura Road, Shahdara Mor, Lahore · +92 307 2053838 · info@tabaartrading.com ·
Monday to Saturday, 9:00 am to 5:00 pm · supplier WhatsApp +92 325 9290449.
These must match the documents used for Meta business verification; change them in `index.html` and `privacy.html`.

## Hosting: GitHub Pages (free, HTTPS included)

1. Push this folder to a **public** GitHub repo (e.g. `Tayyab-68/tabaartrading-website`).
   Free GitHub accounts can only publish Pages from public repos; the site is public anyway.
2. Repo → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
   The `CNAME` file already sets the custom domain `tabaartrading.com`.
3. Spaceship → Domain Manager → tabaartrading.com → Advanced DNS, add:

   | Type  | Host | Value                |
   |-------|------|----------------------|
   | A     | @    | 185.199.108.153      |
   | A     | @    | 185.199.109.153      |
   | A     | @    | 185.199.110.153      |
   | A     | @    | 185.199.111.153      |
   | CNAME | www  | tayyab-68.github.io  |

   Do not touch the `bot`, `erp` or MX (email forwarding) records.
4. After DNS has spread (minutes to a few hours), tick **Enforce HTTPS** in Settings → Pages.

## Updating

Edit the HTML, commit, push. GitHub Pages republishes in about a minute.
