---
name: generic-white-background-cleanup
description: Neutral cleanup rules for white-background EC product imagery. Use when creating or refining prompts that place non-branded products on a clean white background while preserving shape, material accuracy, edge quality, and controlled reflections without importing Eimless styling.
---

# Generic White Background Cleanup

## Overview

Use this skill for standard EC product imagery on a white or near-white background.
Prioritize product accuracy, clean edges, controlled shadows, and realistic material rendering over stylization.

## Workflow

1. Confirm white-background intent
- Use this skill when the product should sit on a plain white or near-white listing background.
- Prefer this skill for catalog-style outputs, marketplace thumbnails, and simple product cut-cleanup work.

2. Preserve the product exactly
- Keep the product's shape, proportions, silhouette, color, materials, and functional parts accurate.
- If the source image is messy, rewrite toward a clean studio recapture rather than a rough cutout.

3. Control the white-background finish
- Use a pure white or very slightly off-white background.
- Add soft grounding shadow only if needed for realism.
- Keep edges crisp but natural, without halo or sticker-like cutout artifacts.

4. Control reflections and cleanup
- Remove dirt, smudges, dust, obvious scratches, and distracting glare when they are not part of the product design.
- Keep reflections soft and readable, not mirror-like and not blown out.

## Default Prompt Pattern

```text
Create a clean white-background EC product image for a non-branded item.
Keep the product shape, proportions, materials, colors, and functional details accurate.

Place the product on a pure white or near-white background with a natural, minimal grounding shadow.
Render the product with clean but natural edges, controlled highlights, realistic materials, and no cutout look.
Remove distracting dust, smudges, minor scratches, and unwanted glare while preserving the true product finish.

Do not add props, text, lifestyle context, or brand-world styling.
Do not redesign the product or exaggerate luxury cues.
```

## Default Negative Terms

```text
cutout look, pasted object, halo edge, hard matte edge,
distorted silhouette, changed proportions, changed color, fake materials,
harsh glare, blown highlights, mirror-like reflection, dirty background,
dust emphasized, scratch emphasized, clutter, props, text, lifestyle scene
```

## Default Finish Rules

Unless the user asks otherwise:
- keep the background plain white
- avoid floating-object artificiality
- use restrained contact shadow
- do not add premium styling cues
- keep the output practical for EC listings

## Escalation Rules

- If the product needs a lifestyle room scene, use a contextual recomposition skill instead.
- If the user needs marketplace-specific constraints later, split those rules into a dedicated marketplace skill.
