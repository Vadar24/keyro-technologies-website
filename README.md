# KEYRO Technologies — Website (GitHub-ready static site)

Production website for **gokeyro.com** — KEYRO Technologies, AI Infrastructure for the Modern Business. Flagship product: VEYRA AI.

## Contents

- `index.html` — homepage (hero, VEYRA AI, products, industries, KEYRO Labs, about, demo form)
- `privacy.html` — Privacy Policy (`/privacy.html`)
- `terms.html` — Terms & Conditions, VEYRA AI messaging program (`/terms.html`)
- `assets/` — approved brand images (KEYRO Technologies wordmark, VEYRA AI logo)

The demo form section embeds the live GHL **VEYRA | Demo Request Form** (`D2SZqKthdJUSDtgD7ELh`) via iframe — submissions flow straight into the Keyro GHL sub-account and trigger the Instant Lead Response workflow. "Book a Demo" CTAs link to the GHL demo calendar: `https://api.leadconnectorhq.com/widget/bookings/veyra-ai-book-a-demo`.

No personal identifiers on the site. Contact: contact@gokeyro.com · help@gokeyro.com.

## Deploy (GitHub Pages + gokeyro.com)

Aj's steps (GitHub auth needed — `gh` is not logged in on the build machine):

1. **Create the repo** (e.g. `keyro-technologies-website`) and push this folder's contents to `main`.
2. **Enable Pages:** repo Settings → Pages → Source: Deploy from a branch → Branch: `main`, folder `/ (root)`.
3. **Custom domain:** Settings → Pages → Custom domain: `gokeyro.com` → Save. (This creates the `CNAME` file; or add a `CNAME` file containing `gokeyro.com` at the repo root before pushing.)
4. **DNS at GoDaddy** (gokeyro.com DNS management):
   - `A` @ → `185.199.108.153`
   - `A` @ → `185.199.109.153`
   - `A` @ → `185.199.110.153`
   - `A` @ → `185.199.111.153`
   - `CNAME` www → `<github-username>.github.io`
   - Remove any old A/CNAME records pointing at GoDaddy Website Builder (`keyro6.godaddysites.com`).
5. **Enforce HTTPS** in Pages settings once the certificate issues (~minutes to hours).
6. **Verify:** `https://gokeyro.com/`, `https://gokeyro.com/privacy.html`, `https://gokeyro.com/terms.html` — and submit the demo form once to confirm the GHL workflow fires.

## A2P 10DLC notes

- The campaign's Privacy Policy URL can point to `https://gokeyro.com/privacy.html` and the Terms & Conditions URL to `https://gokeyro.com/terms.html` once live.
- The demo form embedded on the homepage **is** the campaign's opt-in point and carries the SMS consent field.
- Privacy/Terms content was drafted for compliance, not by counsel — have an attorney review before the A2P resubmission cites them.

## Local preview

```bash
cd ~/workspace/keyro-technologies/website && python3 -m http.server 8080
# open http://localhost:8080
```
