# Free LootLabs Bypasser

A lightweight LootLabs link processor with a responsive interface.

## Features
- Accepts HTTPS links from `links.lootlabs.gg` and `lootlabs.com`.
- Checks for a publicly exposed standard HTTP redirect.
- Displays a redirect target only when the server explicitly returns one.
- Reports task-gated or inaccessible links clearly.
- No database, accounts, ads, or link history.

This project does not execute page scripts, simulate task completion, forge tokens, or skip required verification.

## Deploy to Cloudflare Pages
1. Connect this GitHub repository to Cloudflare Pages.
2. Framework preset: None.
3. Build command: leave blank.
4. Build output directory: `.`.
5. Deploy. The `functions/api/resolve.js` file is deployed as a Pages Function.

## Local testing
Run `npx wrangler pages dev .` to test the Pages Function locally. Opening `index.html` directly does not provide the API endpoint.