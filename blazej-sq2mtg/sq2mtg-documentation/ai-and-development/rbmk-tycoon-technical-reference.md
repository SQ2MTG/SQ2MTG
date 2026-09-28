# RBMK Tycoon — technical reference

## Repository and runtime

RBMK Tycoon is an AI Studio-derived web application. The repository README documents Node.js as the prerequisite.

## Local development

Documented workflow:

```bash
npm install
npm run dev
```

The application requires `GEMINI_API_KEY` in `.env.local`.

## Documentation boundary

The default README is a generic AI Studio deployment guide and does not document the game's mechanics or internal architecture. Exact gameplay systems, state persistence, UI structure, Gemini usage and deployment configuration require direct source inspection.

API keys must remain outside source control.
