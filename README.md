# Haugtun

The market-facing landing page for **Haugtun** — a market-guidance initiative by **Adarsh S**, an Authorised Person with Angel One. The site covers structured account onboarding, brokerage plans, and an enquiry form for prospective clients.

🌐 **Live:** [haugtun.in](https://haugtun.in)

## Overview

Haugtun is a lightweight, dependency-free static site (plain HTML, CSS, and vanilla JavaScript) deployed via **GitHub Pages** on a custom domain. It is a standalone project — its only outbound link is a "View Portfolio" link to [samadarsh.vercel.app](https://samadarsh.vercel.app).

## Features

- **Responsive single-page layout** — hero, approach, offers, onboarding process, brokerage plans, about, contact, and enquiry sections.
- **Sticky navigation** with a mobile menu toggle and scroll-spy that highlights the active section.
- **Account opening CTAs** linking directly to Angel One onboarding (app and web) for each brokerage plan.
- **Authorised Person card viewer** — a lightbox to preview the card front/back.
- **Enquiry form** that posts submissions to a Google Apps Script web app endpoint.
- **Plausible analytics** with tagged outbound-link and custom event tracking.
- **Dynamic copyright year** in the footer.

## Project structure

```
.
├── index.html          # Page markup and content
├── haugtun.css         # Styles
├── haugtun.js          # Nav, scroll-spy, card lightbox, enquiry form
├── assets/haugtun/     # Authorised Person card images (front/back)
├── CNAME               # Custom domain (haugtun.in)
└── .nojekyll           # Disable Jekyll processing on GitHub Pages
```

## Local development

No build step or dependencies are required. Serve the folder with any static server, for example:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Configuration

- **Enquiry endpoint** — set `ENQUIRY_ENDPOINT` in `haugtun.js` to your Google Apps Script web app URL.
- **Analytics** — the Plausible script tag in `index.html` is configured for the `haugtun.in` domain.

## Deployment

Hosted on **GitHub Pages**. Pushing to the `main` branch automatically deploys to [haugtun.in](https://haugtun.in) (configured via the `CNAME` file).

## Disclaimer

Adarsh S operates as an Authorised Person with Angel One and does not provide investment advisory services or guaranteed returns. All market participation involves risk and should be approached responsibly.
