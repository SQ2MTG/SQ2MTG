# Vinted / Vinted Fav — Technical Reference

## Vinted

`SQ2MTG/vinted` is a private TypeScript application-builder workspace. The documented stack includes React 19, TypeScript 5.7, Vite 8, TanStack Router/Start, Nitro, Tailwind 4, Radix UI, React Hook Form, Zustand, Recharts and Playwright.

The application uses Kysely with PostgreSQL/PGLite, Better Auth/JOSE and migration tooling. Development uses `scripts/with-app-env.mjs` and port 8080; the documented build combines Vite with database migration steps.

Authentication and application-data tests are part of the project. Server-side database access must remain isolated from browser code.

## Vinted Fav

`SQ2MTG/vinted-fav` is a separate private JavaScript project focused on organizing Vinted favourites and incomplete seller/item information.

The bookmarklet operates in an authenticated Vinted browser session. It validates the host, redirects to favourites, scans `/items/{id}` links, scrolls the page, extracts item ID/canonical URL/title/image and can send or copy structured JSON.

The browser-side approach exists because direct server-side Vinted HTML scraping can block or hang. Persistence can use Neon PostgreSQL when `DATABASE_URL` is configured or PGLite otherwise, with Kysely providing the SQL abstraction and migrations.

## Security boundary

The bookmarklet inherits the privileges of the authenticated browser session. Database credentials and provider secrets must remain server-side. Vinted-facing automation should be treated as a brittle integration because site markup and anti-automation behavior can change.
