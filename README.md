# legal

Public site for Vantage Point, served via GitHub Pages at https://getvantagepoint.app

- [index.html](index.html) — landing page + beta / launch signups (Kit forms)
- [privacy.html](privacy.html) — privacy policy (the app, the site, the list, the form, the community)
- [terms.html](terms.html) — terms of use (Apple's standard EULA governs the app; the rest in plain English)
- [support.html](support.html) — support + FAQ (the App Store support URL)
- [thanks.html](thanks.html) / [thanks-beta.html](thanks-beta.html) — Kit post-signup redirects
- [confirmed.html](confirmed.html) / [confirmed-beta.html](confirmed-beta.html) — Kit post-confirm redirects
- [404.html](404.html) — GitHub Pages picks this up for missing paths
- `feedback/` → the Notion feedback form · `community/` → r/VantagePointApp (redirect pages, noindex)
- [site.css](site.css) — the shared theme for every page except `index.html`, which keeps its own inline styles; both use the same tokens (the app icon's twilight band, cream mark, warm paper)
- `img/` — assets

**`main` is exactly what the domain serves.** Pushing to `main` is the go-live action.

## Editing the legal pages

- Both legal pages carry an **effective date** in the band. Bump it when the substance changes; git history is the changelog and both pages link to it.
- The privacy policy's load-bearing claim is "the app has no network path." Any future network feature (sync, telemetry, StoreKit is fine) reopens `privacy.html`, the App Store privacy label, and the trust card on the landing page.
- The canonical text lives here, not in the app repo. `ahwahnee/docs/legal/PRIVACY-POLICY.md` is a pointer.

## Signup plumbing (verified end to end 2026-08-24)

Kit forms 9840102 (beta) / 9840379 (launch) are our own markup posting to Kit's endpoint; `ck.5.js`
at the foot of `index.html` attaches to them and Kit answers `{"status":"success"}` (without the
script Kit quarantines every POST). Confirmation emails send from `rob@getvantagepoint.app`
(Porkbun forward → Gmail; Kit verified domain: CNAMEs `ckespa`, `cka._domainkey`, `cka2._domainkey`
+ `_dmarc` TXT). mail-tester 9.4/10, DMARC pass.

- ⚠️ Each Kit form's confirmation email has its **own** sender — a new form must be switched to the
  domain address by hand; the account default does not carry over.
- ⚠️ The thank-you page is never evidence: Kit redirects there for any submission.

## The historic photograph

“Masonic Building, ca 1924,” San Leandro Historical Photograph and Document Collection (Sirsi asset 5385/0),
credited in the hero caption, the footers, and `terms.html` §8. Pre-1931 US publication → very
likely public domain by age; the library's interest is the scan + credit. Courtesy ask to the
History Room drafted (#327); capture day replaces these placeholders with Rob's own footage.
