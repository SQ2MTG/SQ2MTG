# Vinted — application workspace

## Repository

`SQ2MTG/vinted` is a private JavaScript/TypeScript application workspace on the `main` branch. GitHub currently reports no declared repository license.

## Toolchain

The current package manifest documents React 19, TypeScript 5.7, Vite 8, TanStack Router/Start, Tailwind CSS 4, Zustand, Radix UI, Recharts, React Hook Form and Playwright. Server/runtime dependencies include Nitro, Kysely, PostgreSQL (`pg`) and PGlite.

## Development

The documented development command runs `scripts/with-app-env.mjs` and starts Vite on `0.0.0.0:8080`:

```bash
npm install
npm run dev
```

The repository also defines build, database migration, typecheck, authentication-invariant checks, tests, lint and formatting scripts.

## Data and authentication

The project uses Kysely with PostgreSQL support and PGlite as a local database option. Authentication-related dependencies include Better Auth and JOSE. The repository contains dedicated authentication invariant and application-data tests.

## Documentation boundary

This repository has no README in the current default branch. Therefore implementation details such as routes, database schema, authorization rules and business workflows should be documented from source inspection rather than inferred from package metadata.

## Security

Keep authentication secrets, database credentials and signing material outside source control. Treat session/authentication and user data as sensitive application state.

## Source

Repository: SQ2MTG/vinted
