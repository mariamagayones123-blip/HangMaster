# 🎮 HangMaster — Game Design Document (GDD)

> **Version:** 1.0  
> **Project:** HangMaster  
> **Document:** 03_GAME_DESIGN_DOCUMENT.md  
> **Status:** Draft  
> **Last Updated:** August 2026

---

# 📖 Table of Contents

1. Executive Summary
2. Vision Statement
3. Game Overview
4. Target Audience
5. Platform
6. Theme & Art Direction
7. Story & World
8. Core Gameplay Loop
9. Core Design Pillars

---

# 🎯 1. Executive Summary

## Introduction

**HangMaster** is a modern reimagining of the classic Hangman word game, transformed into a polished **Pixel Fantasy Adventure** experience.

Instead of presenting a plain educational interface, HangMaster immerses players in a vibrant medieval-inspired world filled with colorful pixel environments, charming characters, rewarding progression systems, and engaging gameplay mechanics.

The project is designed not only as a fun and replayable word game but also as a **high-quality portfolio project** that demonstrates professional full-stack development skills using modern web technologies.

---

## Project Goals

HangMaster aims to deliver:

- Modern gameplay inspired by the classic Hangman formula
- Beautiful pixel-art visuals
- Smooth and responsive user experience
- Player progression and statistics
- Online authentication
- Cloud save support
- Competitive leaderboards
- Achievement system
- Responsive gameplay across desktop and mobile
- Scalable architecture powered by Supabase

---

## Unique Selling Points

Unlike traditional Hangman games, HangMaster includes:

- Pixel Fantasy Adventure theme
- RPG-inspired progression system
- Player levels and experience
- Achievements
- Online leaderboards
- Cloud save
- Daily challenges (future)
- Fantasy-inspired UI
- Beautiful pixel environments
- Responsive web design
- Modern frontend architecture

---

# 🌟 2. Vision Statement

The vision of HangMaster is to transform one of the world's oldest word games into a premium indie-quality web experience.

The game should feel less like an educational activity and more like a complete adventure game where players continually improve, unlock achievements, compete with others, and enjoy satisfying progression.

Every interaction should feel rewarding through:

- Smooth animations
- Pixel-perfect visuals
- Meaningful progression
- Responsive controls
- Relaxing fantasy atmosphere

Players should always feel encouraged to play "just one more game."

---

# 🎮 3. Game Overview

## Genre

- Word Puzzle
- Casual
- Strategy
- Educational
- Adventure

---

## Gameplay Type

Single Player

Future Expansion

- Multiplayer Challenges
- Daily Competitions

---

## Camera

2D

Static Interface

---

## Perspective

Front-facing UI

Pixel Art Presentation

---

## Session Length

Quick Session

5–10 minutes

Long Session

15–30 minutes

Perfect for casual gaming.

---

# 👥 4. Target Audience

HangMaster is designed for players of all ages.

Primary audience:

- Students
- Casual gamers
- Puzzle lovers
- Word game enthusiasts

Secondary audience:

- Recruiters
- Software engineers
- Portfolio reviewers
- UI/UX designers

Because this project is also a portfolio application, the code quality and user experience are just as important as the gameplay.

---

# 💻 5. Platform

Supported platforms:

- Desktop
- Laptop
- Tablet
- Mobile Browser

Deployment

Frontend

- Vercel

Backend

- Supabase

The game is entirely web-based and requires no installation.

---

# 🎨 6. Theme & Art Direction

## Official Theme

Pixel Fantasy Adventure

---

## Visual Inspiration

The game's visual identity is inspired by modern pixel-art games that combine nostalgia with polished interfaces.

Inspirations include:

- Stardew Valley
- Celeste
- Pokémon
- CrossCode
- Eastward
- Octopath Traveler

The objective is not to copy these games but to adopt their attention to detail, vibrant color palettes, and polished presentation.

---

## Artistic Style

The game combines:

- Pixel Art
- Medieval Fantasy
- Cozy Adventure
- RPG-inspired interface
- Bright environments
- Modern UI principles

---

## Visual Mood

HangMaster should feel:

- Warm
- Friendly
- Relaxing
- Colorful
- Adventurous
- Rewarding

The interface should avoid looking overly dark or intimidating.

---

## Environment Themes

The game world includes multiple fantasy-inspired locations such as:

- Forest
- Castle
- Village
- Library
- Dungeon
- Floating Island

Each environment reinforces the feeling of progressing through a fantasy adventure.

---

## Color Philosophy

The color palette is based on the official UI design.

Primary colors include:

- Royal Blue
- Gold
- Wooden Brown
- Emerald Green
- Crimson Red
- Purple
- Orange

Each color communicates gameplay information while maintaining visual consistency.

---

# 📜 7. Story & World

## Background

In the Kingdom of Lexoria, ancient magical words hold the power to protect the realm.

Over time, many of these words have been forgotten, causing magical barriers around the kingdom to weaken.

As the newest apprentice known as the **HangMaster**, the player embarks on a journey to recover these forgotten words.

Each correctly guessed word restores fragments of the kingdom's lost knowledge and strengthens its magical defenses.

---

## Player Role

The player becomes the HangMaster, a young adventurer tasked with solving magical word puzzles.

Through each successful challenge, the player gains experience, earns rewards, and climbs the ranks of the kingdom's greatest word guardians.

---

## World Progression

Although the initial release focuses on gameplay, the world is designed to expand over time.

Future updates may introduce:

- New kingdoms
- Seasonal events
- Story chapters
- Character interactions
- Special quests

---


# 🔄 8. Core Gameplay Loop

The gameplay loop is intentionally simple yet rewarding.

```text
Open Game
      │
      ▼
Login / Continue as Guest
      │
      ▼
Choose Difficulty
      │
      ▼
Choose Category
      │
      ▼
Start Match
      │
      ▼
Guess Letters
      │
      ▼
Correct?
      │
 ┌───────────────┐
 │               │
 ▼               ▼
Yes              No
 │               │
Reveal Letter    Lose Life
 │               │
 └──────┬────────┘
        ▼
Word Completed?
        │
   ┌────┴────┐
   ▼         ▼
Yes         No
 │           │
Win        Continue
 │
 ▼
Gain XP
Coins
Achievements
Leaderboard Update
 │
 ▼
Play Again
```

The loop is designed to encourage replayability through progression and rewards.

---

# 🏛 9. Core Design Pillars

Every feature in HangMaster must support at least one of these pillars.

---

## 1. Fun First

Gameplay should always be enjoyable before adding complexity.

Simple mechanics with polished execution are preferred over unnecessary features.

---

## 2. Reward Progress

Players should constantly feel rewarded.

Rewards include:

- Experience
- Levels
- Coins
- Achievements
- Statistics
- Leaderboard ranking

Every completed game should contribute toward long-term progression.

---

## 3. Easy to Learn

New players should understand the game within minutes.

The interface should remain intuitive, with clear instructions and helpful feedback.

---

## 4. Beautiful Pixel Experience

Every screen should reflect the official Pixel Fantasy Adventure theme.

Consistency in colors, typography, icons, animations, and artwork is essential.

---

## 5. Accessibility

HangMaster should be playable by as many people as possible.

Accessibility goals include:

- Keyboard navigation
- High contrast support
- Reduced motion options
- Responsive layouts
- Clear visual feedback

---

## 6. Production-Ready Quality

HangMaster is built as a professional portfolio project.

Every feature should meet production standards in terms of:

- Code quality
- User experience
- Performance
- Scalability
- Maintainability

---

# ✅ End of Part 1

The next section of this Game Design Document will cover:

- Authentication System
- Screen Flow
- Home Screen
- Gameplay Screen
- Game Mechanics
- Difficulty Levels
- Categories
- Hint System
- Lives System
- Hangman Drawing
- Timer System
- On-screen Keyboard
- Win & Lose Conditions

# 🎮 10. Authentication System

## Overview

HangMaster supports both authenticated players and guest players.

Authentication allows players to securely save their progress, statistics, achievements, and leaderboard rankings using Supabase Authentication.

Players who do not wish to create an account may continue as a Guest, but their progress will only be stored locally.

---

## Authentication Goals

The authentication system should:

- Be simple and fast
- Require minimal setup
- Secure player accounts
- Enable cloud save
- Synchronize player statistics
- Support future social logins

---

## Authentication Methods

### Register

Players create a new account using:

- Username
- Email Address
- Password
- Confirm Password

Validation includes:

- Required fields
- Valid email format
- Minimum password length
- Password confirmation

---

### Login

Returning players log in using:

- Email
- Password

Optional:

- Remember Me

---

### Guest Mode

Players may immediately start playing without creating an account.

Guest Mode includes:

- Gameplay
- Statistics stored locally
- Local achievements
- Local settings

Guest Mode limitations:

- No online leaderboard
- No cloud save
- No account synchronization

---

### Forgot Password

Players can request a password reset using their email.

Supabase Authentication manages the recovery process.

---

### Logout

Logging out should:

- End the session
- Return to the Welcome Screen
- Preserve cloud data

---

# 🖥 11. Screen Flow

The UI follows a simple navigation flow designed to minimize player confusion.

```text
Splash Screen
        │
        ▼
Welcome Screen
        │
 ┌──────┴────────┐
 │               │
 ▼               ▼
Login       Register
 │               │
 └──────┬────────┘
        ▼
Home Screen
        │
 ├───────────────┐
 ▼               ▼
Start Game    Profile
 │               │
 ▼               ▼
Gameplay     Statistics
 │
 ▼
Victory / Defeat
 │
 ▼
Results Screen
 │
 ▼
Play Again
```

Navigation should always feel predictable and intuitive.

---

# 🏠 12. Home Screen

## Purpose

The Home Screen acts as the player's central hub.

It provides quick access to every major feature.

---

## Sections

### Header

Displays

- Player Avatar
- Username
- Level
- XP Progress Bar

---

### Currency

Displays

- Coins
- Gems

Future versions may use Gems for cosmetic rewards.

---

### Main Menu

Primary actions include:

- Start Game
- Continue
- Instructions
- Leaderboard
- Profile
- Settings
- Logout

---

### Background

The Home Screen uses the official fantasy castle environment.

Subtle environmental animations include:

- Moving clouds
- Floating particles
- Light shimmer

The background should remain calm and never distract from navigation.

---

# 🎮 13. Gameplay Screen

The Gameplay Screen is the heart of HangMaster.

Everything should be immediately visible without clutter.

---

## Main Layout

Top Area

- Category
- Difficulty
- Score
- Timer

Center

- Hidden Word
- Hangman Drawing

Bottom

- Pixel Keyboard

Side Panel

- Hearts
- Hint Button
- Pause Button

---

## Gameplay Information

Players should always know:

- Remaining lives
- Remaining time
- Current score
- Difficulty
- Category

---

## Responsive Design

Desktop

- Full layout

Tablet

- Condensed spacing

Mobile

- Vertical stacking
- Larger touch targets

---

# 🎲 14. Categories

Categories provide replayability by grouping words into themes.

---

## Launch Categories

🐾 Animals

Examples

- Tiger
- Elephant
- Rabbit

---

🍔 Food

Examples

- Pizza
- Burger
- Sushi

---

🌍 Countries

Examples

- Japan
- Canada
- Brazil

---

🎬 Movies

Examples

- Frozen
- Avatar
- Moana

---

💻 Technology

Examples

- Keyboard
- Internet
- Browser

---

⚽ Sports

Examples

- Football
- Tennis
- Boxing

---

🎵 Music

Examples

- Guitar
- Piano
- Violin

---

🎲 Random

Randomly selects words from every category.

---

Future updates may introduce:

- Fantasy
- Science
- Space
- History
- Programming
- Geography

---

# ⚔ 15. Difficulty System

Difficulty changes both challenge and rewards.

---

## Easy

Time

Unlimited or 180 seconds

Characteristics

- Short words
- More common vocabulary
- Beginner friendly

Reward Multiplier

1x

---

## Medium

Time

120 seconds

Characteristics

- Medium-length words
- Moderate vocabulary

Reward Multiplier

1.5x

---

## Hard

Time

60 seconds

Characteristics

- Longer words
- Less common vocabulary

Reward Multiplier

2x

---

## Expert

Time

30 seconds

Characteristics

- Long words
- Rare vocabulary
- Fast gameplay

Reward Multiplier

3x

---

# ❤️ 16. Lives System

Players begin each game with seven lives.

Each incorrect letter removes one life.

Represented visually using pixel-art hearts.

Example

❤️ ❤️ ❤️ ❤️ ❤️ ❤️ ❤️

Incorrect Guess

❤️ ❤️ ❤️ ❤️ ❤️ 🖤 🖤

---

## Life Loss Animation

When a wrong letter is selected:

- Heart briefly shakes
- Heart breaks
- Fade animation
- Small particle effect

The animation should provide satisfying feedback without slowing gameplay.

---

# 🪢 17. Hangman Drawing

Each incorrect guess draws another part of the hangman.

Seven stages are used.

Stage 0

Empty Gallows

↓

Stage 1

Head

↓

Stage 2

Body

↓

Stage 3

Left Arm

↓

Stage 4

Right Arm

↓

Stage 5

Left Leg

↓

Stage 6

Right Leg

↓

Stage 7

Complete Hangman

Game Over

Each stage should animate smoothly rather than appearing instantly.

---

# 💡 18. Hint System

Hints assist players while reducing their final score.

Players may use hints strategically.

---

## Available Hints

Reveal Letter

Randomly reveals one hidden letter.

---

Reveal Vowel

Reveals one unrevealed vowel.

---

Future Features

- Eliminate Wrong Letters
- Skip Word
- Double XP Hint
- Freeze Timer

---

## Hint Penalty

Each hint decreases the final score.

Example

Reveal Letter

-50 points

Reveal Vowel

-75 points

Future power-ups may remove penalties.

---

# 🏆 19. Win & Lose Conditions

## Win

The player wins when every letter has been correctly revealed before:

- Lives reach zero
- Timer expires

Rewards include:

- XP
- Coins
- Score
- Statistics update
- Achievement progress

---

## Lose

Players lose if:

- Lives reach zero
- Timer reaches zero

After losing:

- Correct word is revealed
- Final score shown
- Statistics updated
- Retry option displayed

---

# ⏱ 20. Timer System

The timer adds urgency and excitement.

---

## Timer States

Safe

Green

More than 50% remaining

---

Warning

Yellow

Less than 50%

---

Danger

Orange

Last 20 seconds

---

Critical

Red

Last 10 seconds

The timer pulses and flashes during the final countdown.

---

## Pause

Players may pause the game.

Pause Menu includes:

- Resume
- Restart
- Return to Home

Timer automatically stops while paused.

---

## Timeout

When the timer reaches zero:

- Timer animation completes
- Word is revealed
- Game Over screen appears
- Statistics update
- Player may retry

---

# ⌨ 21. Keyboard System

The on-screen keyboard supports both desktop and mobile players.

---

## Input Methods

- Mouse
- Touch
- Physical Keyboard

---

## Key States

Normal

Gray

Hover

Blue Glow

Correct

Green

Wrong

Red

Disabled

Dark Gray

---

Selecting a disabled key has no effect.

Correct letters animate with a satisfying pop effect.

Incorrect letters briefly shake before becoming disabled.

---

# ✅ End of Part 2

The next section of the Game Design Document will cover:

- Player Profile
- Experience (XP)
- Level System
- Statistics
- Coins & Gems
- Achievements
- Leaderboards
- Save System
- Daily Challenges
- Player Progression


# 👤 22. Player Profile System

## Overview

The Player Profile represents the player's identity and long-term progression within HangMaster.

Profiles provide players with a sense of ownership, achievement, and motivation to continue playing.

Profiles are stored in Supabase for authenticated users and Local Storage for guest users.

---

## Profile Information

Each profile contains:

- Avatar
- Username
- Email
- Level
- XP
- Coins
- Gems
- Games Played
- Wins
- Losses
- Win Rate
- Best Score
- Best Time
- Favorite Category
- Achievements

---

## Avatar System

Launch avatars include:

- Hero
- Knight
- Wizard
- Witch

Future updates may add:

- Seasonal avatars
- Unlockable characters
- Cosmetic customization

---

# ⭐ 23. Experience (XP) System

## Purpose

The XP system rewards player activity and provides a sense of progression.

Players gain XP after every completed game.

---

## XP Sources

Winning a game:

+100 XP

Correct guess:

+10 XP

Perfect game:

+50 XP

Expert difficulty:

+75 XP bonus

Daily challenge:

+150 XP

Achievement unlock:

+100 XP

---

## XP Formula

```text
Total XP =
Base XP
+ Difficulty Bonus
+ Time Bonus
+ Perfect Bonus
+ Achievement Bonus
```

---

# 🏅 24. Level System

Levels visually represent player progression.

Higher levels indicate greater experience.

---

## Example Levels

Level 1

Word Apprentice

---

Level 5

Letter Guardian

---

Level 10

Puzzle Knight

---

Level 20

Word Wizard

---

Level 50

HangMaster

---

## Level Formula

Example:

```text
Required XP = Level × 100
```

Examples:

Level 1

100 XP

Level 2

200 XP

Level 10

1000 XP

Level 20

2000 XP

---

# 📊 25. Statistics System

Statistics allow players to track performance.

---

## Statistics Collected

Games Played

Wins

Losses

Win Rate

Longest Streak

Current Streak

Best Score

Best Time

Hints Used

Favorite Category

Favorite Difficulty

Words Solved

Total Play Time

---

## Win Rate Formula

```text
Win Rate =
(Wins ÷ Games Played) × 100
```

Example:

80 wins

100 games

Win Rate = 80%

---

# 🪙 26. Currency System

HangMaster includes two currencies.

---

## Coins

Coins are earned through gameplay.

Uses:

- Future cosmetics
- Themes
- Avatars
- Decorations

---

## Gems

Premium currency.

Future use:

- Seasonal content
- Exclusive rewards

Launch version:

Visual only.

---

## Coin Rewards

Easy

25 coins

Medium

50 coins

Hard

75 coins

Expert

100 coins

---

Perfect Game

+25 bonus coins

---

# 🏆 27. Achievement System

Achievements reward player milestones.

Achievements encourage replayability.

---

## Achievement Categories

Gameplay

Skill

Progression

Speed

Collection

Events

---

## Examples

### Beginner

First Win

Win one game.

Reward:

50 XP

---

### Word Explorer

Play 25 games.

Reward:

100 XP

---

### Perfect Player

Win without mistakes.

Reward:

150 XP

---

### Speed Runner

Win in less than 30 seconds.

Reward:

200 XP

---

### Expert Champion

Win 10 Expert games.

Reward:

500 XP

---

### HangMaster

Reach Level 50.

Reward:

Exclusive Badge

---

# 🏅 28. Achievement UI

Achievements include:

- Icon
- Name
- Description
- Progress Bar
- Reward
- Unlock Date

Locked achievements appear darkened.

Unlocked achievements animate when earned.

---

# 🏆 29. Leaderboard System

The leaderboard allows players to compare performance.

---

## Local Leaderboard

Stored in Local Storage.

Includes:

- Name
- Score
- Difficulty
- Time
- Date

---

## Online Leaderboard

Stored in Supabase.

Includes:

- Username
- Score
- Difficulty
- Time Remaining
- Category
- Date

---

## Leaderboard Filters

Today

Weekly

Monthly

All Time

Friends (Future)

---

# 🥇 Ranking System

Ranks provide status.

Examples:

Bronze

Silver

Gold

Platinum

Diamond

Master

HangMaster

---

# 💾 30. Save System

HangMaster supports:

- Local Save
- Cloud Save

---

## Local Save

Stored in browser storage.

Saved:

- Settings
- Statistics
- High Scores
- Achievements
- Current Session

---

## Cloud Save

Stored in Supabase.

Saved:

- Player Profile
- XP
- Level
- Statistics
- Achievements
- Leaderboard Scores

---

# 🔄 Synchronization

When players log in:

Cloud data becomes the primary source.

Guest players may optionally import local progress.

---

# 📅 31. Daily Challenge System

Future feature.

Every player receives the same word each day.

Rules:

- One attempt
- Separate leaderboard
- Bonus rewards

Rewards:

XP

Coins

Achievements

Special badges

---

# 🎁 32. Reward Philosophy

Every play session should feel rewarding.

Players should gain:

- XP
- Coins
- Progress
- Statistics
- Achievements

Even after losing, players should feel motivated to continue.

---

# 🎯 33. Player Motivation

HangMaster uses multiple motivational systems:

Short-Term Motivation

- Win games
- Solve words

Medium-Term Motivation

- Earn XP
- Gain levels
- Unlock achievements

Long-Term Motivation

- Reach leaderboard
- Complete collections
- Become HangMaster

---

# 🌟 34. Replayability

Replayability is supported through:

- Categories
- Difficulty levels
- Achievements
- Leaderboards
- Daily challenges
- Statistics
- Future events

---

# 🔒 35. Anti-Cheat Considerations

Future online systems should validate:

- Score
- Time
- Difficulty
- Statistics

Validation should occur through Supabase functions when online features become more competitive.

---

# 📈 36. Progression Summary

Player Journey:

```text
Create Account
      │
      ▼
Play Games
      │
      ▼
Earn XP
      │
      ▼
Gain Levels
      │
      ▼
Unlock Achievements
      │
      ▼
Earn Coins
      │
      ▼
Improve Statistics
      │
      ▼
Climb Leaderboards
      │
      ▼
Become HangMaster
```

---

# ✅ End of Part 3

The next section of the Game Design Document will cover:

- UI Design System
- Official Colors
- Typography
- Wooden Panels
- Pixel Buttons
- Characters
- Backgrounds
- Art Direction
- Audio Design
- Animation Design
- Visual Effects


# 🎨 37. User Interface (UI) Design

## Overview

The HangMaster user interface combines classic pixel-art aesthetics with modern usability principles.

Every screen should be visually consistent, easy to navigate, responsive, and enjoyable to interact with.

The interface should immediately communicate that HangMaster is more than a traditional Hangman game—it is a polished Pixel Fantasy Adventure.

---

# 🎯 UI Design Goals

The UI should always be:

- Clean
- Consistent
- Responsive
- Accessible
- Easy to understand
- Visually rewarding
- Pixel-perfect

The player should never feel overwhelmed by unnecessary information.

---

# 🏰 Design Theme

Official Theme

**Pixel Fantasy Adventure**

The visual identity combines:

- Medieval Fantasy
- Cozy Adventure
- Pixel RPG
- Modern Web UI
- Colorful Environments

The UI should feel like a charming indie game rather than a school project.

---

# 🎨 Official Color Palette

## Primary Colors

### Royal Blue

Purpose

- Main background
- Navigation
- Primary buttons

Hex

```text
#3B82F6
```

---

### Gold

Purpose

- Borders
- Titles
- Rewards
- Highlights

Hex

```text
#FBBF24
```

---

### Wooden Brown

Purpose

- Panels
- Frames
- Dialogs

Hex

```text
#8B5A2B
```

---

## Success

Emerald Green

Purpose

- Correct answers
- Success messages
- Victory

```text
#22C55E
```

---

## Warning

Orange

Purpose

- Medium difficulty
- Warnings

```text
#F97316
```

---

## Danger

Red

Purpose

- Wrong guesses
- Game Over
- Errors

```text
#EF4444
```

---

## Expert

Purple

Purpose

- Expert Mode
- Magic
- Premium Features

```text
#8B5CF6
```

---

# 🔤 Typography

## Headings

Recommended Fonts

- Press Start 2P
- Pixelify Sans

Usage

- Screen Titles
- Buttons
- Important Labels

---

## Body Text

Recommended Fonts

- Tiny5
- VT323

Usage

- Descriptions
- Statistics
- Dialogs

Body text should prioritize readability while preserving the pixel aesthetic.

---

# 🪟 UI Components

## Wooden Panels

Panels are the primary containers used throughout the interface.

Used for:

- Profile Cards
- Settings
- Statistics
- Instructions
- Dialogs
- Popups

Characteristics

- Wooden texture
- Pixel borders
- Rounded pixel corners
- Gold outline

---

## Buttons

Buttons are one of the most frequently used components.

Every button includes:

- Hover animation
- Press animation
- Pixel border
- Shadow
- Icon (when appropriate)

---

## Primary Button

Color

Blue

Usage

- Play
- Login
- Continue

---

## Success Button

Color

Green

Usage

- Confirm
- Save
- Resume

---

## Danger Button

Color

Red

Usage

- Logout
- Delete
- Exit

---

## Secondary Button

Color

Brown

Usage

- Back
- Cancel

---

# ❤️ Hearts

Player lives are displayed using pixel-art hearts.

Example

❤️ ❤️ ❤️ ❤️ ❤️ ❤️ ❤️

Lost hearts

🖤 🖤

Animations

- Shake
- Break
- Fade

---

# ⌨ Keyboard Design

The on-screen keyboard follows the fantasy pixel style.

States

Normal

Hover

Pressed

Correct

Wrong

Disabled

Animations

- Press
- Pop
- Shake

---

# 🎴 Difficulty Cards

Each difficulty has its own color.

Easy

Green

Medium

Orange

Hard

Red

Expert

Purple

Each card displays:

- Name
- Time Limit
- Reward Multiplier
- Description

---

# 🏷 Category Cards

Categories use colorful icons.

Examples

🐾 Animals

🍔 Food

🌍 Countries

🎬 Movies

⚽ Sports

💻 Technology

🎵 Music

🎲 Random

Every category includes:

- Pixel icon
- Color
- Title

---

# 👤 Profile Card

Displays

- Avatar
- Username
- Level
- XP Bar
- Coins
- Gems

Future versions may include:

- Equipped Avatar
- Title
- Seasonal Badge

---

# 🏆 Achievement Cards

Every achievement includes:

- Icon
- Name
- Description
- Reward
- Progress
- Unlock Date

Locked achievements appear faded.

Unlocked achievements animate with:

- Glow
- Shine
- Scale

---

# 🏅 Leaderboard Cards

Display

- Rank
- Avatar
- Username
- Score
- Difficulty
- Time Remaining

Top three players receive unique decorations.

🥇 Gold

🥈 Silver

🥉 Bronze

---

# 🌄 Background Design

Backgrounds represent different fantasy locations.

Launch backgrounds

🏰 Castle

🌲 Forest

🏘 Village

📚 Library

🏰 Dungeon

Future

☁ Floating Island

🏔 Snow Kingdom

🌋 Volcano

🌌 Sky Realm

Each background includes subtle ambient animation.

---

# 🧙 Characters

Launch Characters

🧝 Hero

🧙 Wizard

⚔ Knight

🧙‍♀️ Witch

Each character reinforces the fantasy atmosphere.

Future updates may introduce unlockable avatars.

---

# 🎨 Icon Style

Icons follow the pixel-art style.

Examples

🏠 Home

👤 Profile

⚙ Settings

🏆 Leaderboard

❤️ Lives

💡 Hint

⏱ Timer

🎵 Music

🔊 Sound

Icons should remain simple and readable at small sizes.

---

# ✨ Visual Feedback

Every player action should provide immediate feedback.

Correct Guess

- Green flash
- Pop animation
- Sparkle particles

Wrong Guess

- Red flash
- Shake
- Heart break animation

Victory

- Confetti
- Fireworks
- Coin animation
- XP animation

Game Over

- Camera shake
- Dark overlay
- Fade animation

---

# 🎬 Animation Principles

Animations should feel:

- Responsive
- Smooth
- Lightweight

Animations must improve usability rather than distract from gameplay.

Recommended duration

150–300 ms for UI interactions.

---

# 🔊 Audio Design

## Background Music

Menu

Relaxing fantasy village theme.

Gameplay

Light orchestral pixel music.

Victory

Celebration fanfare.

Game Over

Gentle defeat melody.

---

## Sound Effects

Button Click

Soft wooden click.

Correct Guess

Coin pickup sound.

Wrong Guess

Wood impact.

Hint

Magic sparkle.

Timer Warning

Ticking clock.

Victory

Fanfare.

Game Over

Low fantasy tone.

---

# 🌟 Accessibility

Support

- Keyboard navigation
- Focus indicators
- Reduced motion
- High contrast
- Screen reader labels

Avoid relying solely on color to communicate gameplay states.

---

# 📱 Responsive Design

Desktop

Full layout.

Tablet

Compact spacing.

Mobile

Vertical layout with larger touch targets.

Every screen should remain usable regardless of device size.

---

# 🎯 UI Design Principles

Every screen should follow these principles:

- Consistency
- Simplicity
- Immediate feedback
- Clear hierarchy
- Pixel-perfect presentation
- Accessibility
- Performance

The UI should always reinforce the Pixel Fantasy Adventure identity established by the official HangMaster design.

---

# ✅ End of Part 4

The next and final section of the Game Design Document will cover:

- Technical Design
- Backend Architecture
- Supabase Integration
- Database Overview
- Save System
- Performance Goals
- Accessibility Standards
- Future Expansions
- Success Metrics
- Definition of Done
- Appendix


# 🏗 38. Technical Design

## Overview

HangMaster is designed as a modern web application built with a scalable frontend architecture and a cloud-powered backend.

The project emphasizes maintainability, performance, responsiveness, and long-term scalability.

---

## Frontend Architecture

Framework

- React 19

Build Tool

- Vite

Programming Language

- TypeScript

Routing

- React Router

Styling

- Tailwind CSS

Animation

- Framer Motion

State Management

- Zustand

Forms

- React Hook Form

Validation

- Zod

Icons

- Lucide React

---

## Backend Architecture

Backend Platform

Supabase

Services

- PostgreSQL Database
- Authentication
- Storage
- Row Level Security (RLS)
- Realtime (Future)
- Edge Functions (Future)

Deployment

Frontend

Vercel

Backend

Supabase Cloud

---

# 🗄 39. Database Overview

## Purpose

The database stores player accounts, game progress, achievements, leaderboards, and cloud saves.

---

## Core Tables

### profiles

Stores player information.

Fields

- id
- username
- avatar
- level
- xp
- coins
- gems
- created_at
- updated_at

---

### game_statistics

Stores player performance.

Fields

- games_played
- wins
- losses
- best_score
- best_time
- total_play_time

---

### achievements

Stores unlocked achievements.

Fields

- achievement_id
- player_id
- unlocked_at

---

### leaderboard

Stores leaderboard records.

Fields

- player
- score
- difficulty
- category
- remaining_time
- date

---

### settings

Stores user preferences.

Examples

- Theme
- Music Volume
- Sound Volume
- Preferred Difficulty

---

# 🔐 40. Security Design

Security is handled through Supabase Authentication and Row Level Security (RLS).

Rules

- Every player only accesses their own data.
- Leaderboard entries are read-only for other users.
- Sensitive keys are never exposed to the client.
- Service role keys remain server-side.

Authentication methods include:

- Email & Password
- Guest Mode

Future support:

- Google Login
- GitHub Login

---

# 💾 41. Data Persistence

## Guest Players

Data is stored in Local Storage.

Saved items include:

- High Scores
- Statistics
- Settings
- Current Progress

---

## Registered Players

Data is synchronized with Supabase.

Stored items include:

- Profile
- XP
- Coins
- Achievements
- Statistics
- Leaderboard Entries
- Settings

---

# ⚡ 42. Performance Goals

The application should provide a fast and responsive experience.

Goals include:

- Fast page loading
- Optimized assets
- Code splitting
- Lazy loading where appropriate
- Efficient state updates
- Minimal unnecessary re-renders

Target loading time:

Less than 3 seconds on a standard broadband connection.

---

# 📱 43. Responsive Design Goals

HangMaster must provide a consistent experience across devices.

Supported devices:

- Desktop
- Laptop
- Tablet
- Mobile

Responsive layouts should maintain usability without sacrificing visual quality.

---

# ♿ 44. Accessibility Standards

The game should be accessible to as many players as possible.

Accessibility features include:

- Keyboard navigation
- Focus indicators
- Screen reader labels
- High-contrast support
- Reduced motion support
- Large touch targets for mobile

Accessibility should be considered during development rather than added later.

---

# 🧪 45. Testing Strategy

Each feature should be tested before being considered complete.

Testing includes:

## Functional Testing

- Authentication
- Gameplay
- Timer
- Score
- Leaderboard
- Save System

---

## UI Testing

- Buttons
- Navigation
- Dialogs
- Forms
- Responsive layouts

---

## Cross-Browser Testing

Supported browsers:

- Chrome
- Edge
- Firefox
- Safari

---

## Device Testing

- Desktop
- Tablet
- Mobile

---

## Performance Testing

Verify:

- Fast rendering
- Smooth animations
- Low memory usage

---

# 🚀 46. Deployment Strategy

## Development

Local machine

↓

GitHub

↓

Automatic Vercel Preview Deployment

↓

Testing

↓

Production Deployment

---

## Production Environment

Frontend

Vercel

Backend

Supabase

Version Control

GitHub

Environment variables should be securely managed through Vercel and Supabase dashboards.

---

# 🔮 47. Future Expansion

The project is designed with scalability in mind.

Potential future features include:

- Daily Challenges
- Seasonal Events
- Multiplayer (Turn-Based)
- Avatar Customization
- Cosmetic Shop
- Custom Word Packs
- Localization
- Community Events
- Admin Dashboard
- Analytics Dashboard

These features are intentionally excluded from the initial release to maintain a focused development scope.

---

# 📊 48. Success Metrics

The project will be considered successful when it meets the following goals:

## Technical Goals

- Stable architecture
- Responsive UI
- Clean codebase
- Type-safe implementation
- Successful deployment

---

## Gameplay Goals

- Fun and engaging gameplay
- Balanced difficulty
- Clear progression
- High replayability

---

## Portfolio Goals

- Demonstrates modern frontend development
- Demonstrates backend integration
- Showcases UI/UX design skills
- Highlights software architecture and engineering practices

---

# ✅ 49. Definition of Done

HangMaster is considered complete when:

- All planned gameplay features are implemented.
- Authentication is fully functional.
- Cloud save works correctly.
- Statistics and achievements are tracked.
- Leaderboards operate as intended.
- Responsive design is verified.
- Accessibility standards are met.
- Performance goals are achieved.
- Documentation is complete.
- Production deployment is successful.

---

# 📚 50. Appendix

## Project Documents

The following documentation forms the complete project reference.

- 01_ROADMAP.md
- 02_PROJECT_RULES.md
- 03_GAME_DESIGN_DOCUMENT.md
- 04_TECH_STACK.md
- 05_UI_UX_GUIDELINES.md
- 06_DATABASE_DESIGN.md
- 07_SUPABASE_SETUP.md
- 08_COMPONENT_ARCHITECTURE.md
- 09_API_SPECIFICATION.md
- 10_DEPLOYMENT_GUIDE.md
- 11_TESTING_CHECKLIST.md
- 12_CLAUDE_INSTRUCTIONS.md
- README.md

These documents should be kept synchronized throughout development.

---

# 🏁 Closing Statement

HangMaster is more than a word puzzle game—it is a professional full-stack portfolio project that demonstrates modern software engineering, UI/UX design, and cloud application development.

Every design decision, gameplay mechanic, and technical implementation should support the project's vision of delivering a polished, accessible, and enjoyable Pixel Fantasy Adventure experience.

The primary goal is to create a maintainable, scalable, and production-ready application that reflects industry best practices while providing players with a memorable gaming experience.

---

**End of Document**

