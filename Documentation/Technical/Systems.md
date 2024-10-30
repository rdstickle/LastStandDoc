# Last Stand: Defenders - Systems Overview

## Table of Contents
- [1. Overview](#1-overview)
- [2. Game Loop System](#2-game-loop-system)
- [3. Level Management System](#3-level-management-system)
- [4. Resource & Economy System](#4-resource--economy-system)
- [5. AI & Pathfinding System](#5-ai--pathfinding-system)
- [6. Defense & Upgrade System](#6-defense--upgrade-system)
- [7. Multiplayer System](#7-multiplayer-system)
- [8. UI System](#8-ui-system)
- [9. Monetization System](#9-monetization-system)
- [10. Data Persistence & Syncing System](#10-data-persistence--syncing-system)

---

## 1. Overview
This document provides a comprehensive look at the systems that power *Last Stand: Defenders*, detailing each system’s components, interactions, and purpose within the game. Each section describes dependencies, cross-system interactions, and specific components required to support the core gameplay.

---

## 2. Game Loop System
### Purpose
Handles the main gameplay phases and transitions, ensuring smooth flow between build, wave, and reward phases.

### Components
- **Phase Manager:** Controls transitions between build phase, wave phase, and reward phase.
- **Timer Controller:** Tracks time remaining in each phase and displays countdowns.
- **Event Triggers:** Notifies other systems when phases change, prompting updates in UI, AI spawning, and resource allocation.

### Dependencies
- **Level Management System:** Receives wave data.
- **Resource & Economy System:** Calculates resource generation at the end of each wave.
- **UI System:** Updates HUD with phase changes and timers.

---

## 3. Level Management System
### Purpose
Manages level-specific configurations, including environment setup, wave data, and spawning logic.

### Components
- **Level Configurator:** Sets up environment objects (barricades, towers, spawn points) based on selected level.
- **Wave Generator:** Defines and spawns zombies per wave, scaling difficulty over time.
- **Boss Wave Controller:** Identifies mini-boss and main boss waves, adjusting wave data accordingly.

### Dependencies
- **Game Loop System:** Sends wave completion data to trigger new wave setups.
- **AI & Pathfinding System:** Relies on zombie pathing to determine routes.
- **Defense & Upgrade System:** Places initial defense structures.

---

## 4. Resource & Economy System
### Purpose
Tracks and manages resources, currency, and in-game economy, supporting resource gathering, premium transactions, and upgrades.

### Components
- **Resource Manager:** Stores player resources (wood, metal, electronics, ammo).
- **Priority System:** Players adjust sliders to control the rate of resource gathering between waves.
- **Upgrade Controller:** Applies temporary and permanent upgrades to defenses, towers, and player attributes.
- **Currency Manager:** Manages in-game currency (Basic Coins and Gems), tracking earned, purchased, and spent amounts.

### Dependencies
- **Defense & Upgrade System:** Provides resources for upgrades and fortifications.
- **UI System:** Updates resource counts, currency displays, and priority sliders.

---

## 5. AI & Pathfinding System
### Purpose
Controls enemy behaviors, zombie spawning, and pathfinding around player defenses to provide a challenging experience.

### Components
- **Zombie Spawner:** Spawns zombies based on wave data and player progression.
- **Pathfinding Controller:** Calculates optimal paths for zombies based on player-placed obstacles, adjusting dynamically as barricades are added or removed.
- **Zombie Behavior AI:** Determines different zombie actions, such as attacking obstacles, summoning other zombies, or navigating challenging paths.

### Dependencies
- **Level Management System:** Defines spawn points and zombie types per wave.
- **Defense & Upgrade System:** Registers interactions when zombies attack barricades or are damaged by towers.
- **UI System:** Displays zombie health and special abilities.

---

## 6. Defense & Upgrade System
### Purpose
Enables players to place, upgrade, and manage defenses such as barricades and towers. Tracks defense durability and upgrade effects.

### Components
- **Defense Placement System:** Allows players to place barricades, towers, and obstacles during the build phase.
- **Upgrade System:** Manages tower and barricade upgrades, enhancing defense stats or adding new abilities.
- **Damage Calculator:** Calculates damage taken by barricades and inflicted by towers on zombies.

### Dependencies
- **Resource & Economy System:** Deducts resources for new placements and upgrades.
- **AI & Pathfinding System:** Adjusts zombie paths in response to new or removed barricades.
- **UI System:** Updates tower and barricade stats, upgrade options, and health bars.

---

## 7. Multiplayer System
### Purpose
Facilitates competitive multiplayer matches, including player matching, score tracking, and leaderboard updates.

### Components
- **Matchmaking System:** Matches players based on progression and skill level.
- **Scoring System:** Tracks kills, barricade health, and resource efficiency to determine winners in Fixed Rounds mode.
- **Sudden Death Mode Controller:** Initiates and monitors waves until one player’s defenses are breached.
- **Leaderboard Manager:** Updates player standings and ranks in global or seasonal leaderboards.

### Dependencies
- **Data Persistence & Syncing System:** Saves and syncs multiplayer scores and ranks.
- **UI System:** Displays opponent stats, leaderboards, and match results.
- **Resource & Economy System:** Awards resources or currency for multiplayer wins.

---

## 8. UI System
### Purpose
Provides all on-screen displays, menus, HUD elements, and user interactions. Updates dynamically based on player actions and game states.

### Components
- **HUD Controller:** Displays resources, timers, wave info, and health of defenses and zombies.
- **Card Reward UI:** Manages the post-level card selection interface, allowing players to pick rewards and optionally watch an ad for a second draw.
- **Upgrade & Placement UI:** Allows players to select and place defenses, adjust resource priorities, and upgrade towers.
- **Main Menu & Settings:** Provides access to game options, settings, and navigation to different game modes.

### Dependencies
- **Game Loop System:** Receives triggers to update phases and timers.
- **Resource & Economy System:** Updates resource counts and currency displays.
- **Multiplayer System:** Displays scores, leaderboard data, and opponent information.

---

## 9. Monetization System
### Purpose
Integrates ads, microtransactions, and premium rewards to support monetization without compromising gameplay quality.

### Components
- **Ad Manager:** Handles interstitial ads, optional reward ads, and video ads for additional rewards.
- **Currency Store:** Provides in-app purchase options for premium currency (Gems) in different bundle sizes.
- **Premium Rewards System:** Tracks premium players’ daily rewards and provides extra currency and bonus items.
- **Lottery Card Draw System:** Implements the randomized card rewards for players at the end of levels.

### Dependencies
- **Data Persistence & Syncing System:** Saves player purchases, currency balances, and premium status.
- **UI System:** Displays ad options, currency packs, and reward information in the store interface.
- **Resource & Economy System:** Updates currency balances when purchases or rewards are made.

---

## 10. Data Persistence & Syncing System
### Purpose
Manages data storage and syncing for player progress, achievements, and multiplayer scores across devices.

### Components
- **Local Storage Manager:** Saves player progress, inventory, and unlocked items locally.
- **Cloud Sync Service:** Syncs player data to the cloud for backup and multi-device access.
- **Leaderboard & Ranking Sync:** Updates and retrieves leaderboard data from the server.
- **Analytics & Logging:** Tracks player behavior and logs errors for performance and gameplay improvements.

### Dependencies
- **Multiplayer System:** Syncs scores, ranks, and match results.
- **Monetization System:** Tracks purchases, ad views, and currency balances.
- **UI System:** Displays data such as player ranks, achievements, and progress on different screens.

---

## Appendix
- **API References:** Documentation for third-party services used (e.g., ads, cloud syncing, and analytics).
- **Configuration Files:** Locations of config files for tuning difficulty, wave patterns, and resource gathering rates.
- **Glossary:** Definitions of key terms and abbreviations for systems and gameplay features.
