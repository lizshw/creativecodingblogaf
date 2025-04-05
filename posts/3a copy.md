---
title: Images, Sound, & Interaction
published_at: 2025-03-18
snippet: Week 3 Tuesday Homework
disable_html_sanitization: true
allow_math: true
---

# Images, Sound, & Interaction

## Cute in my project

Instead of aiming for a soft, soothing kind of cuteness, my project leans into the idea of "cute chaos"—a vibrant, energetic overload that keeps Reese focused and entertained.

**Visually – Bright, Bouncy, and Busy**

- High-contrast, neon-inspired colors that shift dynamically, grabbing Reese’s attention.

- A constantly changing grid where shapes react in real-time, keeping movement unpredictable but fun.

- Fast but smooth transitions - everything moves in a way that feels lively, not harsh.

**Sonically – Playful but Not Overwhelming (Potential Additions)**

- High-pitched, bubbly sound effects that match the energy of the visuals, creating a full sensory experience.

- Sounds that respond to interaction, reinforcing the feeling of playful feedback.

**Interactivity – A Constantly Changing Playground**

- A hyper-responsive grid that reacts instantly to movement, making it feel alive.

- Clicking changes the grid size, adding a layer of unpredictability that keeps things fresh.

- A chaotic but engaging experience—not calming, but captivating enough to distract Reese when he’s stressed.

My project embraces the idea of cute chaos by using bright, high-contrast colors and dynamic movement that draws Reese’s attention while keeping the experience playful and engaging. The grid of colorful shapes constantly changes, reacting to mouse movement and clicks, creating a visually stimulating environment similar to how colorful bouncing balls or playful animations might catch the eye. The shapes grow, shrink, and shift in size, creating an erratic but smooth visual effect that mirrors the bouncy, chaotic motion found in lighthearted mobile games or animated GIFs. The movement is unpredictable but never harsh, making it more like a game of constant, playful change—an overload of visual stimulation designed to entertain without overwhelming.

If sound were added, I would include soft, playful chimes or tone shifts, similar to the background noises you might hear in playful, whimsical games or apps, further emphasizing the light-hearted nature of the chaotic visuals. Overall, the combination of constant color shifts, interactive changes, and potential sound creates a dynamic yet cute environment—one that mimics the feel of energetic yet harmless chaos, keeping Reese distracted and entertained.

## Cute in Rafaël Rozendaal’s "Reflection"

Rafaël Rozendaal’s _Reflection_ achieves a cute aesthetic through a combination of simple visuals, playful interactivity, and subtle sonic design. Visually, he uses bold, high-contrast colors and smooth gradients in simple geometric shapes, which create an inviting and playful atmosphere. The rounded forms and the soft transitions between colors give the piece a gentle, non-threatening appearance, avoiding any harsh edges or sharp lines. The reflective effect adds a sense of depth without complicating the overall minimalist composition, keeping it visually light and approachable.

While _Reflection_ doesn’t explicitly incorporate sound, Rozendaal’s works often embrace silence as part of the experience. The absence of sound allows the visuals to take center stage, creating a calm, almost meditative environment. If sound were included, it would likely be something soft and ambient, reinforcing the gentle and hypnotic feel of the artwork.

Interactivity in _Reflection_ is gentle and responsive. The piece reacts smoothly to the user’s input, creating a fluid experience that feels natural rather than rigid. The mirrored effect of the interaction evokes a childlike sense of curiosity, encouraging exploration in a playful and non-intimidating way. There are no complex controls or any sense of punishment for mistakes, making the experience simple, satisfying, and fun to engage with.

Overall, Rozendaal’s work achieves cuteness not by relying on traditional notions of sweetness, but by being approachable, playful, and lighthearted. It invites the user to engage with it in a way that feels effortless and enjoyable, which is key to the "cute" aesthetic.

## My Project Update

<iframe id="a1d2" src="https://editor.p5js.org/lizshw/full/4W4SelKOk"></iframe>

<script type="module">

    const iframe  = document.getElementById (`a1d2`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

This sketch demonstrates me trying to add the colour changing feature of the squares, where the squares touching the hovered square also change colour. I struggles with this for a while before realising that the order of events were writing code over important code (if that makes sense). The right and bottom square would be drawn, then imediately drawn over again.

<iframe id="a1d3" src="https://editor.p5js.org/lizshw/full/QYawmBH6d"></iframe>

<script type="module">

    const iframe  = document.getElementById (`a1d3`)
    iframe.width  = iframe.parentNode.scrollWidth
    iframe.height = iframe.width * 9 / 16 + 42

</script>

This sketch fixed my problem by changing the order of events. I also added a random colour changer for the colour every time you click, including a dakrer colour for the middle of the square. I replaced my old way of colouring the squares with an array inside an array. Very hard for me to comprehend at times, a lot of drawings were used. I also started to make a black and white mode (to include a boolean), starting when the user clicks 'B' on the keyboard.
