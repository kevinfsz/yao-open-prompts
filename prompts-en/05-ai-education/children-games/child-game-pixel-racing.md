---
title: "Child Game Pixel Racing"
category: "AI Education"
subcategory: "Children Games"
source_section: "prompts/05-ai-education/children-games/child-game-pixel-racing.md"
author: "Yao Jingang"
version: "V1.0-en"
status: "active"
tags: "AI Education, Children Games, Child, Game, Pixel"
---
# Kids Mini Game: Pixel Racing Dodge Game

## Introduction
After children come up with ideas, use AI to generate a playable single-file HTML5 mini game.

## Prompt
```markdown
## Role (Role)
Experienced HTML5 game developer.

## Task (Task)

Create a single-file, pixel-style HTML5 top-down racing dodge game with the following features, ensuring the code is clear, playable, and has increasing difficulty.

## Format (Format)
1. Core Gameplay
The player controls a car to avoid obstacles coming from the opposite direction on a three-lane road. The game ends when the life runs out.
2. Controls
Keyboard: Left and right arrow keys to switch lanes.
Touch: Left and right virtual directional buttons (⬅️, ➡️) at the bottom of the screen to switch lanes.
3. Visuals and UI
Theme: Dark theme (e.g., background #1a202c, container #2d3748). UI elements use Tailwind CSS.
Canvas:
Default size 500x750px, responsive adjustment while maintaining aspect ratio.
Enable pixelated rendering (image-rendering: pixelated), base pixel unit pixelSize = 10.
Road: Central driving area (e.g., #718096), grass on both sides (e.g., #16a34a, about 12% of canvas width), white dashed lines moving downward in pixel style (opacity 0.4).
Player Car:
Pixel pattern (5x7 pixel units): [[0,1,1,1,0], [1,1,2,1,1], [1,1,1,1,1], [0,1,1,1,0], [0,1,1,1,0], [1,0,0,0,1], [1,1,0,1,1]] (0: empty, 1: main color #3b82f6, 2: secondary color #60a5fa).
Initially located in the center bottom of the canvas.
Obstacles:
At least 3 types of pixel style, appearing randomly from the top lane.
Cone: 4x4 pixel units, red/light red (#ef4444/#fca5a5), pattern: [[0,1,1,0],[1,2,2,1],[1,2,2,1],[1,1,1,1]].
Barrier: 6x3 pixel units, orange/light orange (#f97316/#fdba74), pattern: [[1,2,1,2,1,2],[1,2,1,2,1,2],[1,1,1,1,1,1]].
Pothole: 3x2 pixel units, dark/light gray (#4a5568/#718096), pattern: [[1,1,1],[1,0,1]].
Scorebar: At the top of the canvas, background #2c5282, white text. Displays: score, level, life (❤️/🖤).
Message Overlay: Semi-transparent black background, centered display of game status information (start, upgrade, end). Title uses 'Press Start 2P' font, content uses 'Inter'. Contains "Start/Restart" button.
4. Game Mechanics
Score: +10 points for avoiding obstacles.
Life: Starts with 3 points, decreases by 1 on collision.
Level: Starts at 1, upgrades when score reaches current level * 150, overlay shows "LEVEL X!" for about 2 seconds.
Speed and Difficulty:
Initial forward speed (obstacle/road line) 1.5.
Every 10 points, speed increases slightly by 0.0025.
Each level up, speed increases by 0.3.
Maximum forward speed 7. Player car response speed (playerCar.speed) also slightly increases with level and has an upper limit.
Obstacle Generation:
Initial interval 2500ms. After level up, shortens by 150ms (minimum 500ms).
Maximum number of obstacles on screen 6 + current level.
Collision: AABB detection. Consequence: Life -1, remove obstacle. Feedback: brief screen shake (CSS animation).
5. Game State
Initial: Title "Pixel Racing", operation instructions, "Start Game" button.
In Progress: Normal game, real-time UI updates.
Level Up: Briefly displays level information.
End: "Game Over!", displays final score and level, "Restart" button.
6. Technical Requirements
Single HTML file: Includes all HTML, CSS, JS.
CSS: Mainly Tailwind CSS (CDN), with a small amount of custom <style>.
Fonts: Google Fonts: 'Inter', 'Press Start 2P'.
JavaScript: Clear, modular, well-commented code. No external game engine.
Responsive: Adapts to desktop and mobile devices.
```