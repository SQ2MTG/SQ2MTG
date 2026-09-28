# KanarekAPP — technical reference

## Repository and runtime

KanarekAPP is an Android-oriented AI Studio project. The repository README documents Android Studio as the development environment and supports running on an emulator or physical Android device.

## Configuration

The documented local setup requires a `.env` file containing `GEMINI_API_KEY`. The key is a secret and must not be committed.

The README also documents an Android Gradle signing configuration that is intended for local development. Production/release signing must use a proper private keystore and protected credentials.

## Current documentation boundary

The repository README is an AI Studio bootstrap README rather than a complete application specification. Exact package name, activities, permissions, Gemini request flow, model selection, UI architecture and release configuration require source inspection.
