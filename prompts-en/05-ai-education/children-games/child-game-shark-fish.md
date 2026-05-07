---
title: "Child Game Shark Fish"
category: "AI Education"
subcategory: "Children Games"
source_section: "prompts/05-ai-education/children-games/child-game-shark-fish.md"
author: "Yao Jingang"
version: "V1.0-en"
status: "active"
tags: "AI Education, Children Games, Child, Game, Shark"
---
# Kids Game: Shark Catch Fish

## Introduction
After children come up with ideas, use AI to generate playable single-file HTML5 games.

## Prompt
```markdown
## Role (Role): 
You are a professional HTML5 game development AI assistant.

## Task (Task): 
Create a complete, interactive HTML, CSS and JavaScript single-file web game named "Shark Catch Fish!". This game is designed for children around 6 years old, and should include the following core features and behaviors:

Game Concept and Theme:
Core Gameplay: Players control the shark with the mouse, chasing and "eating" schools of small fish in a 2D aquatic environment.
Target Audience: Children around 6 years old, so the visual style, interaction, and difficulty should be appropriate.
Visuals and UI/UX:
Overall Style: Bright and colorful, cartoonish. Background is sky blue or light sea blue, canvas (game area) is a darker sea blue.
Character Design:
Small Fish (Boids): Multiple small, variously colored (mainly blue/green tones) cartoon fish with eyes.
Shark: A single, significantly larger cartoon shark (e.g., gray-blue body, red eyes, with a mouth).
Canvas: Responsive size, adapting to different screens.
UI Elements:
Prominent game title: "Shark Catch Fish!"
Clear score board showing the score in real time.
Simple gameplay instructions: "Use the mouse to control the big shark, catch the blue little fish!"
Control Panel: Contains the following adjustable sliders and displays their values in real time:
Number of Small Fish (NumBoids)
Shark Speed (SharkSpeed)
Fish Reaction (FishReaction - affects the strength of evasion)
"Restart!" (Reset) button.
Effects: When a small fish is eaten, create several rising small bubble animations at its position.
Behavior Logic of Small Fish (Boids) (optimized for children's games based on Boids algorithm):
Group Behavior:
Separation: Avoid being too close to nearby small fish, maintaining a certain distance.
Alignment: Tend to swim in the same direction as nearby small fish.
Cohesion: Tend to move towards the center of nearby small fish groups.
Individual Behavior:
Wander: Core behavior. Each small fish should have a continuous and significant intrinsic random movement tendency, changing direction and moving independently even without external stimuli (like sharks) or group influence, effectively preventing the formation of stationary fish groups. The intensity of this behavior should be sufficient to break overly stable group structures.
Flee from Shark: When the shark enters its perception range, produce a strong evasive behavior, quickly fleeing.
Avoid Edges: When approaching the canvas edge, produce a strong turning force to guide it back to the center of the canvas, preventing it from getting stuck at the edges for long periods.
Edge Wrapping: As an auxiliary feature, if a small fish completely leaves the canvas, it re-enters from the corresponding opposite side.
Shark Behavior Logic:
Control: Controlled by the mouse position within the canvas in real time.
Movement (Seek): Smoothly swims towards the mouse pointer position.
Arrival Behavior: When the shark is very close to the mouse pointer (e.g., less than half its own size) and the mouse is stationary, the shark should smoothly decelerate and stop, avoiding jittering back and forth at the target point. It should remain oriented when stopped.
Game Mechanisms and Interaction:
Feeding: When the shark collides with a small fish (visually overlapping), it is considered that the small fish is "eaten".
Scoring: Score increases by one for each small fish eaten.
Sound Effects:
Use the Tone.js library.
Play a short, fun "eaten" or "bubble" sound effect (e.g., short notes within the C4-F4 range) whenever the shark eats a small fish.
The audio context should be initialized after the user's first interaction with the page (e.g., click) to comply with browser policies.
Fish Resupply: When the number of small fish decreases to a certain extent (e.g., less than half the initial number and the total is low), automatically and slightly resupply new small fish to maintain game playability.
Technical Implementation:
Use HTML, CSS (can be inline or use Tailwind CSS CDN) and pure JavaScript.
Introduce Tone.js (CDN).
All behavior parameters (such as weights of various forces, perception radius, speed, turning force, etc.) need to be carefully adjusted to achieve lively and active individual movement of small fish, natural fish school shapes, and ensure the effectiveness of the above anti-clustering, edge handling, and shark stopping behaviors.

## Format (Format): 
Generate a standalone, fully functional HTML file containing all necessary CSS styles and JavaScript logic. Ensure the code structure is clear and well-commented (especially key logic sections).
```