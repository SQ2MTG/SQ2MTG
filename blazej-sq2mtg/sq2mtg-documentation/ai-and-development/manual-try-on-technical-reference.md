# Manual Try-On — technical reference

## Purpose

Manual Try-On is an AI Studio-derived TypeScript web application for an image-generation workflow.

## Local runtime

The repository README documents Node.js as the prerequisite:

```bash
npm install
npm run dev
```

The Gemini API key is supplied through `.env.local`.

## Application context

Earlier source documentation identifies an image-upload + prompt workflow using Gemini image generation, with a React/TypeScript/Vite frontend.

## Security and privacy

Uploaded images may contain personal or sensitive visual information. Treat them as untrusted user input and avoid logging or persisting them unnecessarily.

The Gemini API key must remain server-side/managed through the intended application configuration and must not be committed.

## Documentation boundary

Exact model identifier, image MIME/size constraints, request schema, persistence/retention behavior and deployment configuration require source verification.
