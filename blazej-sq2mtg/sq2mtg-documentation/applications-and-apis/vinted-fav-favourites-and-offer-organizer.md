# Vinted Fav — favourites and offer organizer

## Repository

`SQ2MTG/vinted-fav` is a private JavaScript/TypeScript application on `main`. GitHub currently reports no declared repository license.

## Toolchain

The package manifest documents React 19, TypeScript 5.7, Vite 8, TanStack Router/Start, Tailwind CSS 4, Zustand, Radix UI, Recharts, React Hook Form and Playwright, with Kysely, PostgreSQL (`pg`) and PGlite on the data side.

## Development

The development environment uses `scripts/with-app-env.mjs` and Vite on port `8080`:

```bash
npm install
npm run dev
```

Build, migration, typecheck, authentication checks, tests, lint and formatting scripts are also defined in the package manifest.

## Project scope

The project is documented as a Vinted favourites/offer organizer. Earlier technical documentation describes a browser-side bookmarklet workflow because authenticated Vinted pages can block or hang when collected server-side. Exact selectors, request schemas and Vinted integration behavior must be verified against the current source before being treated as stable interfaces.

## Data and authentication

Kysely supports PostgreSQL and PGlite configurations. Better Auth and JOSE are used for authentication/session handling. User/session isolation and server-side secret handling should remain explicit implementation invariants.

## Security

The bookmarklet runs in the user's authenticated browser context and therefore inherits browser privileges. Keep database credentials and authentication secrets server-side and never embed them in client-side collection code.

## Source

Repository: SQ2MTG/vinted-fav
