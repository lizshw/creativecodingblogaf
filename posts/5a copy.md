---
title: JavaScript Ecology: Libraries, Packages, & Modules
published_at: 2025-04-03
snippet: Week 5 Thursday
disable_html_sanitization: true
allow_math: true
---

### JavaScript Ecology: Libraries, Packages, & Modules

<script src="./scripts/p5.js"></script>

<canvas id="p5_example"></canvas>

<script>
    const cnv = document.getElementById ("p5_example")


    let gridSize = 4; // Initial grid size
    let squareSize;    
    let highlightedSquares; // 2D array to store highlighted squares
    let bwMode = false;
    let newRandomColor;
    let centerColor;
    let particles = []; // Store floating particles

    function setup() {
    createCanvas (1000, 500, P2D, cnv)
    squareSize = width / gridSize; 
    highlightedSquares = createGrid(gridSize); // Initialize grid
    newRandomColor = randomColor();
    centerColor = darkenColor(newRandomColor, 50);
    for (let i = 0; i < 10; i++) {
    particles.push(new Particle());
    }
    }

    function draw() {
    background(220);
    noStroke();

    // Recalculate square size when grid size changes
    squareSize = width / gridSize;

    for (let i = 0; i < gridSize; i++) {
        for (let j = 0; j < gridSize; j++) {
        let x = i * squareSize;
        let y = j * squareSize;
        /*
        // Set the correct color based on the stored grid state
        if (highlightedSquares[i][j] === "pink") {
            fill("pink");
        } else if (highlightedSquares[i][j] === "purple") {
            fill("purple");
        } else if (highlightedSquares[i][j] === "blue") {
            fill("blue");
        } else if (highlightedSquares[i][j] === "yellow") {
            fill("yellow");
        } else if (highlightedSquares[i][j] === "green") {
            fill("green");
        } else {
            fill("powderblue"); // Default color
        }*/
        fill(highlightedSquares[i][j] || "powderblue"); 
        // Default to powderblue if no color is stored
        rect(x, y, squareSize, squareSize);
        }
    }
    for (let particle of particles) {
        particle.update();
        particle.display();
        }

    updateHighlightedSquares(); // Update the grid for hover effect
    }

    function createGrid(size) {
    let arr = [];
    for (let i = 0; i < size; i++) {
        arr[i] = [];
        for (let j = 0; j < size; j++) {
        arr[i][j] = null; // Default state
        }
    }
    return arr;
    }

    function updateHighlightedSquares() {
    // Reset grid state before re-applying highlights
    highlightedSquares = createGrid(gridSize);

    for (let i = 0; i < gridSize; i++) {
        for (let j = 0; j < gridSize; j++) {
        let x = i * squareSize;
        let y = j * squareSize;

        // If mouse is over this square, mark it and its neighbors
        if (mouseX > x && mouseX < x + squareSize && mouseY > y && mouseY < y + squareSize) {
            highlightedSquares[i][j] = centerColor; // Hovered square
            checkSquares(i, j);
        }
        }
    }
    }

    function checkSquares(i, j) {
    // left
    if (i > 0) {
        highlightedSquares[i - 1][j] = newRandomColor; 
    }
    // right
    if (i < gridSize - 1) {
        highlightedSquares[i + 1][j] = newRandomColor; 
    }
    // top
    if (j > 0) {
        highlightedSquares[i][j - 1] = newRandomColor;
    }
    // bottom
    if (j < gridSize - 1) {
        highlightedSquares[i][j + 1] = newRandomColor;
    }
    }

    function mousePressed() {
    gridSize++; // Increase grid size
    highlightedSquares = createGrid(gridSize);// Reset the grid data for the new size
    newRandomColor = randomColor();
    centerColor = darkenColor(newRandomColor, 50);
    
    for (let i = 0; i < 5; i++) {
        particles.push(new Particle());
        }
    }

    function keyPressed() {
    if (key === 'B' || key === 'b') {
        bwMode = !bwMode; // Toggle black-and-white mode

        // Update all existing particles' colors
        for (let particle of particles) {
        if (bwMode) {
            particle.color = color(0, 0, random(50, 150)); // Random grayscale but avoid white
        } else {
            particle.color = randomColor(); // Return to random colors
        }
        }
    }
    mousePressed();
    }


    function randomColor() {
    colorMode(HSB);
    if (bwMode) {
        let gray = random(50, 100); // Light gray to white
        return color(0, 0, gray);
    } else {
        return color(random(360), 100, 100); // Vibrant color
    }
    }

    function darkenColor(col, amount) {
    colorMode(HSB);
    let h = hue(col);
    let s = saturation(col);
    let b = brightness(col);
    
    if (bwMode) {
        return color(0, 0, max(b - amount, 0)); // Keep grayscale
    } else {
        return color(h, s, max(b - amount, 0));
    }
    }

    class Particle { // defining a new class called 'Particle'
    constructor() { // called when a new particle is created
        this.x = random(width); // x pos between 0-width
        this.y = random(height); // y pos between 0 - height
        this.size = random(5, 15); // size of particle between 5-15
        this.xSpeed = random(-1, 1); // horizontal speed between -1 - 1
        this.ySpeed = random(-1, 1); // vertical speed between -1 - 1
        this.color = randomColor(); // colour using randomColour function
    }

    update() { // called to update the particles
        this.x += this.xSpeed; // add horizontal speed to current x pos to move the particle
        this.y += this.ySpeed; // add vericle speed to current x pos to move the particle

        // Bounce off edges
        if (this.x < 0 || this.x > width) this.xSpeed *= -1;
        if (this.y < 0 || this.y > height) this.ySpeed *= -1;
    }

    display() { // called to draw the particles
        fill(this.color);
        ellipse(this.x, this.y, this.size);
    }
    }

</script>
