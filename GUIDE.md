# Technical guide

## Structure
- `index.html`: application interface
- `assets/css/style.css`: responsive dark theme
- `assets/js/script.js`: validation, UI state, API call and result handling
- `functions/api/resolve.js`: Cloudflare Pages Function

## Processing flow
1. Browser validates the HTTPS LootLabs hostname.
2. Browser sends the URL to `/api/resolve`.
3. The Pages Function requests the URL with automatic redirects disabled.
4. If the response contains a standard HTTP 3xx Location header, that target is returned.
5. If the response is a task/verification page or exposes no standard redirect, the tool reports that status.

The function does not execute page JavaScript or complete task workflows. Task pages may use cookies, timers, client-side scripts, or server-side verification that cannot be treated as ordinary HTTP redirects.