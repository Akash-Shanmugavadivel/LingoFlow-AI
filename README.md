# LingoFlow AI

An AI-powered German conversation coach. Practice everyday scenarios, get contextual grammar and phrasing corrections, translate words or sentences, and review a generated session summary.

## Features

- Scenario-based German conversation practice
- Context-aware grammar and phrasing corrections with explanations
- Word and sentence translation tools
- End-of-session summaries with corrections, vocabulary, and practice suggestions

## Stack

- Next.js 15, React 18, and TypeScript
- Genkit with Google’s Gemini 2.5 Flash model
- Tailwind CSS and Radix-based UI components

## Requirements

- Node.js compatible with Next.js 15
- npm
- A Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey)

## Run locally

```bash
npm install
```

Set `GEMINI_API_KEY` in your environment before starting the app. For PowerShell:

```powershell
$env:GEMINI_API_KEY="your-api-key"
npm run dev
```

Open [http://localhost:9002](http://localhost:9002). Keep the API key server-side; do not prefix it with `NEXT_PUBLIC_` or commit it to the repository.

## Useful commands

```bash
npm run dev         # Start Next.js on port 9002
npm run genkit:dev  # Start the Genkit development flow inspector
npm run typecheck   # Check TypeScript types
npm run build       # Build the production app
npm run start       # Run the production build
```

The AI provider and model are configured in `src/ai/genkit.ts`; the server-side AI actions are in `src/lib/actions.ts`, with individual flows in `src/ai/flows/`.

## Project structure

- `src/app/` — landing page and conversation experience
- `src/components/lingoflow/` — chat, scenarios, word lookup, and summary UI
- `src/ai/flows/` — correction, translation, and session-summary flows
- `src/lib/actions.ts` — server actions that call the AI flows
- `docs/blueprint.md` — product feature and design blueprint

## Notes

This repository contains the application source. No screenshots or hosted demo link are currently documented here.