# Mythical Operator community beta13

Public entry page and tester guide for the first invited round, 15–29 October 2026.

- Live site: https://operator.mythicalbeings.io
- Guide: https://operator.mythicalbeings.io/guide
- Feedback and access requests: https://operator.mythicalbeings.io/feedback
- Private downloads: https://operator.mythicalbeings.io/downloads

This repository contains the static website only. Matching app source and licence notices accompany the private beta delivery. Feedback is accepted through the form only; GitHub Issues and Discussions are disabled.

## Development and publication

No dependencies or build step. Preview with `python3 -m http.server 4178 --bind 127.0.0.1`. Locally, open `/guide.html`; Vercel serves `/guide` with clean URLs and provides the `/feedback` and `/downloads` redirects from `vercel.json`.

The Vercel project is `mythical-operator-site` under `palheiro1s-projects`. It is connected to this repository: every push to `codex/beta13-launch` deploys to production automatically. Production domain: `operator.mythicalbeings.io`. DNS is managed in Cloudflare. Keep form editor links and response workbooks private.

Edit `index.html`, commit the change and push `codex/beta13-launch` to publish sanitized round updates. Verify the Vercel deployment reaches READY and check the public domain after each update. Never publish submissions, addresses, account identifiers or private reports here. The site has no JavaScript, analytics, external fonts or remote artwork.

Code is licensed under AGPL-3.0-or-later; see LICENSE. The original mark in this repository is part of this website.
