# ☁️ HangMaster — Supabase Setup Guide

> **Version:** 1.0
>
> **Project:** HangMaster
>
> **Document:** 07_SUPABASE_SETUP.md
>
> **Status:** Active
>
> **Purpose**
>
> This document provides the official guide for setting up and configuring Supabase for the HangMaster project.
>
> It covers project creation, authentication, database configuration, security, storage, environment variables, and deployment integration.
>
> All backend development should follow this document.

---

# 🎯 Objectives

The Supabase backend will provide:

- User Authentication
- PostgreSQL Database
- Cloud Storage
- Row Level Security (RLS)
- Cloud Save
- Leaderboards
- Player Profiles
- Game Statistics
- Achievements

Future features:

- Realtime
- Edge Functions
- Daily Challenges
- Multiplayer Support

---

# 🏗 Backend Architecture

```text
                React 19 Frontend
                        │
                        ▼
                Supabase Client SDK
                        │
                        ▼
                ┌──────────────────┐
                │    Supabase      │
                ├──────────────────┤
                │ Authentication   │
                │ PostgreSQL       │
                │ Storage          │
                │ Row Level Security│
                │ Realtime (Future)│
                │ Edge Functions   │
                └──────────────────┘
```

---

# 📦 Create a Supabase Project

## Step 1

Go to:

https://supabase.com

---

## Step 2

Create a new project.

Project Name

```text
HangMaster
```

---

## Step 3

Choose:

- Organization
- Region (closest to your users)
- Strong database password

---

## Step 4

Wait for project initialization.

This usually takes a few minutes.

---

# 🔑 Project Credentials

After project creation, obtain:

- Project URL
- Anon Public Key

Never expose:

- Service Role Key

The Service Role Key must remain private.

---

# 📁 Environment Variables

Create a local environment file.

Example:

```env
VITE_SUPABASE_URL=https://your-project.supabase.co

VITE_SUPABASE_ANON_KEY=your-public-anon-key
```

---

## Environment Rules

Never commit:

- .env
- Secrets
- Service Keys

Commit:

- .env.example

---

# 📂 Recommended File Structure

```text
src/
│
├── lib/
│     └── supabase.ts
│
├── config/
│     └── env.ts
│
├── services/
│
├── types/
│
└── features/
```

---

# ⚙ Supabase Client

Create:

```text
src/lib/supabase.ts
```

Responsibilities:

- Initialize Supabase Client
- Export reusable instance
- Use environment variables

The client should be created only once.

---

# 🔐 Authentication

HangMaster uses Supabase Authentication.

Launch Methods

- Email
- Password

Future Methods

- Google
- GitHub
- Discord (Optional)

---

# 👤 Authentication Flow

```text
Register
    │
    ▼
Email Verification (Optional)
    │
    ▼
Login
    │
    ▼
Create Profile
    │
    ▼
Home Screen
```

---

# 🧾 User Registration

When a new account is created:

1. User signs up.
2. Supabase creates a record in `auth.users`.
3. Application creates a corresponding record in the `profiles` table.
4. Default statistics and settings records are created.

---

# 🔓 Login Flow

```text
Login

↓

Validate Credentials

↓

Create Session

↓

Load Profile

↓

Navigate to Home
```

---

# 🚪 Guest Mode

Guest players may play without an account.

Guest data is stored in Local Storage.

Cloud features require login.

---

# 🔒 Row Level Security (RLS)

Enable RLS on every application table.

Protected Tables

- profiles
- player_statistics
- player_settings
- player_preferences
- game_sessions
- leaderboard_entries
- player_achievements
- saved_games

---

# 🔑 RLS Rules

## Profiles

Player may:

- Read own profile
- Update own profile

---

## Statistics

Player may:

- Read own statistics
- Update own statistics

---

## Settings

Player may:

- Read own settings
- Update own settings

---

## Game Sessions

Player may:

- Insert own sessions
- Read own sessions

---

## Leaderboards

Everyone

- Read leaderboard

Authenticated Players

- Insert their own scores

No direct updates or deletes.

---

## Achievements

Master table

Read-only

---

## Player Achievements

Players

Read their own progress.

Backend validates unlock conditions.

---

# 🗂 Database Tables

```text
profiles

player_statistics

player_settings

player_preferences

achievements

player_achievements

game_sessions

leaderboard_entries

categories

words

daily_challenges

saved_games (optional)
```

---

# 🪣 Storage Buckets

## avatars

Stores player avatars.

Public.

---

## achievement-icons

Stores achievement artwork.

Public.

---

## game-assets

Future downloadable assets.

Public.

---

# 🔄 Data Flow

```text
Player Action

↓

React Component

↓

Service Layer

↓

Supabase Client

↓

Database

↓

Response

↓

UI Update
```

---

# 🛡 Security Best Practices

Always:

- Enable RLS
- Use UUID primary keys
- Validate user input
- Use parameterized queries
- Protect private routes
- Keep Service Role Key server-side

Never:

- Store secrets in frontend code
- Disable RLS in production
- Expose Service Role Key

---

# 📊 Cloud Save Strategy

Automatically synchronize:

- Player Profile
- XP
- Coins
- Statistics
- Achievements
- Settings
- Leaderboard Scores

Guest users continue using Local Storage until they register.

---

# 🚀 Deployment Integration

## Frontend

Hosted on:

Vercel

---

## Backend

Hosted on:

Supabase Cloud

---

## Production Environment Variables

Configure in Vercel:

```text
VITE_SUPABASE_URL

VITE_SUPABASE_ANON_KEY
```

Never add the Service Role Key to Vercel frontend environment variables.

---

# 🔮 Future Supabase Features

The architecture supports future enhancements:

- Google OAuth
- GitHub OAuth
- Discord OAuth
- Realtime Leaderboards
- Daily Challenge Automation
- Edge Functions
- Multiplayer
- Push Notifications
- Cloud Inventory

---

# 📋 Setup Checklist

## Supabase

- [ ] Create Supabase Project
- [ ] Configure Project Region
- [ ] Save Project URL
- [ ] Save Anon Key
- [ ] Create Environment Variables

---

## Authentication

- [ ] Enable Email Authentication
- [ ] Configure Password Rules
- [ ] Enable Email Verification (Optional)
- [ ] Disable Anonymous Authentication

---

## Database

- [ ] Create All Tables
- [ ] Configure Relationships
- [ ] Create Indexes
- [ ] Enable RLS
- [ ] Create Policies

---

## Storage

- [ ] Create avatars bucket
- [ ] Create achievement-icons bucket
- [ ] Configure Public Access

---

## Frontend

- [ ] Create Supabase Client
- [ ] Connect Authentication
- [ ] Test Database Connection

---

## Deployment

- [ ] Configure Vercel Environment Variables
- [ ] Test Production Build
- [ ] Verify Authentication
- [ ] Verify Cloud Save

---

# 📚 Related Documents

- 01_ROADMAP.md
- 02_PROJECT_RULES.md
- 03_GAME_DESIGN_DOCUMENT.md
- 04_TECH_STACK.md
- 05_UI_UX_GUIDELINES.md
- 06_DATABASE_DESIGN.md
- 08_COMPONENT_ARCHITECTURE.md
- 09_API_SPECIFICATION.md
- 10_DEPLOYMENT_GUIDE.md
- 11_TESTING_CHECKLIST.md
- 12_CLAUDE_INSTRUCTIONS.md

---

# 🏁 Conclusion

Supabase serves as the complete backend platform for HangMaster, providing authentication, database services, storage, and cloud synchronization through a secure PostgreSQL foundation.

By following this setup guide, the project will maintain a scalable, secure, and production-ready backend architecture that supports both the initial release and future feature expansion.

**End of Document**

