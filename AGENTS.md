# Agent Guide

This is a Cloudflare Worker/D1 OpenAPI example based on the Chanfana template. Its deployment status is not established by the upstream demo URL in the README.

- `src/index.ts` is the router; `src/endpoints/` defines endpoints; `migrations/` owns D1 schema; `wrangler.jsonc` owns Worker and database binding configuration.
- After installing dependencies, run `npm run test` for the declared Wrangler dry run and Vitest suite. Use `npx wrangler d1 migrations apply DB --local` before local development; remote migration and deploy require an explicitly configured D1 database.
- Do not commit secrets. `wrangler.jsonc` already contains a D1 database ID; confirm its account and intended target before any remote migration or deploy.
