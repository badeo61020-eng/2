---
name: generic-ec-product-metaprompt
description: Neutral metaprompt framework for non-branded EC product imagery. Use when creating or refining prompts for miscellaneous products, household goods, home and kitchen items, or other items that should not inherit Eimless brand tone, men's bag assumptions, or gender-coded styling.
---

# Generic EC Product Metaprompt

## Overview

Use this skill for EC product imagery that should stay neutral, descriptive, and broadly reusable.
Prioritize clean presentation, readable materials, controlled lighting, and low-character composition over brand-world storytelling.

## Workflow

1. Classify the request
- Confirm the product is not being treated as an Eimless asset.
- Use this skill for non-branded items, home and kitchen goods, household products, and miscellaneous EC items that should not read as specifically masculine or feminine.

2. Fix the visual direction
- Keep the output neutral unless the user asks for a stronger style.
- Prefer no model, no narrative, no fashion-coded scene language, and no brand-specific worldbuilding.

3. Build the prompt around product readability
- Preserve the product's shape, proportions, material identity, and functional parts.
- State the background, light quality, reflection control, and cleanup requirements explicitly.
- For image editing, prefer full-scene regeneration wording over simple pasted-background wording.

4. Add failure prevention
- Block shape drift, over-stylization, clutter, harsh reflections, and mismatched lighting.
- If the product is utilitarian, keep the composition practical and explanation-friendly.

## Default Prompt Pattern

Use and adapt the block below:

```text
Create a neutral EC product image for a non-branded item.
Keep the product shape, proportions, materials, and functional details accurate.
Prioritize a clean, descriptive presentation suitable for a general online store listing.

Background: simple, bright, uncluttered, and non-distracting.
Lighting: soft, even, controlled lighting with realistic shadows and restrained highlights.
Styling: neutral, non-gendered, non-fashion-led, and not tied to any brand world.
Output: photoreal, tidy, easy to understand at a glance, with the product as the clear focal point.

Do not introduce unnecessary personality, luxury signaling, or editorial drama.
Do not change the product design or add extra accessories unless requested.
```

## Default Negative Terms

Use and adapt as needed:

```text
brand-specific styling, masculine fashion mood, feminine fashion mood,
editorial storytelling, cluttered scene, distracting props, excessive luxury cues,
distorted proportions, changed product structure, fake materials,
harsh glare, blown highlights, mirror-like reflection, dirty background,
cutout look, pasted object, mismatch lighting, mismatch sharpness
```

## Generic EC Defaults

Unless the user says otherwise:
- do not add a model
- do not imply a specific gender target
- do not imply a specific brand identity
- use clean white or light neutral backgrounds, or a simple indoor setting
- keep reflections controlled and practical
- optimize for EC readability first, mood second

## Escalation Rules

- If the user explicitly wants Eimless continuity, stop using this skill and route to the Eimless side.
- If the product needs a category-specific treatment later, create a dedicated Generic sub-skill instead of overloading this one.
