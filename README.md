# HangMaster

A pixel-art fantasy reimagining of Hangman — built with React 19, TypeScript, Tailwind CSS, and Supabase.

> Status: **Phase 1 — Project Foundation** (see `docs/01_ROADMAP.md`)

## Stack

- React 19 + Vite + TypeScript
- Tailwind CSS 4
- Zustand (state)
- React Router
- Framer Motion (animation)
- React Hook Form + Zod (forms/validation)
- Supabase (auth, database, storage)

## Getting Started

```bash
npm install
cp .env.example .env   # then fill in your Supabase project URL/anon key
npm run dev
```

## Scripts

| Command | Purpose |
|---|---|
| `npm run dev` | Start the Vite dev server |
| `npm run build` | Type-check and build for production |
| `npm run typecheck` | Type-check only, no emit |
| `npm run lint` | Run ESLint |
| `npm run preview` | Preview the production build locally |

## Project Structure

Feature-first architecture (see `docs/12_CLAUDE_INSTRUCTIONS.md`):

```text
src/
├── features/     # self-contained feature modules
├── components/   # shared/reusable UI components
├── hooks/        # reusable React hooks (useAuth, useGame, useTimer, ...)
├── services/     # all Supabase communication lives here
├── layouts/      # page layout wrappers
├── pages/        # route-level components (composition only, no business logic)
├── store/        # Zustand stores
├── utils/        # pure helper functions
├── types/        # shared TypeScript types
└── lib/          # third-party client setup (e.g. Supabase client)
```

## Documentation

See `docs/` for the full project documentation set, including the roadmap,
design document, architecture, database schema, and API specification.
Some documents are still being written — check each file before relying on it.

## Environment Variables

Copy `.env.example` to `.env` and fill in your own Supabase project values.
Never commit `.env` or the Supabase **Service Role Key**.
