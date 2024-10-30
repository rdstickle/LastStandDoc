# Last Stand: Defenders - Architecture Overview

## Table of Contents
- [1. Introduction](#1-introduction)
- [2. Game Overview](#2-game-overview)
- [3. Core Systems](#3-core-systems)
  - [3.1 Game Loop](#31-game-loop)
  - [3.2 Level System](#32-level-system)
  - [3.3 Resource & Upgrade System](#33-resource--upgrade-system)
  - [3.4 Zombie AI & Pathfinding](#34-zombie-ai--pathfinding)
  - [3.5 Defense & Tower System](#35-defense--tower-system)
  - [3.6 Multiplayer System](#36-multiplayer-system)
  - [3.7 Monetization System](#37-monetization-system)
- [4. UI & UX](#4-ui--ux)
- [5. Data Persistence](#5-data-persistence)
- [6. Future Development & Scaling](#6-future-development--scaling)

---

## 1. Introduction
*Last Stand: Defenders* is a mobile strategy defense game set in a post-apocalyptic world where players build, upgrade, and maintain defenses against waves of zombies. Key mechanics include resource management, upgrading defensive structures, and strategic placement of barricades and towers. The game also features a competitive multiplayer mode and a dual currency system.

---

## 2. Game Overview
- **Genre:** Strategy / Tower Defense
- **Platform:** Mobile (iOS & Android)
- **Core Gameplay:** Players defend a base in various locations by placing and upgrading defenses to survive increasingly difficult waves of zombies. Resources are gathered and used to build structures and towers, with an optional premium system for faster progression.
- **Multiplayer Mode:** Asynchronous competition, where players attempt to build the best defense and score higher than opponents.

---

## 3. Core Systems

### 3.1 Game Loop
- **Main Phases:** 
  - **Build Phase:** Players place barricades, towers, and obstacles with available resources.
  - **Wave Phase:** Zombies spawn and follow paths based on player’s barricade placement.
  - **Reward Phase:** After each wave, players receive resources and choose from a reward card.
- **Progression Logic:** Difficulty ramps up every wave, introducing more zombie types and spawn points.

### 3.2 Level System
- **Level Design:** 
  - Each level represents a distinct location (e.g., suburban cul-de-sac, shopping mall).
  - Levels consist of 40 waves, with mini-bosses every 10 waves and a main boss on the 40th wave.
- **Environment Layouts:** Levels feature specific layouts that dictate zombie spawn points and areas where barricades can be placed.

### 3.3 Resource & Upgrade System
- **Resource Types:** 
  - **Wood** for barricade fortifications
  - **Metal** for building structures
  - **Electronics** for tower upgrades
  - **Ammo** for refilling towers in Normal/Hard modes
- **Upgrade Tiers:** 
  - Temporary upgrades (wave-based) and rare permanent upgrades.
  - Premium upgrades for specific towers or resource generation, purchased with in-game currency.
- **Resource Priority System:** Players adjust sliders to prioritize resources gathered between waves.

### 3.4 Zombie AI & Pathfinding
- **AI Types:**
  - **Standard Zombies:** Basic AI, slower and with predictable pathing.
  - **Special Zombies:** Zombies with unique abilities (e.g., tanky zombies, summoners) to create more dynamic challenges.
- **Pathfinding:** Zombies calculate paths based on player-placed barricades, choosing to go around or climb over obstacles based on player’s maze design.
- **Spawn Logic:** Spawning escalates by wave, adding new spawn points and varying zombie types based on player progression.

### 3.5 Defense & Tower System
- **Tower Types:**
  - **Basic Towers:** General-purpose towers for early defense.
  - **Sniper Towers:** Long-range, high-damage towers for strong zombie types.
  - **Support Towers:** Provides support (e.g., slows zombies, boosts nearby tower damage).
- **Obstacle Types:**
  - **Barricades:** Basic barriers made from wood and metal, can be upgraded.
  - **Traps:** One-time-use items for crowd control or temporary zombie deterrence.
- **Tower Upgrades:** Each tower has specific upgrade paths (e.g., increased fire rate, damage boost, splash effects).

### 3.6 Multiplayer System
- **Multiplayer Modes:**
  - **Fixed Rounds:** Players compete over a set number of waves; the winner is determined by zombie kill count and damage taken.
  - **Sudden Death:** Endless waves until one player’s base is breached.
- **Matchmaking:** Based on player progression and performance; players are matched against others with similar levels and skills.
- **Leaderboard & Ranking:** Players earn ranking points for winning matches, with seasonal rewards.

### 3.7 Monetization System
- **In-Game Ads:**
  - Ads shown after certain levels or waves, with optional ads for extra rewards.
- **Two-Tier Currency System:**
  - **Basic Coins:** Earned through gameplay, used for general upgrades.
  - **Gems (Premium Currency):** Used for premium upgrades, purchased with real money or occasionally earned.
- **Premium Daily Rewards:** Premium players receive a bonus daily reward with extra currency and resources.
- **Lottery Card Draw:** Players choose one of six cards after each level; an optional ad view or premium currency can unlock a second card draw.

---

## 4. UI & UX
- **Main UI Components:**
  - **HUD:** Displays current resources, wave info, and timer for the build phase.
  - **Resource Priority Sliders:** Allows players to adjust gathering priorities for wood, metal, electronics, and ammo.
  - **Tower/Obstacle Placement UI:** Selection and placement system for building during the build phase.
- **Card Reward System UI:** Post-level screen with six face-down cards; player selects a card, with the option to watch an ad or use currency for a second draw.

---

## 5. Data Persistence
- **Progress Tracking:**
  - Player progression (completed waves, levels unlocked, upgrades) is stored locally and on the cloud for backup and syncing.
- **Resource Management:** Tracks current resources, premium currency, and active upgrades.
- **Leaderboard Data:** Multiplayer ranking, scores, and leaderboard positions are stored on a server.

---

## 6. Future Development & Scaling
- **Content Updates:** New levels, zombie types, and defenses to be introduced in seasonal updates.
- **Feature Expansion:** Additional premium content and advanced multiplayer features (e.g., co-op mode, event-based competitions).
- **Performance Optimization:** Regular testing on low-end devices to ensure smooth gameplay for a broad user base.

---

## Appendix
- **Glossary:** Terms for zombie types, tower functions, and resource definitions.
- **API Reference:** External API usage for leaderboard integration, data backup, and analytics.
- **Dependencies:** List of third-party libraries and frameworks used in the game (e.g., pathfinding library, ad integration SDK).
