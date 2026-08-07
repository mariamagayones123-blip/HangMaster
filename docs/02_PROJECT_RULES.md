# 📘 HangMaster — Project Rules & Engineering Standards

> **Version:** 1.0
>
> **Project:** HangMaster
>
> **Document:** 02_PROJECT_RULES.md
>
> **Purpose**
>
> This document defines the engineering standards, coding conventions, architecture, implementation workflow, and quality expectations for the HangMaster project.
>
> Every feature, component, page, and system must follow these rules to ensure the project remains consistent, maintainable, scalable, and production-ready.

---

# 🎯 Core Principles

Every implementation should be:

- Simple
- Modular
- Reusable
- Maintainable
- Scalable
- Type-safe
- Accessible
- Responsive
- Performant

Always prioritize **clarity over cleverness**.

---

# Development Philosophy

When making implementation decisions, follow this priority order:

1. Correctness
2. Maintainability
3. Readability
4. Reusability
5. Performance
6. Visual Polish

Never sacrifice long-term quality for short-term speed.

---

# Technology Stack

## Frontend

- React 19
- Vite
- TypeScript
- Tailwind CSS
- React Router
- Framer Motion
- Zustand
- React Hook Form
- Zod
- Lucide React

## Backend

- Supabase

### Services

- PostgreSQL
- Authentication
- Storage
- Row Level Security (RLS)

## Deployment

- Vercel
- GitHub

---

# Project Architecture

Use a **feature-first architecture**.

Separate responsibilities clearly.

Never place unrelated logic inside the same folder.

```
src/
│
├── assets/
├── components/
│   ├── ui/
│   ├── layout/
│   ├── game/
│   ├── auth/
│   ├── profile/
│   └── common/
│
├── features/
│   ├── auth/
│   ├── game/
│   ├── leaderboard/
│   ├── profile/
│   ├── achievements/
│   └── settings/
│
├── hooks/
├── layouts/
├── lib/
├── pages/
├── routes/
├── services/
├── store/
├── styles/
├── types/
├── utils/
│
└── main.tsx
```

---

# File Naming Convention

## Components

Use PascalCase.

Examples

```
Button.tsx

GameBoard.tsx

HangmanCanvas.tsx

Keyboard.tsx

PlayerProfile.tsx
```

---

## Hooks

```
useAuth.ts

useTimer.ts

useGame.ts

useKeyboard.ts
```

---

## Utilities

```
calculateScore.ts

shuffleWords.ts

formatTime.ts
```

---

## Constants

```
GAME_CONFIG.ts

DIFFICULTIES.ts

THEME.ts
```

---

## Types

```
game.ts

player.ts

leaderboard.ts
```

---

# Component Rules

Every component should:

- Have one responsibility
- Be reusable
- Be strongly typed
- Accept props
- Avoid hardcoded values
- Avoid duplicated logic

If a component becomes too large, split it into smaller components.

Target:

- 50–200 lines preferred
- Avoid exceeding 300 lines

---

# React Standards

Use:

- Functional Components
- Hooks
- Composition
- Custom Hooks

Avoid:

- Class Components
- Prop drilling
- Nested state
- Large monolithic components

---

# TypeScript Standards

Never use:

```ts
any
```

Prefer:

- interface
- type
- Readonly
- Record
- Partial
- Pick
- Omit

Everything must be typed.

Including:

- Props
- State
- API responses
- Function parameters
- Return values

---

# State Management

Use **Zustand**.

Global State:

- Authentication
- Theme
- Player
- Settings

Local State:

- Forms
- Dialogs
- Hover
- Temporary UI

Never place feature-specific state inside the global store.

---

# Styling Rules

Use Tailwind CSS only.

Avoid:

- Inline CSS
- Random spacing
- Hardcoded colors

Use design tokens whenever possible.

---

# Theme Rules

Support:

- Dark Mode
- Light Mode

Theme switching should be global.

Every component must work correctly in both themes.

---

# Pixel Art Guidelines

The visual style should remain consistent.

Design principles:

- Pixel-art inspired
- Fantasy adventure theme
- Modern UI
- Clean spacing
- Rounded pixel panels
- Consistent shadows
- Crisp typography

Never mix pixel-art UI with realistic assets.

---

# Animation Rules

Use Framer Motion.

Animations should be:

- Fast
- Smooth
- Purposeful

Avoid excessive movement.

Support users who prefer reduced motion.

---

# Accessibility Standards

Every interactive element must have:

- Keyboard support
- Focus indicator
- ARIA labels
- Semantic HTML

Never rely solely on color to communicate state.

Support:

- Screen readers
- Keyboard navigation
- High contrast

---

# Performance Rules

Optimize for speed.

Prefer:

- Lazy loading
- Code splitting
- Memoization when appropriate
- Image optimization

Avoid unnecessary renders.

---

# Services Layer

Never fetch data directly inside UI components.

Use dedicated service files.

Example

```
services/

auth.service.ts

game.service.ts

profile.service.ts

leaderboard.service.ts
```

---

# Business Logic

Keep business logic separate from UI.

Examples

Game logic

```
features/game/
```

UI

```
components/game/
```

Utilities

```
utils/
```

---

# Error Handling

Every async operation should support:

- Loading
- Success
- Error
- Retry

Never ignore exceptions.

Always provide user-friendly error messages.

---

# Forms

Use:

- React Hook Form
- Zod

Validation must never rely only on HTML attributes.

---

# Authentication Rules

Guest Mode must always be available.

Login unlocks:

- Cloud Save
- Statistics
- Achievements
- Leaderboards

Gameplay should never require an account.

---

# Database Rules

Use Supabase.

Requirements:

- Row Level Security (RLS)
- Secure policies
- No exposed service keys
- User data isolated by owner

---

# Git Workflow

Use feature branches.

Examples

```
feature/authentication

feature/game-engine

feature/timer

feature/leaderboard
```

Commit format

```
feat:

fix:

refactor:

style:

docs:

test:

chore:
```

Examples

```
feat: implement timer system

fix: resolve keyboard input bug

docs: update roadmap

refactor: simplify score calculation
```

---

# Pull Request Checklist

Before merging:

- Builds successfully
- No TypeScript errors
- No ESLint warnings
- Responsive
- Accessible
- Tested
- Matches design system
- No duplicated code

---

# Testing Standards

Every major feature should be tested.

Including:

- Game Engine
- Timer
- Keyboard
- Score Calculation
- Authentication
- Leaderboard
- Profile

---

# Documentation Standards

Whenever a major feature is added:

Update:

- ROADMAP.md (if scope changes)
- GAME_DESIGN_DOCUMENT.md (if gameplay changes)
- DATABASE_SCHEMA.md (if database changes)
- UI_UX_GUIDELINES.md (if UI changes)

Documentation should stay synchronized with the codebase.

---

# Security Guidelines

Never:

- Store secrets in the repository
- Commit `.env` files
- Expose API keys
- Trust client-side validation alone

Always validate sensitive operations on the backend.

---

# Claude AI Development Workflow

Before implementing any task, Claude must:

1. Read the user's request carefully.
2. Inspect the existing codebase before making changes.
3. Identify the files affected.
4. Explain the implementation plan.
5. Reuse existing components whenever possible.
6. Avoid duplicate logic.
7. Preserve project architecture.
8. Follow the design system.
9. Follow accessibility standards.
10. Stop after completing only the requested task.

Claude should never continue into unrelated work unless explicitly instructed.

If requirements are unclear or missing, Claude should ask clarifying questions instead of making assumptions.

---

# 📏 HangMaster — Project Rules

> **Version:** 1.0
>
> **Project:** HangMaster
>
> **Document:** 02_PROJECT_RULES.md
>
> **Status:** Active
>
> **Purpose**
>
> This document defines the engineering standards, coding conventions, architecture principles, and development workflow for HangMaster.
>
> Every implementation must follow these rules to ensure the project remains clean, maintainable, scalable, and production-ready.

---

# 🎯 Core Development Principles

Every feature should be:

- Simple
- Readable
- Reusable
- Modular
- Scalable
- Accessible
- Responsive
- Type-safe
- Performance-oriented

Always prioritize **maintainability** over clever code.

---

# 🏗 Architecture Principles

## Follow Feature-Based Architecture

Organize code by feature instead of placing everything in one folder.

Example

```text
src/
│
├── assets/
├── components/
├── features/
├── hooks/
├── layouts/
├── lib/
├── pages/
├── routes/
├── services/
├── store/
├── styles/
├── types/
└── utils/
```

---

## Separate Responsibilities

Keep responsibilities clear.

- UI components render the interface.
- Hooks manage reusable logic.
- Services communicate with Supabase.
- Stores manage application state.
- Utilities contain helper functions.

Never mix unrelated responsibilities in the same file.

---

# ⚛ React Standards

## Use Functional Components

Always use function components.

Preferred

```tsx
export function GameBoard() {}
```

Avoid class components.

---

## Keep Components Small

Each component should have one responsibility.

Good examples

- Button
- Keyboard
- Timer
- PlayerCard
- ScorePanel

Avoid components that try to do everything.

---

## Reuse Components

Before creating a new component:

- Search the project.
- Reuse existing components if possible.
- Extend existing components instead of duplicating them.

---

## Component Size

Recommended maximum

- 200–300 lines

If a component grows too large, split it into smaller pieces.

---

# 🟦 TypeScript Rules

## Never Use `any`

❌ Bad

```ts
const player: any
```

✅ Good

```ts
interface Player {}
```

or

```ts
type Player = {}
```

---

## Define Shared Types

Shared interfaces belong in

```text
src/types/
```

Do not duplicate interfaces across files.

---

## Enable Strict Typing

Use strict TypeScript settings.

Prefer explicit types where they improve readability.

---

# 🎨 UI Development Rules

Every UI must follow the official HangMaster design.

Theme

- Pixel Fantasy Adventure

Use

- Wooden panels
- Pixel buttons
- Pixel borders
- Gold highlights
- Fantasy backgrounds

Do not introduce a different visual style without updating the design guidelines.

---

## Responsive First

Every page must work on:

- Desktop
- Tablet
- Mobile

Design mobile responsiveness from the beginning.

---

## Accessibility

All interactive elements must include:

- Keyboard navigation
- Visible focus states
- Accessible labels
- Sufficient color contrast

Avoid relying only on color to communicate information.

---

# 🎮 Gameplay Rules

Game logic should be independent from UI.

Examples

Do not calculate score inside a component.

Instead

- Create a scoring utility.
- Call it from the game logic.
- Display the result in the UI.

This keeps gameplay logic reusable and testable.

---

# 🗂 Folder Organization

Keep folders organized.

Example

```text
features/

authentication/

game/

leaderboard/

profile/

settings/
```

Avoid dumping unrelated files into a single directory.

---

# 📁 File Naming Convention

Components

```text
PlayerCard.tsx
```

Hooks

```text
useTimer.ts
```

Utilities

```text
calculateScore.ts
```

Stores

```text
gameStore.ts
```

Types

```text
player.ts
```

Pages

```text
HomePage.tsx
```

Use **PascalCase** for components and pages, **camelCase** for hooks, utilities, and stores.

---

# 🧩 Component Conventions

Each component should:

- Have one responsibility.
- Receive data through props.
- Avoid unnecessary internal state.
- Be reusable.
- Be easy to test.

If multiple screens use the same UI element, create a shared component.

---

# 🗃 State Management

Use Zustand for global state.

Examples

- Player
- Authentication
- Game
- Settings
- Theme

Keep temporary UI state inside components when it doesn't need to be shared.

---

# 🌐 Supabase Rules

Supabase handles:

- Authentication
- Database
- Storage
- Leaderboards
- Player Profiles
- Statistics
- Achievements

Do not access Supabase directly from UI components.

Use a service layer.

Example

```text
services/

authService.ts

profileService.ts

leaderboardService.ts
```

---

# 🔐 Security Rules

Never expose:

- Service role keys
- Database passwords
- Secrets

Only use public environment variables on the client.

Enable Row Level Security (RLS) for all player data.

---

# 🎨 Styling Rules

Use Tailwind CSS.

Avoid inline styles unless absolutely necessary.

Create reusable UI classes when patterns repeat.

Keep spacing and typography consistent with the design system.

---

# 🎞 Animation Rules

Use Framer Motion.

Animations should:

- Improve usability.
- Feel smooth.
- Be subtle.

Avoid excessive motion that distracts from gameplay.

Respect reduced-motion preferences where appropriate.

---

# 🎵 Audio Rules

Provide separate controls for:

- Background Music
- Sound Effects

Remember the user's preferences between sessions.

Do not autoplay loud sounds unexpectedly.

---

# 🧪 Testing Rules

Every feature should be manually tested before being considered complete.

Check:

- Gameplay
- Authentication
- Responsive layout
- Accessibility
- Performance
- Edge cases

Fix issues before moving to the next phase.

---

# 🚀 Git Workflow

Commit after completing a meaningful task.

Example

```text
feat: implement timer system

fix: correct score calculation

refactor: simplify keyboard component

docs: update game design document
```

Keep commit messages clear and descriptive.

---

# 📚 Documentation Rules

When a feature changes:

- Update the relevant documentation.
- Keep roadmap, design, and architecture documents synchronized.

Documentation is part of the project, not an afterthought.

---

# 🤖 AI Development Workflow

Before implementing a feature:

1. Read the relevant documentation.
2. Inspect the existing codebase.
3. Identify reusable components.
4. Reuse existing logic whenever possible.
5. Implement only the requested scope.
6. Verify the implementation.
7. Summarize completed work.

Do not make unrelated changes.

---

# ✅ Definition of Done

A task is complete only when:

- Requirements are fully implemented.
- Code follows project conventions.
- No TypeScript errors remain.
- No linting errors remain.
- Responsive layout is verified.
- Accessibility is considered.
- Documentation is updated if needed.
- The feature is tested.
- The project builds successfully.

---

# ❌ Avoid

- Duplicate code
- Massive components
- Deeply nested logic
- Hardcoded values
- Unused files
- Unused dependencies
- `any` types
- Direct database calls from components
- Mixing UI and business logic

---

# 🏆 Development Philosophy

HangMaster should be built as if it were a commercial indie game.

Every feature should:

- Improve the player experience.
- Be maintainable.
- Be scalable.
- Match the official UI/UX.
- Follow the architecture.
- Be production-ready.

Quality is more important than speed.
