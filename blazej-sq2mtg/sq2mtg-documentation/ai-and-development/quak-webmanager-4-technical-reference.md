# Quak WebManager 4 — technical reference

## Repository and runtime

Quak WebManager 4 is an AI Studio-derived TypeScript web application.

The repository README documents Node.js as the prerequisite and the standard workflow:

```bash
npm install
npm run dev
```

Gemini configuration is supplied through `.env.local` using `GEMINI_API_KEY`.

## Documentation boundary

The README is a generic AI Studio bootstrap document. Existing project notes identify a TypeScript/Gemini web application, but exact routes, data structures, UI modules, Gemini requests and deployment behavior require direct source verification.

API credentials must remain outside source control.
