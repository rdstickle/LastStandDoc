# Last Stand: Defenders - Game Design Document

## Table of Contents
- [1. Game Overview](#1-game-overview)
  - [1.1 Game Concept](#11-game-concept)
  - [1.2 Genre & Platform](#12-genre--platform)
  - [1.3 Target Audience](#13-target-audience)
- [2. Gameplay Mechanics](#2-gameplay-mechanics)
  - [2.1 Core Gameplay Loop](#21-core-gameplay-loop)
  - [2.2 Build & Defend Mechanics](#22-build--defend-mechanics)
  - [2.3 Resource Management](#23-resource-management)
  - [2.4 Combat & Zombie AI](#24-combat--zombie-ai)
  - [2.5 Multiplayer Mechanics](#25-multiplayer-mechanics)
- [3. Progression & Reward Systems](#3-progression--reward-systems)
  - [3.1 Level Progression](#31-level-progression)
  - [3.2 Card Reward System](#32-card-reward-system)
  - [3.3 Daily & Streak Rewards](#33-daily--streak-rewards)
- [4. Story & Setting](#4-story--setting)
  - [4.1 World Background](#41-world-background)
  - [4.2 Locations](#42-locations)
  - [4.3 Zombie Types](#43-zombie-types)
- [5. Monetization Strategy](#5-monetization-strategy)
  - [5.1 Ad-Based Revenue](#51-ad-based-revenue)
  - [5.2 In-Game Purchases](#52-in-game-purchases)
  - [5.3 Premium Subscription](#53-premium-subscription)
- [6. User Interface & Experience](#6-user-interface--experience)
  - [6.1 HUD & Gameplay UI](#61-hud--gameplay-ui)
  - [6.2 Menus & Navigation](#62-menus--navigation)
- [7. Technical Specifications](#7-technical-specifications)
  - [7.1 Platforms](#71-platforms)
  - [7.2 Engine & Tools](#72-engine--tools)
- [8. Future Expansions](#8-future-expansions)

---

## 1. Game Overview

### 1.1 Game Concept
*Last Stand: Defenders* is a post-apocalyptic, strategic tower defense game where players defend fortified locations against waves of zombies. Players must gather resources, build defenses, and upgrade structures to survive escalating waves of enemies. In addition to a single-player campaign, *Last Stand: Defenders* includes a competitive multiplayer mode, allowing players to compete to build the most effective defense.

### 1.2 Genre & Platform
- **Genre:** Strategy / Tower Defense
- **Platform:** Mobile (iOS & Android)

### 1.3 Target Audience
- **Age Range:** 13+
- **Player Types:** Strategy and defense enthusiasts, casual and competitive mobile gamers

---

## 2. Gameplay Mechanics

### 2.1 Core Gameplay Loop
1. **Build Phase:** Players set up defenses, adjust resource gathering priorities, and prepare for the next wave.
2. **Wave Phase:** Zombies spawn and advance toward the player’s base, navigating obstacles and attacking barricades and towers.
3. **Reward Phase:** After each wave, players earn resources and have the option to draw cards for additional rewards.

### 2.2 Build & Defend Mechanics
- **Tower & Barricade Placement:** Players place barricades to funnel zombies into kill zones and towers to deal damage from range.
- **Upgrade System:** Towers and barricades can be upgraded to improve durability, damage, range, and effects (e.g., splash damage).
- **Obstacle Durability:** Zombies will climb over or destroy barricades, requiring players to repair or reinforce frequently.

### 2.3 Resource Management
- **Four Resources:** Wood, metal, electronics, and ammo, each with unique uses in building and upgrading defenses.
- **Resource Priority Sliders:** Players adjust sliders to control the percentage of each resource gathered between waves.

### 2.4 Combat & Zombie AI
- **Zombie Types:** Includes standard zombies and specialized types like tanks, screamers, and summoners, each with unique abilities and weaknesses.
- **Pathfinding:** Zombies dynamically adjust their paths based on barricade placement and will attempt to find or create paths to the player’s base.

### 2.5 Multiplayer Mechanics
- **Fixed Rounds Mode:** Players compete in a set number of rounds, scored based on zombie kills and defense health.
- **Sudden Death Mode:** Players survive as long as possible in an endurance-based competition.
- **Leaderboards:** Players earn ranking points, contributing to global and seasonal leaderboards with exclusive rewards.

---

## 3. Progression & Reward Systems

### 3.1 Level Progression
- **Unlockable Levels:** Players advance through locations like a suburban cul-de-sac, a shopping mall, and an abandoned warehouse, each with unique layouts and challenges.
- **Difficulty Scaling:** Levels grow progressively harder, introducing more zombies, stronger enemies, and additional spawn points.

### 3.2 Card Reward System
- **Card Draw Rewards:** At the end of each level, players draw a card to receive bonus resources or upgrades. Watching an ad or using Gems allows them to select a second card.
- **Card Types:** Includes resource packs, temporary boosts, and rare permanent upgrades for defenses.

### 3.3 Daily & Streak Rewards
- **Daily Login Rewards:** Both free and premium players receive daily bonuses, with premium players receiving additional currency and resource bonuses.
- **Streak Bonuses:** Players receive escalating rewards for consecutive logins, encouraging regular engagement.

---

## 4. Story & Setting

### 4.1 World Background
Set in a post-apocalyptic world where society has collapsed due to a zombie outbreak, players are survivors attempting to protect their last strongholds.

### 4.2 Locations
- **Suburban Cul-de-Sac:** A fortified two-story house surrounded by barricades and obstacles in a small neighborhood.
- **Shopping Mall:** A large, open structure with multi-level defenses and choke points.
- **Abandoned Warehouse:** High ceilings and narrow corridors force players to adapt to a unique defensive setup.

### 4.3 Zombie Types
- **Standard Zombie:** Slow but numerous, forming the backbone of the waves.
- **Tank Zombie:** Heavy health, slower, and capable of dealing high damage to barricades.
- **Screamer Zombie:** Emits an area of effect that temporarily disables nearby towers.
- **Summoner Zombie:** Spawns additional zombies and must be eliminated quickly to avoid overwhelming defenses.

---

## 5. Monetization Strategy

### 5.1 Ad-Based Revenue
- **Interstitial Ads:** Shown after completing a level or every 10 waves to generate revenue without breaking gameplay flow.
- **Reward Ads:** Optional ads that allow players to double their card draw rewards, obtain extra resources, or gain boosters.

### 5.2 In-Game Purchases
- **Currency Packs:** Players can buy Gems (premium currency) for exclusive upgrades, additional card draws, or resource packs.
- **Lottery System:** Players use Gems to spin for rare upgrades, with guaranteed rare items after a certain number of spins.

### 5.3 Premium Subscription
- **Premium Daily Rewards:** Premium players receive extra daily rewards, including additional currency, resource boosters, and exclusive upgrades.
- **Ad-Free Option:** Premium subscribers have the option to play ad-free, with the option to purchase a one-time ad removal upgrade.

---

## 6. User Interface & Experience

### 6.1 HUD & Gameplay UI
- **Resource Display:** Shows current amounts of wood, metal, electronics, and ammo, updating dynamically.
- **Wave Information:** Displays wave number, enemy types, and a countdown timer for Build and Wave phases.
- **Tower & Barricade Status:** Shows health and upgrade status for each defense structure.

### 6.2 Menus & Navigation
- **Main Menu:** Access to single-player, multiplayer, shop, daily rewards, and player profile.
- **Reward Screens:** Card draw interface, daily reward claims, and premium options are easily accessible from the main menu.

---

## 7. Technical Specifications

### 7.1 Platforms
- **Primary Platforms:** iOS and Android
- **Screen Orientation:** Portrait mode optimized for mobile gameplay

### 7.2 Engine & Tools
- **Game Engine:** Unity or Unreal Engine (depending on team preference and tool support for mobile)
- **Ad Integration SDKs:** Support for Google AdMob, Unity Ads, or other mobile ad services for revenue generation
- **Analytics:** Firebase Analytics for player engagement tracking and data-driven improvements

---

## 8. Future Expansions
- **Co-op Multiplayer Mode:** A potential future update to allow two players to defend a shared base together.
- **Additional Zombie Types:** Expansion packs could introduce new zombies with unique abilities, adding variety to gameplay.
- **Seasonal Events:** Limited-time events tied to holidays or major updates, offering exclusive rewards and unique challenges.
- **Endless Mode:** A new game mode where players can test their defenses against endless waves, with global leaderboard tracking for high scores.

---
