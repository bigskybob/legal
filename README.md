# legal

Public site for Vantage Point, served via GitHub Pages at https://getvantagepoint.app

- [index.html](index.html) — landing page + beta waitlist
- [privacy.html](privacy.html) — Vantage privacy policy
- [support.html](support.html) — Vantage support/contact
- `img/` — landing page assets

## Before pushing the landing page

Merging `landing-page` into `main` **is** the go-live action; `main` is exactly what the domain serves.

1. ✅ **Signup verified end to end (2026-08-24).** Kit forms 9840102 (beta) / 9840379 (launch) are our
   own markup posting to Kit's endpoint; `ck.5.js` at the foot of `index.html` attaches to them and
   Kit answers `{"status":"success"}` (without the script Kit quarantines every POST). Confirmation
   emails send from `rob@getvantagepoint.app` (Porkbun forward → Gmail; Kit verified domain: CNAMEs
   `ckespa`, `cka._domainkey`, `cka2._domainkey` + `_dmarc` TXT). mail-tester 9.4/10, DMARC pass,
   and a Gmail-alias signup received its confirmation in the inbox.
   ⚠️ Each Kit form's confirmation email has its **own** sender — a new form must be switched to
   the domain address by hand; the account default does not carry over.
   ⚠️ The thank-you page is never evidence: Kit redirects there for any submission.
2. Confirm rights on the historic archive photograph (#327). It is used in the hero, the section
   images, and `img/lines-historic.jpg` on **both** confirmation pages.
