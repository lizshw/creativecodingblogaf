---
title: Canvas API, Recursion, & Effective Complexity
published_at: 2025-03-20
snippet: Week 4 Tuesday Homework
disable_html_sanitization: true
allow_math: true
---

# Canvas API, Recursion, & Effective Complexity

## My Three Sketches

### High Compressibility

This sketch is super simple — it’s just a grid of squares, all the same size, evenly spaced, nothing too wild. You could describe the whole thing with just a few lines: “draw a bunch of squares across and down.” It’s super easy to explain and reproduce, which is why it’s highly compressible. It’s kind of boring to look at, but that’s kind of the point — it’s all about structure.

<iframe id="w4s1" src="https://editor.p5js.org/lizshw/full/Uh2LX-IrP"></iframe>

<script type="module">

    const iframe  = document.getElementById (`w4s1`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

### Low Compressibility

This one’s the total opposite. It’s chaotic — squares randomly popping up in all kinds of positions, colors, and sizes every time you run it. There’s no clear pattern or structure, and it’s pretty much impossible to describe simply. It looks cool in its own wild way, but there's no obvious system behind it — just noise.

<iframe id="w4s23" src="https://editor.p5js.org/lizshw/full/RVVeZXhV6"></iframe>

<script type="module">

    const iframe  = document.getElementById (`w4s2`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

### High Effective Complexity

This is my favorite. It looks like a tree made out of squares, and it’s built using recursion — basically, the same bit of code repeats and draws smaller and smaller “branches.” It follows a set of rules (structure), but I added a bit of randomness to the angles so it doesn’t look too robotic. It’s got a natural vibe, like something you might actually see growing outside. It’s not totally predictable, but it’s not just chaos either — it’s right in the middle, which is what makes it feel alive.

<iframe id="w4s3" src="https://editor.p5js.org/lizshw/full/s2RwBw_Hl"></iframe>

<script type="module">

    const iframe  = document.getElementById (`w4s3`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

## Why Subjective Structure Matters in Generative Art

In his paper, Galanter says structure is kinda in the eye of the beholder — and honestly, that’s pretty useful for generative art. What looks like noise to one person might feel meaningful to someone else. That gives us more freedom as artists. It means we can play with randomness and still get something that feels organized or intentional, even if it’s technically unpredictable.

All three of my sketches show this in different ways. The tree sketch especially hits that sweet spot — there’s a pattern, but it’s loose enough to surprise you. That’s what makes generative art fun — it’s not about strict rules or complete chaos, it’s about finding that magic in-between.

## What’s Making the Structure in the Tree Sketch?

The structure comes from recursion — one function calling itself to build smaller and smaller branches. Each “branch” is a stretched square, and it splits off from the one before it. The randomness in angle makes each version unique, but the way the tree grows upward and splits is always the same. So you’ve got rules + surprise = effective complexity.

## Artist Example: Casey Reas

Casey Reas is a great example of someone who plays with structure and randomness. His work uses systems of rules — like instructions for drawing — but introduces random elements that change how each piece looks. Some of his stuff feels super organic, even though it’s all coded. That balance between machine logic and randomness is what gives his work its energy and complexity — it’s like the code is alive.
