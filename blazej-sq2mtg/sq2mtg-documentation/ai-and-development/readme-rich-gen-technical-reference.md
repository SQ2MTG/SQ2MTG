# README Rich Gen — Technical Reference

## Overview

A React/TypeScript application for creating rich Markdown and README content with Gemini-based generation.

## Core capabilities

The source implements:

* visual Markdown editing;
* source Markdown editing;
* rendered preview;
* AI generation;
* web-grounded generation;
* deeper reasoning mode;
* GitHub repository analysis;
* attached-file context;
* reusable custom templates;
* browser-local autosave.

## AI workflow

The application builds a final prompt from:

1. the user prompt;
2. analyzed GitHub repository metadata and content summary;
3. attached files.

Generation is delegated to Gemini service functions:

* `generateRichMarkdown()`
* `generateWithSearch()`
* `generateWithDeepThinking()`

## Repository analysis

A GitHub repository URL can be analyzed through `analyzeRepository()`. Repository metadata is appended to the generation context, including repository name, URL, language, stars, license, description and summarized file content.

## Local persistence

The UI stores editor state and preferences in browser `localStorage`, including:

* Markdown autosave;
* preview width;
* preview collapsed state;
* custom Markdown templates.

Autosave is debounced by approximately 750 ms.

## Technology

* React
* TypeScript
* Gemini API integration
* GitHub repository analysis
* browser LocalStorage

## Source

Repository: `SQ2MTG/README-Rich_Gen`
