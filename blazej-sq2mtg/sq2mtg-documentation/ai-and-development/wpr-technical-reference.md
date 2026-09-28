# WPR — technical reference

## Purpose

WPR is a TypeScript web application for AI-assisted virtual hosiery try-on.

The current README documents a migration from Google Gemini to the Hugging Face Inference API using Stable Diffusion Inpainting.

## Current documented workflow

1. Install Node.js dependencies with `npm install`.
2. Provide `HUGGING_FACE_API_KEY` through `.env.local`.
3. Start with `npm run dev`.
4. Open the development server on port 5173.

## Model and provider

The README identifies:

* model: `runwayml/stable-diffusion-inpainting`
* provider: Hugging Face Inference API
* task: image inpainting
* OpenRAIL licensing for the referenced model

The README also documents retry handling for HTTP 429 and an optional self-hosting path using ComfyUI.

## Application features

Documented inputs include a user photo, preset hosiery styles, colors and custom patterns/designs.

## Security and privacy

The Hugging Face API key is a secret and must remain outside source control. Uploaded photographs should be treated as sensitive user input and should not be retained or logged unnecessarily.

## Provenance

The project states that it is based on SQ2MTG/Manual-TryOn. Exact current request payloads, image preprocessing, provider URLs and self-hosted ComfyUI integration should be source-verified.
