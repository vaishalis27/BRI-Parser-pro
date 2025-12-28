# BRI-Parser-pro

Browser-based React + TypeScript project for parsing and displaying BRI content.

## Overview

`BRI-Parser-pro` is a small Vite + React + TypeScript application that demonstrates parsing BRI-formatted input in the browser and rendering results in a UI. The parsing logic lives in the `services` layer while UI pieces live under `components`.

## Features

- Client-side parsing of BRI content using `services/browserParser.ts`.
- Small, componentized React UI for rendering parsed output and code snippets.
- Built with Vite for fast local development.

## Tech stack

- Vite
- React
- TypeScript

## Quick start

1. Install dependencies

```bash
npm install
```

2. Run development server

```bash
npm run dev
```

3. Build for production

```bash
npm run build
```

4. Preview production build

```bash
npm run preview
```

If your `package.json` uses different script names, adjust the commands accordingly.

## Project structure (important files)

- `index.html` — Vite entry HTML.
- `index.tsx` — React bootstrap.
- `App.tsx` — Root application component.
- `metadata.json` — Project metadata / example data (if used by the app).
- `types.ts` — Shared TypeScript types.
- `vite.config.ts` — Vite configuration.
- `components/` — Reusable React components:
  - `PythonCodeSnippet.tsx` — Renders code snippets with formatting.
  - `ReadmeSection.tsx` — Generic readme/content section component.
- `services/` — Business logic / utilities:
  - `browserParser.ts` — BRI parsing logic executed in the browser.

## How it works (brief)

The UI collects BRI input from the user, passes it to `browserParser.ts` which returns a parsed representation (using types from `types.ts`), and the React components render the parsed output and any code snippets.

## Development notes

- Keep parsing logic inside `services` so it can be reused or tested independently.
- Components under `components` are designed to be small and focused; follow the existing patterns when adding new UI pieces.

## Contributing

1. Fork the repo and create a branch for your changes.
2. Open a pull request describing the change.

