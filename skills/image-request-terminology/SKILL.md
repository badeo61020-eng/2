---
name: image-request-terminology
description: Translate vague Japanese image-generation and image-editing requests into practical prompt language. Use when the user does not know professional terms for composition, lighting, tone, materials, background replacement, model posing, or negative prompts, and needs help turning plain Japanese requests into reusable image instructions.
---

# Image Request Terminology

Use this skill to turn everyday Japanese requests like `高級感を出したい`, `自然にしたい`, `プロっぽくしたい`, or `背景を変えたい` into concrete prompt wording.

Read [references/terms-ja.md](references/terms-ja.md) when you need term mappings or a request template.

## Workflow

1. Identify the user's vague words.
   - Example: `高級感`, `自然`, `おしゃれ`, `なじませたい`
2. Map them to concrete image terms.
   - composition
   - lighting
   - tone
   - material
   - pose
   - negatives
3. Rewrite the request in practical prompt language.
4. If useful, explain the terms briefly in Japanese.
5. Prefer short, reusable wording over theory-heavy explanations.

## Output Shape

When the user asks for wording help, prefer this format:

1. Short explanation of what the vague word means in image terms
2. 2 to 5 practical replacement phrases
3. A ready-to-use rewritten prompt block

## Core Rules

1. Prefer concrete visual language over abstract praise words.
2. Translate user intent, not literally every word.
3. Keep Japanese output natural and usable as-is.
4. When the user is writing an image request, include both positive instructions and failure-prevention wording if needed.
5. If the request is about product imagery, prioritize:
   - shape retention
   - material consistency
   - lighting control
   - background integration
   - dust / scratch cleanup when relevant

## Typical Conversions

- `高級感`
  - Translate into low saturation, elegant shading, controlled highlights, clean material finish.
- `自然に`
  - Translate into realistic anatomy, realistic lighting, no cutout look, no forced pose.
- `背景だけ変えたい`
  - Translate into full-scene regeneration language, not simple background replacement.
- `黒すぎる`
  - Translate into charcoal, dark gray, slightly brighter than the bag, preserve tonal separation.
- `素材感を合わせたい`
  - Translate into grain, highlight behavior, roughness, edge hardness, surface uniformity.

## Reference

- Use [references/terms-ja.md](references/terms-ja.md) for concrete vocabulary, negative terms, and a reusable Japanese request template.
