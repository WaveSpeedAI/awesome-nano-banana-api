# Awesome Nano Banana API 🍌 — Prompts, Variants & One-Call Image Generation

> The most complete open guide to **Google Nano Banana — the viral AI image model (Nano Banana 2 & Pro, text-to-image + edit)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><img src="https://img.shields.io/badge/▶_Run_Nano_Banana_2-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run Nano Banana 2"></a>
  <a href="https://wavespeed.ai/nano-banana-pro-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><img src="https://img.shields.io/badge/Nano_Banana_Pro-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="Nano Banana Pro"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api">WaveSpeedAI</a> — serverless Nano Banana API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>→ Get a Nano Banana 2 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/nano-banana-pro-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>→ Try Nano Banana Pro</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/image-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>WaveSpeedAI Image Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run google/nano-banana-2/text-to-image -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is Nano Banana?](#what-is-nano-banana)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 12 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is Nano Banana?

**Nano Banana** (Google) is the viral AI image model behind the internet's favorite character-consistent edits and figurine renders. WaveSpeed serves **Nano Banana 2** (+ lite / fast) and **Nano Banana Pro** (+ ultra / multi) — text-to-image and edit.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/google/nano-banana-2/text-to-image" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A collectible figurine of a corgi astronaut on a clear acrylic base, studio light"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your Nano Banana 2 API key](https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api)** · pay-as-you-go, live pricing on each model page.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### Nano Banana 2 &nbsp;[▶ API](https://wavespeed.ai/nano-banana-2-api)
[text-to-image](https://wavespeed.ai/models/google/nano-banana-2/text-to-image) · [edit](https://wavespeed.ai/models/google/nano-banana-2/edit) · [fast](https://wavespeed.ai/models/google/nano-banana-2/text-to-image-fast) · [lite](https://wavespeed.ai/models/google/nano-banana-2-lite/text-to-image)

### Nano Banana Pro &nbsp;[▶ API](https://wavespeed.ai/nano-banana-pro-api)
[text-to-image](https://wavespeed.ai/models/google/nano-banana-pro/text-to-image) · [edit](https://wavespeed.ai/models/google/nano-banana-pro/edit) · [ultra](https://wavespeed.ai/models/google/nano-banana-pro/text-to-image-ultra) · [edit-multi](https://wavespeed.ai/models/google/nano-banana-pro/edit-multi)

> Full catalog: **[wavespeed.ai/nano-banana-2-api](https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api)**

---

## Prompt Library

12 prompts curated from the Nano Banana creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. Ukiyo-e holographic trading card
*by [@MANISH1027512](https://x.com/MANISH1027512)*

```
Core instruction: a collectible trading-card design in Japanese ukiyo-e style, vertical composition. The illustration closely mimics the visual aesthetics of "Demon Slayer": ink-brush outlines with varying stroke weight, a traditional woodblock-print color palette, and dramatic dynamic composition.

Subject: the card features {character name} (title: {Hashira title/epithet}) in a dynamic combat pose, wielding {weapon description}. The character is unleashing {breathing-technique name}, surrounded by {VFX description} (e.g., massive flames / a water dragon / a whirlwind), rendered in traditional Japanese sumi-e ink style.

Background & material: blend in a textured holographic foil effect shimmering beneath the traditional ink elements.

Border: a decorative frame of traditional Japanese patterns (seigaiha waves or asanoha hemp-leaf). At the bottom, a stylized banner with "{name in Japanese kanji}" in antique Japanese calligraphy.
```

### 2. Thirty clones of one character
*by [@tapehead_Lab](https://x.com/tapehead_Lab)*

```
Based on the uploaded reference character, shoot a live-action scene inside a spacious Tokyo-girl apartment — a bright, lived-in studio close to 1LDK proportions. The room includes white walls, warm wood flooring, beige curtains, a low bed with soft bedding, a desk with cosmetics, bookshelves, plants, a full-length mirror, a rug, scattered personal items, and a compact kitchen area at the back. The room must have strong depth of field, with distinct foreground, midground, and deep background layers.

Place about thirty copies of the reference character in the room (same face, hair, and outfit as the reference), each in a different action or interaction. Vary spacing, scale, height, and visibility so the room's density feels natural.

Foreground (very close to camera / partially occluded):
- someone walking past the lens, slightly out of focus
- a hand or shoulder entering the frame
- one person leaning toward the camera
- one person half-hidden behind a large plant
- one person sitting up front, tying her hair
- one person kneeling by the desk sorting items

Midground (main room area):
- stretching by the bed
- sitting on the bed checking a phone
- lying face-down on the bed
- reaching under the bed
- arranging cosmetics on the desk
- browsing books on the shelf
- standing at the mirror
- crouching on the rug
- leaning against the wall
- gazing out the window
- adjusting the curtains
- carrying laundry
- drinking from a cup
- fluffing pillows
- sitting on the floor snacking
- doing a small jump or motion-blur action
- moving a small chair

Background (deep field / near kitchen and hallway):
- standing at the stove drinking water
- opening a cabinet
- sitting on a stool
- leaning in the doorway
- walking toward the hallway
- silhouette partially blocked by the fridge
- reaching for a high shelf
- standing far off in the entryway
- faintly visible through the hallway frame
- sitting on the floor near the kitchen mat

Ensure strong layered occlusion: foreground figures partially block midground figures; background figures appear smaller with natural perspective falloff. Scatter the thirty figures naturally — no symmetry or grid alignment. Light everyone with soft natural daylight so they blend seamlessly with the environment.

Place the characters in a real setting matching the illustration's pose and composition while faithfully preserving the illustration's texture and style. Use realistic lighting, depth of field, and subtle photographic effects to fuse illustration and reality.
```

### 3. Flowchart from a paper
*by [@anderssandberg](https://x.com/anderssandberg)*

```
A diagram of the process for building a Dyson swarm, based on the paper: Armstrong, S., & Sandberg, A. (2013). Eternity in six hours: Intergalactic spreading of intelligent life and sharpening the Fermi paradox. Acta Astronautica, 89, 1-13.
```

### 4. Slide deck from an article
*by [@op7418](https://x.com/op7418)*

```
Turn the article below into a slide deck a middle-schooler could understand.

First write a deck outline planning the content of every slide.

Then feed each slide's content to Nano Banana Pro to generate that page, keeping the style consistent.

The deck style should be "Anthropic/Claude-style" "warm academic humanism":

Background: warm beige/cream (#F3F0E9) as the base, mimicking premium paper.

Fonts: elegant serif for titles, modern sans-serif for body text.

Palette: terracotta (#D67052) and mustard (#F0B857) as primaries, deep navy as accent. No neon colors or pure black.

Visual elements: typography-first grid layouts; illustrations as abstract, organic black hand-drawn linework over solid terracotta blocks; key information in card layouts.

Charts: flat, minimal bar charts emphasizing comparison, no extra borders.

Both text and imagery are generated by Nano Banana Pro. Do not merge the deck into one big image — one image per slide.

Article content: []
```

### 5. Fashion character breakdown sheet
*by [@cheerselflin](https://x.com/cheerselflin)*

```
A hand-drawn fashion concept exploded diagram.

Center: a full-body figure of a stylish, confident, subtly alluring (never explicit) female character in a natural, energetic pose.

Around her, a structured layout of her key elements:

• Clothing layers — outerwear, innerwear, tights (lace, tulle), shapewear, with enlarged detail patterns.

• Expression sheet — 3-4 facial expressions (neutral, shy, surprised, focused).

• Close-ups — fabric fold textures, skin detail, hand gestures.

• Lifestyle & accessories — an open handbag spilling everyday items: lipstick, perfume, compact, hand cream, a journal, supplements.

• Material callouts — handwritten-style notes beside each item (e.g., "soft lace", "matte leather", "shade #520").

Background: soft beige or parchment texture for a design-sketch atmosphere.

Lighting: clean soft shadows unifying the frame.

Output: 4K HD 2D illustration, both alluring and fashionable.

Language: bilingual labels.
```

### 6. Kids' vocabulary poster
*by [@lxfater](https://x.com/lxfater)*

```
Generate a children's vocabulary learning poster, "The Amusement Park" — vertical A4, school-newsletter layout, for kids aged 5-9 learning words through pictures.

1. Title area (top): large centered title "Amusement Park Word Poster". Style: kids' classroom-newsletter feel. Big, bold, cartoon handwritten type with colorful outlines. Decorate with bright sticker-style amusement-park elements.

2. Main scene (center): a cartoon illustration of an amusement park. Mood: bright, warm, positive. Composition: objects have clear boundaries for easy labeling — not crowded. Zone A (main subjects): the park's core activities (kids on rides). Zone B (supporting facilities): related items (ticketing, snacks, signage). Zone C (environment): entrance, signposts, bunting, lawns. One cute cartoon guide character (park staff or a young visitor) doing a natural interaction — smiling, pointing the way, waving, playing with kids.

3. Required objects & word list — draw each clearly and leave room for its label:
1) Core roles & rides: staff member, ticket booth, roller coaster, Ferris wheel, carousel
2) Common items: ticket, balloon, ice cream, popcorn, candied fruit skewer, mask, toy, little flag
3) Environment: entrance, exit, signpost, bunting, plaza
(More objects are fine, but the list above must be the focus — 18 typical nouns suitable for ages 5-9.)

4. Labeling rules: each listed object gets a word label. Format: two lines (pronunciation on top, the word below). Style: colorful sticker look, dark text on white, clearly readable. Placement: next to its object, never covering it.

5. Art style: children's picture-book + learning-poster style. Colors: high saturation, bright, warm tone. Quality: 8k resolution, high detail, vector illustration style, clean lines.
```

### 7. Giant creature over a real city photo
*by [@AI_GIRL_DESIGN](https://x.com/AI_GIRL_DESIGN)*

```
Use the uploaded city photo as the base. Do not alter the real buildings, streets, vehicles, or people — keep the photo authentic. Add one enormous, stylized illustrated creature in the sky above and behind the buildings, as if it overlooks the whole city. Draw the creature in a flat graphic style with clean outlines and a limited neon palette (soft neon green, neon yellow, lime), like a mural or poster illustration.

Creature design:
- whimsical fantasy, never horror or violence
- built from layered shapes, scales, fur, or floral patterns
- long arms or hair draping beside the buildings
- huge horns or other fantastic features silhouetted against the sky

Blending with the photo:
- place the creature partially behind building edges with correct perspective
- correct overlap: building edges in front, creature behind, so it sits inside the scene
- if needed, add very soft shadows or color reflections on nearby building faces — keep it subtle
- keep the sky's original brightness so the illustration reads clearly

Optional:
- add a few small, simple illustrated figures on the street (flat, minimal style) — walking a dog, crossing the road — without covering real people.

Overall mood: a dreamlike, surreal cityscape where one giant, friendly illustrated creature rises above realistic buildings — real photography meets clean modern illustration.
```

### 8. Half-cutaway toy teardown
*by [@ZeroZ_JQ](https://x.com/ZeroZ_JQ)*

```
A single [Astro Boy] toy on a table, split into left and right halves for display: the left half is the normal toy; the right half is a transparent shell revealing the internal structure clearly, with white callout lines explaining what each part does. On a tabletop, bright background, blurred table. The left side shows the half-transparent, half-solid toy; the right side of the frame shows the parameters pointed out by the callout lines.
```

### 9. Fluffy plush logo
*by [@toolfolio](https://x.com/toolfolio)*

```
Transform a simple flat vector logo into a soft, fluffy 3D object. Keep the original colors. The object is entirely covered in fur, with hyper-realistic hair texture and soft shadows. It floats gently in the center of a clean light-gray background. The style is surreal, tactile, and modern, evoking comfort and playfulness. Studio lighting, high-resolution render.
```

### 10. Crystal-glass emoji objects
*by [@ZHO_ZHO_ZHO](https://x.com/ZHO_ZHO_ZHO)*

```
A photorealistic, highly detailed image of [a 3D instant camera] rendered in crystal-clear, highly polished transparent glass. [The body has real thickness and depth; the classic instant-camera signature forms — boxy body, front lens, top viewfinder, front shutter button, and bottom film slot — are all rendered in simplified yet precise geometry, instantly recognizable without any graphics]. All edges have rounded bevels and smooth curves that refract light elegantly. The camera sits slightly tilted, as if floating above a spotless, seamless pale-cream or very light gray studio background.

Bright, clean professional studio lighting emphasizes the glass's transparency, mirror reflections, and refraction. Sharp, delicate highlights on the bevels, film-slot edges, and lens ring convey a crystalline, luxurious look. Light passing through the glass body bends and distorts subtly — most visibly where the lens thickness changes, inside the film slot, and around the viewfinder — greatly boosting realism. A soft, diffuse shadow falls below and slightly behind the camera, grounding it without breaking the minimalist mood.

Overall aesthetic: minimal, modern, clean — high-end product photography meets concept-art rendering. The frame focuses entirely on the glass camera's crystalline material and classic geometry. High-key lighting and shallow depth of field keep the camera tack-sharp while the background melts away.
```

### 11. Inflatable puffy logo
*by [@gizakdag](https://x.com/gizakdag)*

```
Turn the attached logo into a high-resolution 3D render shaped like an inflated, puffy object. It should look soft and plump, like a plush balloon or inflatable toy. Use a smooth matte texture with subtle fabric wrinkles and stitching to emphasize the inflated look. Slightly elastic feel, with soft shadows and lighting enhancing volume and realism. Place it on a clean light-gray background.
```

### 12. Face-scan age estimate infographic
*by [@Samann_ai](https://x.com/Samann_ai)*

```
From (your photo), create a hyper-realistic, high-resolution portrait infographic. Keep the person's identity, hairstyle, clothing, and natural skin tone from (your photo) unchanged, on a neutral studio background. Overlay a subtle, semi-transparent facial-analysis mesh across the face, like a 3D face-scan grid: thin, soft white lines following the facial contours, slightly luminous but never hiding skin detail. Add one crisp vertical red laser line across one side of the face, like a futuristic scanning effect. All analysis lines must be soft, clean, and elegant, like a beauty-tech ad.

Make a clean medical-aesthetics infographic scoring 5 aging factors with global-data percentages: 1. fine lines & wrinkles; 2. skin texture & elasticity; 3. facial volume & sagging; 4. periocular aging signs; 5. skin tone & pigmentation. For each factor, place a small label with a thin leader line to the corresponding facial area, a short title, and a realistic 0-100% score (based on global data), e.g. "Fine lines & wrinkles — 18%", "Skin texture & elasticity — 72%", "Facial volume & sagging — 35%", "Periocular aging signs — 41%", "Skin tone & pigmentation — 63%". Use a clean, modern sans-serif with small technical-style text, like a scientific facial-analysis UI. At the bottom center, in large bold type, show the final estimated age from the analysis, e.g.: "Estimated age: (a realistic number based on the facial analysis)". Overall style: futuristic AI-guided skincare analysis, minimalist, premium editorial lighting, gender-neutral, works for any face.
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image *(this repo)*

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/nano-banana-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-nano-banana-api"><b>Run Nano Banana →</b></a></sub></p>
