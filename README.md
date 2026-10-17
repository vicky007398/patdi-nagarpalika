# Patdi Nagarpalika — Gujarati Municipal Website Demo

A mobile-first Gujarati municipal information portal built for Cloudflare Workers, D1 and static assets. **This is a demonstration, not an authorized government website.**

## Pages
Homepage, services, departments, notices, events, gallery, contact, citizen suggestions, and an admin placeholder. Public content comes from D1; citizen suggestions are written to D1. **Admin authentication and content editing are NOT implemented yet.**

## Setup
1. Run `npm install`.
2. Create a Cloudflare D1 database called `patdi-nagarpalika-db` in the Cloudflare dashboard or with `npx wrangler d1 create patdi-nagarpalika-db`.
3. Replace `REPLACE_WITH_YOUR_D1_DATABASE_ID` in `wrangler.jsonc` with the database UUID.
4. Run `npx wrangler d1 execute patdi-nagarpalika-db --remote --file=./schema.sql`.
5. Run `npm run deploy` after authenticating with Cloudflare, or connect the repository to Cloudflare Workers Builds with build command `npm install` and deploy command `npx wrangler deploy`.
6. For local development, initialize the local database with `npx wrangler d1 execute patdi-nagarpalika-db --local --file=./schema.sql` and run `npm run dev`.

## Security / publication
Do not use this demo as an official government site without written authorization, accessibility and security review, appropriate domain/hosting policy review, privacy notice, retention policy, spam prevention and rate limiting. Public suggestions currently have no spam protection. Do not collect sensitive personal data. There are no administrator credentials in this repository.
