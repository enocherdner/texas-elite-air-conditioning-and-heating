# Making this theirs — the three things a client will ask for

Everything below is a small edit to `index.html` in this folder, then:

    ~/.atlas/bin/client publish <this-folder-name>

## 1. Their logo

Put the file in this folder as `logo.png` (transparent PNG) or `logo.svg`.
Then find the **LOGO SLOT** comment near the top of the `<body>` and delete the
`<!--` and `-->` around the `<img class="logo">` line. That is the whole job.

Sizing, spacing and the dark-header contrast are already handled.

## 2. Their photographs — the single biggest upgrade

Put three landscape photos in this folder as `work-1.jpg`, `work-2.jpg`, `work-3.jpg`.
Find the **PHOTO SLOTS** comment and replace each

    <div class="shot"><span>Photograph of recent work<br>goes here</span></div>

with

    <img class="shot" src="work-1.jpg" alt="Say what the job was">

Ask for these on the second call. It is the best reason to ring back, it makes the
page genuinely better, and it costs them nothing.

## 3. Their own domain

    ~/.atlas/bin/client domain <this-folder-name> theirdomain.com

Prints the exact DNS records the domain owner has to set. Up to a day, then HTTPS
switches itself on. **Register it in their name, not yours.**

---

## The enquiry form

Posts to **FormSubmit** at `enocherdner@gmail.com`. The very first submission triggers
a one-off confirmation email — **click it, or the form silently stops working.**
Send yourself one test enquiry before showing this to anyone.

When they become a client, change the address in the `<form action=...>` line to theirs.

## Colours

Every colour is a variable at the top of the `<style>` block: `--brand`, `--deep`,
`--tint`. Change those three and the whole page follows, dark mode included.

## What must not change

Every fact on this page is sourced in `FACTS.md`. Do not add opening hours, prices,
guarantees, licences, review text or "insured" unless the owner tells you it is true.
A page that states one wrong thing about a business loses the deal on the spot.

---

# Insights — what you tell them each month

The page already counts the two things a trade business actually cares about:

- **Call tapped** — someone pressed the phone number
- **Enquiry sent** — someone filled the form

Pageviews are vanity. "Eleven people tapped your number last month" is the sentence
that renews a retainer.

## Switching the counting on (5 minutes, free)

1. **dash.cloudflare.com** → Analytics → **Web Analytics** → Add a site
2. Enter the site's URL, copy the `<script>` tag it gives you
3. Paste it in `index.html` where it says `<!-- ANALYTICS TAG GOES HERE -->`
4. Republish

Free forever, no cookies, so no cookie banner is needed. One Cloudflare account
covers every client site.

If you'd rather hand the client their own live dashboard, **Plausible** ($9/mo)
has a shareable public link — worth it once a few clients are paying.

## The monthly note

    ~/.atlas/bin/client report <this-folder-name>

Writes REPORT.md — the short message you send the owner at month end. Put the
call and enquiry numbers in it. That report is most of what the retainer buys.
