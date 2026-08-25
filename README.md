# legal

Public site for Vantage Point, served via GitHub Pages at https://getvantagepoint.app

- [index.html](index.html) — landing page + beta waitlist
- [privacy.html](privacy.html) — Vantage privacy policy
- [support.html](support.html) — Vantage support/contact
- `img/` — landing page assets

## Before pushing the landing page

Merging `landing-page` into `main` **is** the go-live action; `main` is exactly what the domain serves.

1. ⚠️ **Verify a real signup end to end.** Kit forms 9840102 (beta) / 9840379 (launch) are our own
   markup posting to Kit's endpoint, and `ck.5.js` is loaded at the foot of `index.html` (Rob's call,
   08-24: load their script, drop the no-tracking claim). Without the script Kit **quarantined**
   every submission (`{"status":"quarantined"}`) while still 302-ing to the thank-you page, so the
   thank-you page is not evidence. Done means: a subscriber appears in Kit and the confirmation
   email arrives. Kit's server-side **Bot filtering** setting is the thing to check if it still
   quarantines with the script loaded.
2. Confirm rights on the historic archive photograph (#327). It is used in the hero, the section
   images, and `img/lines-historic.jpg` on **both** confirmation pages.
