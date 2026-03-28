---
name: curtain-rail-end-cap-nanobanana
description: Nano Banana Proでカーテンレール端部のエンドキャップを追加・差し替え・反転・嵌合補正するときの専用スキル。端部への自然な嵌合、参考画像の背面/側面統合、サイズ補正、向き修正が必要なときに使う。
---

# Curtain Rail End Cap Nano Banana

## Overview

Use this skill when editing a curtain rail end cap in Nano Banana Pro.
The goal is to keep the rail body unchanged while making the end cap look naturally inserted, fitted, and aligned with the rail opening.

This skill is for cases such as:
- adding an end cap to an open rail end
- replacing the current end cap with a referenced part
- correcting the direction of the end cap
- increasing the size so the end cap fits into the rail opening
- merging back-view and side-view references into one consistent part

## Workflow

1. Classify the request
- Identify whether the task is `add`, `replace`, `reverse direction`, `insert deeper`, or `shape correction`.
- Confirm the rail itself should remain unchanged unless the user explicitly asks otherwise.

2. Lock the rail-side constraints
- Keep the curtain rail body, curve, material, background, and composition unchanged.
- Limit edits to the end-cap area unless the user asks for a wider correction.

3. Define the fitting behavior
- Explicitly state that the end cap must be inserted into the rail opening, not pasted onto the outside.
- Require the size to match the rail cross-section.
- Require close contact, no visible gap, and natural depth at the joint.

4. Merge reference angles when needed
- If the user provides multiple references, assign each one a role such as back view, side view, or shape reference.
- Instruct the model to reconstruct one consistent 3D part, not to paste a flat view directly.

5. Add failure prevention
- Block floating parts, shallow insertion, wrong scale, wrong direction, pasted-object look, halo edges, and rail deformation.
- If the user asks for reversal only, preserve size and fitting state while changing direction only.

## Prompt Building Rules

- Use Japanese output by default when the user is preparing a Nano Banana Pro instruction.
- Prefer direct edit wording such as `修正してください`, `差し替えてください`, `嵌合した状態にしてください`.
- Use `嵌合`, `開口断面`, `内側へ差し込まれた状態`, and `一体化して見える` when the user wants a true fitted connection.
- If the user mentions a specific reference role, state it explicitly:
  - `図2は背面形状の参考`
  - `図3は側面形状の参考`
- If the generated result already has the correct direction, say so and only request size / insertion fixes.
- If the generated result already has the correct shape, say so and only request direction reversal.

## Default Structure

Build the response in this order:

1. Short purpose
2. Main prompt
3. Optional reinforcement sentence
4. Negative prompt

## Reusable Phrases

Use and adapt these phrases:

```text
エンドキャップはレール端部の外側に付けるのではなく、開口断面の内側へ差し込まれて断面にぴったり嵌合し、端部と一体化して見える状態にしてください。
```

```text
参考画像をそのまま平面的に貼るのではなく、レール端部の現在のパースに従って自然な角度で装着してください。
```

```text
カーテンレール本体の形状、曲線、材質、色、背景、構図は変更しないでください。
修正対象は端部のエンドキャップ部分のみです。
```

## Related Prompt Files

Prefer reusing or adapting these existing prompt files before writing a new prompt from scratch:

- `prompts/generic/ec-product/curtain-rail-end-cap-edit-prompt-ja.md`
- `prompts/generic/ec-product/curtain-rail-end-cap-angle-fix-nanobanana-ja.md`
- `prompts/generic/ec-product/curtain-rail-end-cap-insert-fix-nanobanana-ja.md`
- `prompts/generic/ec-product/curtain-rail-end-cap-deeper-insert-fix-ja.md`
- `prompts/generic/ec-product/curtain-rail-end-cap-reference-insert-nanobanana-ja.md`
- `prompts/generic/ec-product/curtain-rail-end-cap-replace-reference-nanobanana-ja.md`
- `prompts/generic/ec-product/curtain-rail-end-cap-reverse-direction-nanobanana-ja.md`

## Escalation Rules

- If the user wants a prompt family to be reused repeatedly, create or update a dedicated Markdown prompt file under `prompts/generic/ec-product`.
- If the user asks to make it a reusable workflow, keep the logic in this skill and keep the user-facing output as Markdown.
- If the user asks to show the created Markdown on Windows, save it first and then open the exact file if permissions allow.
