---
title: Redundancy, Style, & Refactorisation
published_at: 2025-03-20
snippet: Week 3 Thursday Homework
disable_html_sanitization: true
allow_math: true
---

# Redundancy, Style, & Refactorisation

## My Assignment 1

### Variables

- Store important data like grid size, mouse position, and colour mode (normal or black and white).

- Allow the sketch to update dynamically based on user interaction.

### Functions

- Keep the code organized by handling specific tasks.

- Used for generating new colours, updating the grid based on mouse movement, and toggling black-and-white mode.

- Make the code more reusable and easier to modify.

### Iteration

- Uses for loops to cycle through the grid and update each square efficiently.

- Ensures that when the grid expands, each new square is assigned a colour.

- Allows the sketch to respond quickly to mouse movements and clicks.

### Boolean Logic

- Used to toggle black and white mode (bwMode variable).

- Determines whether the mouse is hovering over a square.

- Controls whether a click should expand the grid.

### Arrays

- Stores the grid of squares as a 2D array, keeping track of their colours and states.

- Manages floating particles, allowing them to change colour when the mode switches.

- Makes it easier to update and manipulate multiple elements at once.

### Classes

- Defines particles with properties like position, speed, and colour.

- Makes it easy to generate and animate multiple floating particles.

- Keeps the code modular and organized, making future expansions easier.

## Reflection of my project so far

I think I achieved a cute aesthetic in a few different ways. Visually, the bright, changing colours and interactive grid create a playful and engaging experience. The way the squares shift and react to movement makes the project feel lively, which suits Reese’s love for fast-moving visuals. Sonically, I haven't included anything uet, but when I add it, I would use softer more gentle noises to enhance the lighthearted, playful mood. Interactively, the project is engaging because it responds directly to user input—hovering changes colours, clicking expands the grid, and pressing “B” shifts the entire aesthetic. This level of responsiveness makes the experience feel dynamic and fun, adding to the overall sense of cute chaos.

For learning resources, I used a mix of different platforms. W3 Schools, Reddit, the inbuilt P5 tutorials, classes, and various online forums helped me figure out specific coding issues, especially when I ran into problems with interactivity. My dad, who has experience with coding, also helped me understand certain programming concepts when I got stuck. Some topics I remembered from highschool easily, others were difficult to comprehend at first, but asking ChatGPT to break them down into simpler explanations really helped. Having things explained step by step in the simplest terms made it easier to understand how different parts of my code worked together.

One of the biggest challenges in this project was handling the colours around the hovered mouse square. At first, I couldn’t figure out why the effect wasn’t working properly—I had only the top and left squares changing because my fill was being overwritten when the grid refreshed. Once I realised what was happening, I was able to adjust the logic and fix it. Then getting the colours to change was another stuggle. I decided on using an array but in hindsight I think I could also have used classes. Another challenge was getting back into coding after taking breaks. Sometimes, I would come back to my project and have no idea what I was working on or where I left off. To help my future self, I started using pictures, diagrams, and comments to explain what I had done and what still needed to be fixed. This made it much easier to jump back in without wasting time trying to remember what I was thinking before.

The most enjoyable part of this process was when I worked on something for ages, couldn’t figure out why it wasn’t working, and then finally solved it myself. That feeling of everything clicking into place after struggling for so long was incredibly satisfying. It was also surprising how much personality and energy the project gained just from adding simple interactivity and randomness—what started as a basic grid quickly became an engaging, chaotic, and playful environment. Seeing Reese react to the visuals made it even more rewarding, since the whole point was to create something he would enjoy.

Overall, this project has been a great way to explore interactive visuals and creative coding. Even though some parts were difficult to grasp at first, breaking things down into smaller concepts and experimenting with different solutions helped me work through the challenges.

## My Project Update

<iframe id="a1d4" src="https://editor.p5js.org/lizshw/full/vF-jB20yV"></iframe>

<script type="module">

    const iframe  = document.getElementById (`a1d4`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

This sketched took me the longest as I introduced the particles. I did play around with how the user could interact with them, initially trying to make it so when the mouse moved the particles would avoid the curser, but I felt that because I couldn't perfect it, it made the entire project feel to messy chaotic rather than cute chaotic. I made the particles "bounce" off the walls which was easier than I expected. I also made the particles use randoms and interact with black and white mode.

https://editor.p5js.org/lizshw/sketches/lQ1Nd6ZXv

<iframe id="a1d5" src="https://editor.p5js.org/lizshw/full/lQ1Nd6ZXv"></iframe>

<script type="module">

    const iframe  = document.getElementById (`a1d5`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

This sketch I did my final touches and added sound when the user clicks the mouse using a random array
