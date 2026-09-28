# NylonBase v2 — technical reference

## Architecture

NylonBase v2 is a private full-stack TypeScript/React application derived from a Google AI Studio template.

Documented stack:

* React 19
* React Router DOM 7
* TypeScript 5
* Vite 8
* Express 5
* Tailwind CSS 4
* Zustand
* Recharts
* Multer
* JOSE
* geoip-lite
* `@google/genai`
* ExcelJS
* Kysely
* PostgreSQL/PGLite

## Runtime

The documented development architecture runs Express on port 3000 with Vite middleware.

Documented API areas include:

* `/api/auth/*`
* `/api/health`
* `/uploads`
* `/avatars`

## Persistence and authentication

The project uses Kysely with PostgreSQL/PGLite and database migrations. Authentication uses Better Auth/JOSE with an HTTP-only `auth_token`.

## Image handling

Uploaded images receive UUID-based names. SHA-256 hashing is used for duplicate-image detection.

## Security findings

Password handling requires particular care: direct SHA-256 password storage is not appropriate for password authentication. Passwords should use a dedicated password-hashing scheme such as Argon2id or bcrypt with appropriate parameters.

Upload endpoints should enforce size/type validation and avoid unrestricted public access to uploaded content.

## Documentation boundary

Exact schema, route contracts, authorization rules and production deployment configuration should be revalidated against the current source before release.
