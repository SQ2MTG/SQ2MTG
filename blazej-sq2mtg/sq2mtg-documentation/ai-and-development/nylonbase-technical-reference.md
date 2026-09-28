# NylonBase — technical reference

## Repository and runtime

NylonBase is a private TypeScript project derived from a Google AI Studio application template.

The repository README documents the standard AI Studio workflow:

```bash
npm install
npm run dev
```

and requires `GEMINI_API_KEY` in `.env.local`.

## Project identity

This repository is separate from NylonBase-v2. The two projects should not be treated as interchangeable implementations.

## Documentation boundary

The default README is only an AI Studio bootstrap guide. Application-specific architecture, routes, data model, Gemini integration, authentication, persistence and deployment behavior require source inspection.

The Gemini key must remain outside source control.
