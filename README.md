# claimsite-landing

Trust/legitimacy page for ClaimSite at https://claimsite.app

- `/` (index.html) — homepage with founder card + masthead
- `/claim` (claim.html) — demo-site lookup against /api/claim/lookup

Hosted on Cloudflare Pages. No build step — pure static HTML/CSS/JS.

## Routes

Cloudflare Pages serves directory paths. `/claim` resolves to `claim.html` 
via `_routes.json` redirect config.

## Backend dependency

`claim.html` calls `https://app.claimsite.app/api/claim/lookup?q=...`.
CORS is whitelisted for this origin in `biz-site-generator/server.js`.
