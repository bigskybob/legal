# legal

Public site for Vantage Point, served via GitHub Pages at https://getvantagepoint.app

- [index.html](index.html) — landing page + beta waitlist
- [privacy.html](privacy.html) — Vantage privacy policy
- [support.html](support.html) — Vantage support/contact
- `img/` — landing page assets

## Before pushing the landing page

1. ⛔ **THE FORMS DO NOT WORK YET — do not push index.html.** Kit forms 9840102 / 9840379 are
   wired, but Kit **quarantines** any submission lacking their reCAPTCHA token
   (`{"status":"quarantined"}`), while still 302-ing to the thank-you page. It looks like it
   worked and no subscriber is created. Fix requires loading `ck.5.js` (which also fires a
   per-visitor tracking beacon) or another approach. Rob's call, pending.
2. Confirm rights on the historic archive photograph used in the hero and section images (#327).
3. Re-test a real signup end to end once the form approach is settled.
