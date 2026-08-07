# 🌐 HangMaster — API Specification

> **Version:** 1.0
>
> **Project:** HangMaster
>
> **Document:** 09_API_SPECIFICATION.md
>
> **Status:** Active
>
> **Purpose**
>
> This document defines the API contract between the HangMaster frontend and backend.
>
> Although HangMaster uses Supabase instead of a traditional REST API, the application should follow a consistent service-oriented architecture. Every frontend feature must communicate with Supabase through dedicated service modules rather than directly accessing the database from UI components.

---

# 🎯 Objectives

The API layer should provide:

- Consistent data access
- Secure communication
- Reusable services
- Type-safe responses
- Error handling
- Separation of concerns

UI components must **never** communicate directly with Supabase.

---

# 🏗 Architecture

```text
React Components
        │
        ▼
Custom Hooks
        │
        ▼
Service Layer
        │
        ▼
Supabase Client
        │
        ▼
Supabase Backend
        │
        ▼
PostgreSQL Database
```

---

# 📂 Service Structure

```text
src/

services/

authService.ts

profileService.ts

gameService.ts

statisticsService.ts

leaderboardService.ts

achievementService.ts

settingsService.ts

categoryService.ts

wordService.ts
```

Each service is responsible for one domain only.

---

# 🔐 Authentication Service

## Responsibilities

- Register
- Login
- Logout
- Forgot Password
- Get Current User
- Refresh Session

---

### register()

Purpose

Create a new account.

Input

```ts
{
  email: string;
  password: string;
  username: string;
}
```

Output

```ts
{
  user;
  session;
}
```

---

### login()

Purpose

Authenticate an existing player.

Input

```ts
{
  email: string;
  password: string;
}
```

Output

```ts
{
  session;
}
```

---

### logout()

Purpose

Destroy the current session.

Output

```ts
void
```

---

# 👤 Profile Service

Responsibilities

- Load profile
- Update profile
- Upload avatar

---

### getProfile()

Input

```ts
playerId
```

Returns

```ts
Profile
```

---

### updateProfile()

Input

```ts
Profile
```

Returns

Updated Profile

---

# 🎮 Game Service

Responsibilities

- Start game
- Save completed game
- Resume game
- Calculate results

---

### createGameSession()

Input

```ts
{
category
difficulty
word
}
```

Output

Game Session

---

### finishGame()

Input

```ts
{
score
remainingLives
remainingTime
result
}
```

Output

Saved Session

---

### getRecentGames()

Returns

Player history

---

# 📊 Statistics Service

Responsibilities

- Load statistics
- Update statistics

---

### getStatistics()

Returns

```ts
PlayerStatistics
```

---

### updateStatistics()

Automatically updates:

- Wins
- Losses
- Games Played
- Best Score
- Best Time

---

# 🏆 Leaderboard Service

Responsibilities

- Submit score
- Fetch leaderboard

---

### submitScore()

Input

```ts
{
score
difficulty
category
timeRemaining
}
```

Output

Leaderboard Entry

---

### getLeaderboard()

Supports filters

- Today
- Weekly
- Monthly
- All Time

Returns

Leaderboard list

---

# ⭐ Achievement Service

Responsibilities

- Load achievements
- Unlock achievements
- Track progress

---

### getAchievements()

Returns

Master achievement list

---

### getPlayerAchievements()

Returns

Unlocked achievements

---

### unlockAchievement()

Backend validates requirements before unlock.

---

# ⚙ Settings Service

Responsibilities

- Load settings
- Update settings

---

Supported Settings

- Theme
- Music Volume
- SFX Volume
- Preferred Difficulty
- Reduced Motion

---

# 📂 Category Service

Responsibilities

Load categories.

Returns

Animals

Food

Countries

Movies

Technology

Sports

Music

Random

---

# 📖 Word Service

Responsibilities

Retrieve playable words.

---

### getRandomWord()

Input

```ts
category

difficulty
```

Returns

Random word

---

### getWordCount()

Returns

Total available words

---

# 📦 Standard Response Format

Every service should return:

```ts
{
success: boolean

data: T | null

error: string | null
}
```

Example

```ts
{
success: true,

data: profile,

error: null
}
```

---

# ❌ Error Handling

Possible Errors

400

Bad Request

401

Unauthorized

403

Forbidden

404

Not Found

409

Conflict

500

Server Error

---

Example

```ts
{
success:false,

error:"Invalid email or password."
}
```

---

# 🔒 Authentication Rules

Public

- Login
- Register
- Forgot Password

Protected

- Profile
- Statistics
- Game Sessions
- Achievements
- Settings

Leaderboard

Public Read

Authenticated Write

---

# 🛡 Validation

Every request must validate:

- Required fields
- Data types
- Length limits
- Allowed values

Validation uses

Zod

---

# 📊 Pagination

Large datasets should support pagination.

Example

Leaderboard

20 records

per page

---

# 🔍 Filtering

Leaderboard

Difficulty

Category

Date

---

Games

Difficulty

Category

Result

---

# 🔄 Data Flow

```text
Player

↓

React Component

↓

Custom Hook

↓

Service

↓

Supabase

↓

Database

↓

Response

↓

Store

↓

UI Update
```

---

# 🚀 Performance

Services should:

- Cache reusable data when appropriate
- Minimize duplicate requests
- Avoid unnecessary queries
- Select only required columns

---

# 🧪 Testing

Every service should be tested for:

- Success
- Failure
- Unauthorized access
- Invalid input
- Empty results

---

# 📚 Related Documents

- 01_ROADMAP.md
- 02_PROJECT_RULES.md
- 03_GAME_DESIGN_DOCUMENT.md
- 04_TECH_STACK.md
- 05_UI_UX_GUIDELINES.md
- 06_DATABASE_DESIGN.md
- 07_SUPABASE_SETUP.md
- 08_COMPONENT_ARCHITECTURE.md
- 10_DEPLOYMENT_GUIDE.md
- 11_TESTING_CHECKLIST.md
- 12_CLAUDE_INSTRUCTIONS.md

---

# 🏁 Conclusion

The HangMaster API specification establishes a consistent, secure, and maintainable communication layer between the React frontend and Supabase backend.

By enforcing service-based access, standardized response formats, strong validation, and clear separation of concerns, the project remains scalable and easier to maintain as new gameplay systems and backend features are introduced.

**End of Document**

