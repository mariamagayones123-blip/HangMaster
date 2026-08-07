# 🎨 HangMaster — UI/UX Guidelines

> **Version:** 1.0
>
> **Project:** HangMaster
>
> **Document:** 08_ARCHITECTURE.md
>
> **Status:** Active
>
> **Purpose**
>
> This document defines the official User Interface (UI) and User Experience (UX) guidelines for HangMaster.
>
> Every screen, component, animation, interaction, and visual asset must follow these standards to ensure a consistent, polished, and professional player experience.

---

# 🎯 Design Philosophy

HangMaster combines the nostalgic charm of classic pixel-art games with the usability and polish of modern web applications.

Every interface should feel:

- Fun
- Cozy
- Colorful
- Fantasy-inspired
- Responsive
- Easy to understand

The UI should instantly communicate that HangMaster is a premium indie game rather than a traditional Hangman application.

---

# 🎮 Official Theme

## Theme Name

**Pixel Fantasy Adventure**

Inspired by:

- Stardew Valley
- Pokémon
- Celeste
- Eastward
- CrossCode
- Octopath Traveler

---

# 🎨 Color System

## Primary Colors

### Royal Blue

Purpose

- Navigation
- Primary buttons
- Headers

```text
#3B82F6
```

---

### Gold

Purpose

- Borders
- Highlights
- Titles
- Rewards

```text
#FBBF24
```

---

### Wooden Brown

Purpose

- Panels
- Cards
- Frames
- Menus

```text
#8B5A2B
```

---

### Emerald Green

Purpose

- Correct Guess
- Success
- Confirm

```text
#22C55E
```

---

### Orange

Purpose

- Warning
- Medium Difficulty

```text
#F97316
```

---

### Crimson Red

Purpose

- Wrong Guess
- Game Over
- Errors

```text
#EF4444
```

---

### Purple

Purpose

- Expert Difficulty
- Premium Rewards
- Magic

```text
#8B5CF6
```

---

# 🌙 Theme Support

The application supports:

## Dark Theme (Default)

Dark fantasy atmosphere.

Recommended for gameplay.

---

## Light Theme

Bright fantasy appearance.

Ideal for accessibility and daytime use.

---

Both themes must preserve:

- Contrast
- Readability
- Pixel style

---

# 🔤 Typography

## Headings

Recommended Fonts

- Press Start 2P
- Pixelify Sans

Used for:

- Titles
- Buttons
- Dialog Headers
- Menu Labels

---

## Body Text

Recommended Fonts

- Tiny5
- VT323

Used for:

- Paragraphs
- Statistics
- Instructions
- Descriptions

---

# 📐 Layout Principles

Every screen follows a consistent layout hierarchy.

```text
Header

↓

Main Content

↓

Action Area

↓

Footer
```

Spacing should remain consistent across all pages.

---

# 📱 Responsive Design

Supported devices

- Desktop
- Laptop
- Tablet
- Mobile

---

## Desktop

- Full navigation
- Side panels
- Spacious layout

---

## Tablet

- Reduced spacing
- Collapsible menus

---

## Mobile

- Vertical layout
- Large touch targets
- Simplified navigation

---

# 🏠 Home Screen

Contains

- Player Profile
- XP Bar
- Coins
- Gems
- Main Menu
- Background Illustration

Primary Actions

- Start Game
- Continue
- Leaderboard
- Profile
- Instructions
- Settings

---

# 🔐 Authentication Screens

Includes

- Welcome
- Login
- Register
- Forgot Password

Design Goals

- Simple
- Friendly
- Minimal
- Fast

Buttons should remain large and touch-friendly.

---

# 🎮 Gameplay Screen

Must display:

Top Area

- Category
- Difficulty
- Timer
- Score

Center

- Hidden Word
- Hangman Drawing

Bottom

- Pixel Keyboard

Side Panel

- Lives
- Hint
- Pause

---

# ❤️ Lives Display

Represented using pixel hearts.

Example

❤️ ❤️ ❤️ ❤️ ❤️ ❤️ ❤️

Animation

- Shake
- Break
- Fade

---

# ⌨ Keyboard

Every key has six states.

Normal

Hover

Pressed

Correct

Wrong

Disabled

The keyboard should support:

- Mouse
- Touch
- Physical Keyboard

---

# 💡 Hint Button

Includes:

Magic icon

Tooltip

Remaining hints

Animations:

Glow

Scale

Sparkle

---

# ⏱ Timer

Display

MM:SS

or

Countdown

Colors

Green

↓

Yellow

↓

Orange

↓

Red

Final ten seconds

- Pulse
- Flash
- Countdown sound

---

# 🏆 Score Panel

Displays

- Current Score
- Best Score
- Multiplier

Animated when score increases.

---

# 👤 Profile Screen

Displays

- Avatar
- Username
- Level
- XP
- Statistics
- Achievements
- Favorite Category

---

# 🏅 Achievement Screen

Every achievement card includes:

- Icon
- Name
- Description
- Reward
- Progress Bar

Locked cards remain grayscale.

Unlocked cards animate.

---

# 🏆 Leaderboard

Display

Rank

Avatar

Username

Difficulty

Score

Time

Date

Top 3 players receive unique decorations.

---

# ⚙ Settings Screen

Contains

- Theme
- Music Volume
- Sound Volume
- Default Difficulty
- Reset Progress
- Logout

Every setting should include a clear label and description.

---

# 📖 Instructions Screen

Explains

- Gameplay Rules
- Difficulty
- Timer
- Lives
- Score
- Categories
- Hints
- Controls

Illustrations should accompany instructions where possible.

---

# 🪟 UI Components

Reusable components include:

- Buttons
- Cards
- Panels
- Inputs
- Dialogs
- Badges
- Progress Bars
- Tooltips
- Toast Notifications

All components must remain visually consistent.

---

# 🖱 Interaction Design

Every interaction should provide feedback.

Hover

Slight lift

Glow

Pressed

Scale down

Shadow reduction

Disabled

Lower opacity

No hover effect

---

# ✨ Animation Guidelines

Animations should be:

- Fast
- Smooth
- Purposeful

Avoid excessive movement.

---

## UI Animations

Buttons

Cards

Dialogs

Screen transitions

Notifications

---

## Gameplay Animations

Correct Guess

Wrong Guess

Heart Loss

Letter Reveal

Victory

Defeat

---

# 🎆 Particle Effects

Victory

- Confetti
- Sparkles
- Coins

Correct Guess

- Magic particles

Wrong Guess

- Dust particles

Particles should remain lightweight.

---

# 🔊 Audio UX

Provide separate controls for:

- Music
- Sound Effects

Default volume:

70%

Player preferences should be remembered.

---

# 🎯 Icon Guidelines

Use pixel-inspired icons whenever possible.

Primary icon style:

Lucide React customized to match the pixel theme.

Icons should remain:

- Consistent
- Recognizable
- Minimal

---

# 🖼 Background Guidelines

Launch backgrounds

- Castle
- Forest
- Village
- Library
- Dungeon

Backgrounds should remain subtle.

Avoid distracting gameplay.

---

# ♿ Accessibility

Every interactive element must include:

- Keyboard support
- Visible focus
- Accessible labels
- Sufficient contrast

Support reduced motion where possible.

---

# 🚀 Performance Guidelines

UI should remain responsive.

Goals:

- Smooth animations
- Fast rendering
- Optimized images
- Lazy-loaded assets

Avoid unnecessary re-renders.

---

# 📏 UI Consistency Rules

Every screen must:

- Use official colors
- Follow typography guidelines
- Use reusable components
- Maintain spacing consistency
- Follow responsive layouts
- Match the Pixel Fantasy Adventure theme

No screen should introduce new visual styles without updating this document.

---

# 🏁 Definition of Good UI

The HangMaster interface is considered successful when it is:

- Beautiful
- Consistent
- Responsive
- Accessible
- Intuitive
- Pixel-perfect
- Enjoyable to use

Every UI decision should enhance gameplay rather than distract from it.

---

# 📚 Related Documents

This document works alongside:

- 01_ROADMAP.md
- 02_PROJECT_RULES.md
- 03_GAME_DESIGN_DOCUMENT.md
- 04_TECH_STACK.md
- 06_DATABASE_DESIGN.md
- 07_SUPABASE_SETUP.md
- 08_COMPONENT_ARCHITECTURE.md
- 09_API_SPECIFICATION.md
- 10_DEPLOYMENT_GUIDE.md
- 11_TESTING_CHECKLIST.md
- 12_CLAUDE_INSTRUCTIONS.md

---

# 🎯 Closing Statement

The UI/UX of HangMaster should feel like a polished indie pixel-art game, combining nostalgic visuals with modern usability. Every screen, interaction, animation, and component should reinforce the Pixel Fantasy Adventure identity while remaining intuitive, accessible, and responsive across all supported devices.

**End of Document**

