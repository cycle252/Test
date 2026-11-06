# Cloudflare test counter

A dependency-free web app with a button that increments a counter. The counter is local to the page and resets on refresh.

## Files

- `public/index.html`: responsive page, styles, and counter behavior.
- `wrangler.jsonc`: deploys the `public` directory to the existing Cloudflare Worker named `test`.

## Cloudflare Git deployment

The Worker is connected to `cycle252/Test`, production branch `master`.

- Root directory: `/`
- Build command: leave empty
- Deploy command: `npx wrangler deploy`

Commits to `master` trigger a new deployment. No database, runtime secrets, or package installation is required by the app.

For a local preview, open `public/index.html` in a browser. With Node.js installed, `npx wrangler dev` also previews the app through Cloudflare's local tooling.
