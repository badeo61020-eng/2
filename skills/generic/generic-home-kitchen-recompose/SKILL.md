---
name: generic-home-kitchen-recompose
description: Neutral recomposition framework for non-branded home and kitchen product imagery. Use when creating or refining prompts for cookware, storage items, countertop goods, household tools, or other practical products that should feel clean, realistic, and broadly usable without Eimless brand tone or gender-coded styling.
---

# Generic Home Kitchen Recompose

## Overview

Use this skill for home and kitchen products that need a natural indoor context without becoming decorative or editorial.
Prioritize practical readability, believable placement, soft daylight or even interior light, and a tidy lived-in environment with low visual noise.

## Workflow

1. Confirm category fit
- Use this skill for kitchenware, countertop goods, storage items, daily-use tools, and other non-branded household products.
- Do not use it for Eimless assets or fashion-led product scenes.

2. Choose a realistic setting
- Prefer kitchens, dining areas, utility spaces, shelves, or bright neutral interiors that match the product's use.
- Keep the environment clean and simple, not luxury-staged and not personality-heavy.

3. Preserve product truth
- Keep shape, scale, material, color, functional parts, and assembly accurate.
- If editing from a reference image, prefer full-scene regeneration wording over pasted-background wording.

4. Control light and clutter
- Use soft natural light or soft interior light.
- Keep reflections, gloss, and shadows controlled.
- Remove unnecessary props, text, and busy patterns unless they support product understanding.

## Default Prompt Pattern

```text
Create a neutral home or kitchen product image for a non-branded EC listing.
Keep the product shape, scale, materials, and functional details accurate.

Place the product in a clean, realistic indoor setting that matches how it is normally used, such as a bright kitchen, dining area, countertop, shelf, or utility space.
Use soft daylight or even interior lighting with realistic contact shadows and restrained highlights.
Keep the scene tidy, practical, and low-noise, with the product as the clear focal point.

Do not add brand storytelling, editorial drama, or gender-coded styling.
Do not change the product design, material identity, or operating parts.
```

## Default Negative Terms

```text
fashion styling, editorial scene, luxury staging, masculine brand mood, feminine brand mood,
cluttered countertop, distracting props, visible text, busy pattern background,
distorted proportions, changed product structure, fake materials, fake wood grain,
harsh glare, blown highlights, dirty kitchen, unrealistic lighting, cutout look
```

## Default Scene Rules

Unless the user asks otherwise:
- use a neutral indoor environment
- keep the product centered or clearly dominant
- avoid strong lifestyle storytelling
- avoid excessive warmth, color cast, or dramatic shadows
- favor product understanding over atmosphere

## Escalation Rules

- If the item should be shown on pure white, route toward white-background treatment instead.
- If the request starts leaning into a brand world or fashion direction, leave this skill and route appropriately.
