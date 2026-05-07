---
title: "Child Game Maze Digging"
category: "AI Education"
subcategory: "Children Games"
source_section: "prompts/05-ai-education/children-games/child-game-maze-digging.md"
author: "Yao Jingang"
version: "V1.0-en"
status: "active"
tags: "AI Education, Children Games, Child, Game, Maze"
---
# Children's Mini Game: Maze Digging Game

## Introduction
After children come up with ideas, generate a playable single-file HTML5 mini game using AI.

## Prompt
```markdown
Final Version of Maze Digging Game Generation Prompt (RTF Summary)
## Role (Role): 
HTML5 Children's Game Development AI Assistant.

## Task (Task): 
Create a complete, playable, HTML5 maze digging game suitable for 6-year-old children. The game includes 5 levels of increasing difficulty, provides clear visual feedback and simple sound effects, ensuring low frustration and high fun.
```## Format (Format): 
Single HTML file, containing all HTML, CSS (prefer using Tailwind CSS classes) and JavaScript. The code must include comments for key logic.
Detailed Specifications:
1. Core Mechanism: * Player: Yellow circle, movable with arrow keys or WASD, can dig bricks. * Environment: 2D grid maze. Contains indestructible walls (1), diggable bricks (2), empty cells (0). * Collectibles: Stars (5) +10 points, Diamonds (6) +50 points. All must be collected to proceed. * Enemies: Green circles, move randomly (avoiding walls), can pass through collectibles. * Progress: Game over if player collides with enemies. Level win when all items are collected, with a short delay before next level. Win the game after completing 5 levels. * UI: Display current level, total score, remaining collectibles in this level. Show corresponding messages when game over/victory. Provide a "Restart Game" button (resets to level 1 and total score).
2. Visuals and Animation: * Style: Bright colors, child-friendly pixelated/cartoon style. * Colors: Background #0f0f1f, Walls #4a4a8a, Bricks #d2691e, Player #ffd700, Enemies #32cd32, Stars #ffeb3b, Diamonds #00bfff. * Shapes: Player/enemies as circles with eyes, stars as five-pointed stars, diamonds as rhombuses. * Animation: Smooth movement for player/enemies (interpolation), bricks disappear immediately. * Layout: Canvas centered, UI clearly displayed, overall responsive and aesthetically pleasing.
3. Sound (Tone.js): * Play different sound effects for level win, collecting stars, collecting diamonds, digging bricks, and game over. * Ensure audio context starts after the user's first interaction.4. Level Design (5 levels total, TILE_SIZE: 32): * Principles: All levels have clear paths, are solvable, and are low difficulty, suitable for children. * Enemy speed (enemyMoveCooldown - higher values mean slower): * Level 1: 45 * Level 2: 40 * Level 3: 31 (Math.max(15, 35 - 2*2)) * Level 4: 29 (Math.max(15, 35 - 3*2)) * Level 5: 27 (Math.max(15, 35 - 4*2)) * Map data (gameLevels array - 0: empty, 1: wall, 2: brick, 3: player, 4: enemy, 5: star, 6: diamond): * Level 1 (Level 1 - 15x9): javascript [ [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,3,2,5,2,2,2,2,2,2,2,6,2,2,1], [1,2,1,1,1,1,1,2,1,1,1,1,1,2,1], [1,2,2,2,2,2,2,4,2,2,2,2,2,5,1], [1,1,1,1,1,1,1,2,1,1,1,1,1,1,1], [1,5,2,2,2,2,2,2,2,2,2,2,2,6,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,2,1], [1,2,2,6,2,2,2,2,2,2,2,5,2,2,1], [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1] ] * Level 2 (Level 2 - 19x9): javascript [ [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,3,2,2,5,2,2,2,2,2,2,2,2,6,2,2,2,4,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2,1], [1,2,2,2,2,2,5,2,2,6,2,2,5,2,2,2,2,2,1], [1,1,1,1,1,2,1,1,1,1,1,1,1,2,1,1,1,1,1], [1,2,2,2,2,2,2,2,4,2,2,2,2,2,2,2,2,4,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,2,1], [1,6,2,2,2,5,2,2,2,2,2,2,2,6,2,2,2,2,1], [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1] ] * Level 3 (Level 3 - 21x9): javascript [ [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,3,2,2,5,2,2,4,2,2,2,1,2,2,2,6,2,2,4,2,1], [1,2,1,1,1,2,1,1,1,1,2,1,2,1,1,1,1,1,1,2,1], [1,2,2,2,2,2,2,2,2,5,2,2,2,2,6,2,2,2,2,2,1], [1,1,1,1,1,1,1,2,1,1,1,1,1,2,1,1,1,1,1,1,1], [1,2,2,6,2,2,2,2,2,2,2,4,2,2,2,5,2,2,2,2,1], [1,2,1,1,1,2,1,1,1,1,2,1,2,1,1,1,1,1,1,2,1], [1,5,2,2,2,2,4,2,2,2,2,1,2,2,2,2,2,6,2,2,1], [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1] ] * Level 4 (Level 4 - 23x9): javascript [ [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,3,2,2,2,5,2,2,4,2,2,2,6,2,2,2,4,2,2,5,2,2,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1], [1,1,1,2,1,1,1,5,1,1,1,4,1,1,1,6,1,1,1,2,1,1,1], [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,6,2,2,4,2,2,2,5,2,2,2,2,2,4,2,2,2,6,2,2,2,1], [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1] ] * Level 5 (Level 5 - 25x9): javascript [ [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,3,2,2,2,2,5,2,2,4,2,2,2,6,2,2,2,4,2,2,2,5,2,2,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1], [1,1,1,1,1,2,1,1,5,1,1,4,1,1,6,1,1,2,1,1,1,1,1,1,1], [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1], [1,2,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1], [1,6,2,2,2,4,2,2,2,5,2,2,2,2,2,4,2,2,2,6,2,2,2,2,1], [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1] ]