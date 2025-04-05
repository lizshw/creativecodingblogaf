---
title: This is my second blog post
published_at: 2025-03-04
snippet: Week 1 Tuesday Homework
disable_html_sanitization: true
allow_math: true
---

# Grid Square Experimentation

## Attempt 1

<iframe id="diagonal_line" src="https://editor.p5js.org/lizshw/full/22QWXT7vO"></iframe>

<script type="module">

    const iframe  = document.getElementById (`diagonal_line`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

With this attempt, I made the y position of the squares a variable. I noticed that in the template, it was a static number. If I were to make it a variable, I could change the location and number of the squares, making it a grid. That's how I view the difference between a line and a grid, a grid being just more lines. I found the size of the square by using 'console.log(innerWidth)' to find the width of the canvas, then divided that by the total number of squares (10), before realising I could have just checked console.log(size) which basically does that for me. I changed the canvas size to 385 to fit the squares perfectly ((size / 2) \* 10 + (size / 2))
</script>

## Attempt 2

<iframe id="vertical_grid" src="https://editor.p5js.org/lizshw/full/KVbXMIKHm"></iframe>

<script type="module">

    const iframe  = document.getElementById (`vertical_grid`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

With this attempt, I started from the base template again and duplicated the code, changing the y positioning by half the size (35) each time. In theory this is a grid, but I think it would look better if the size ran diagonally rather than vertically. Obviously the code could be more efficiant, likely using another for loop that references 'i' and 'size'.

</script>
