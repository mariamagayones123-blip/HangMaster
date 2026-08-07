# 🗄 HangMaster — Database Design

> **Version:** 2.0
>
> **Project:** HangMaster
>
> **Document:** 06_DATABASE_DESIGN.md
>
> **Status:** Official Database Blueprint
>
> **Purpose**
>
> This document defines the complete database architecture for HangMaster.
>
> It serves as the single source of truth for the database schema, table relationships, naming conventions, constraints, indexes, security policies, and future scalability.
>
> Every backend feature must follow this document.

---

# 🎯 Database Goals

The HangMaster database is designed to be:

- Secure
- Normalized
- Scalable
- Maintainable
- Cloud-ready
- Performance optimized
- Compatible with Supabase

---

# ☁ Database Platform

Backend Platform

Supabase

Database Engine

PostgreSQL

Authentication

Supabase Auth

Security

Row Level Security (RLS)

Storage

Supabase Storage

---

# 📦 Database Overview

The database stores:

- Player Accounts
- Player Profiles
- Player Preferences
- Game Sessions
- Statistics
- Achievements
- Leaderboards
- Categories
- Words
- Daily Challenges
- Cloud Save
- Future Cosmetics

---

# 🏗 Database Schema

```text
                           auth.users
                                │
                                │
                                ▼
                           profiles
                                │
      ┌─────────────────────────┼─────────────────────────┐
      │                         │                         │
      ▼                         ▼                         ▼
 statistics                 settings            player_preferences
      │
      ├───────────────────────────────┐
      │                               │
      ▼                               ▼
game_sessions              player_achievements
      │                               │
      ▼                               ▼
leaderboard_entries          achievements
      │
      ▼
saved_games (optional)

categories
      │
      ▼
words
      │
      ▼
daily_challenges
```

---

# 📊 Entity Relationship Summary

| Parent | Child | Relationship |
|---------|--------|-------------|
| auth.users | profiles | One-to-One |
| profiles | statistics | One-to-One |
| profiles | settings | One-to-One |
| profiles | player_preferences | One-to-One |
| profiles | game_sessions | One-to-Many |
| profiles | leaderboard_entries | One-to-Many |
| profiles | player_achievements | One-to-Many |
| achievements | player_achievements | One-to-Many |
| categories | words | One-to-Many |
| words | daily_challenges | One-to-Many |

---

# 📂 Database Tables

The HangMaster database consists of the following tables.

| Table | Purpose |
|--------|----------|
| profiles | Player profile information |
| statistics | Lifetime statistics |
| settings | Game settings |
| player_preferences | Personal preferences |
| achievements | Master achievement list |
| player_achievements | Achievement progress |
| game_sessions | Completed games |
| leaderboard_entries | Leaderboard scores |
| categories | Word categories |
| words | Dictionary of playable words |
| daily_challenges | Daily challenge words |
| saved_games *(optional)* | Resume unfinished games |

---

# 📌 Naming Conventions

## Tables

Use snake_case.

Examples

profiles

game_sessions

leaderboard_entries

---

## Columns

Use snake_case.

Examples

created_at

remaining_time

games_played

---

## Primary Keys

Every table uses

id UUID

---

## Foreign Keys

Examples

player_id

category_id

achievement_id

word_id

---

# 🔗 Relationships

Then your document continues like this:
# 📦 Table: profiles

Purpose

Stores player profile information.

Columns

...

Constraints

...

Indexes

...

Relationships

...

RLS

...
Then
# 📦 Table: statistics
Then
# 📦 Table: settings
Then
# 📦 Table: player_preferences
Then
# 📦 Table: achievements
Then
# 📦 Table: player_achievements
Then
# 📦 Table: game_sessions
Then
# 📦 Table: leaderboard_entries
Then
# 📦 Table: categories
Then
# 📦 Table: words
Then
# 📦 Table: daily_challenges
Then
# 📦 Table: saved_games (Optional)


