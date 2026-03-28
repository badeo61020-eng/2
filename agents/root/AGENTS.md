# AGENTS.md (Root Scope)

This file covers repository-wide organization rules for `ImageCreate`.

## Repository Structure

This repository contains two asset domains:

- `Eimless`: brand-specific assets for Eimless products and image creation
- `Generic EC`: non-brand-specific assets for miscellaneous products such as home, kitchen, household, and neutral EC items

Do not assume that all requests belong to Eimless.
Do not assume that brand-neutral products should inherit Eimless tone, model defaults, or scene conventions.

## Repository Rules

- Save prompt files under `prompts/`, not at the repository root.
- Save reusable references under `references/`.
- Save scripts and generated catalogs under `tooling/`.
- Save scope instructions under `agents/`.

## Workstream Separation

Treat this repository as containing two different work types:

- `image-edit`: prompts and instructions used to generate, recomposite, clean up, or transform image assets
- `lp-prompt`: prompts and planning assets used to compose LP visuals from one or more finished images

Do not assume that all image-related requests belong to the same skill family just because they involve images.

When a request is about editing or regenerating the visual asset itself, route it as `image-edit`.
When a request is about using one or more images to design LP sections, hero blocks, galleries, benefit areas, or CTA visuals, route it as `lp-prompt`.

## Domain Separation Rule

- Existing legacy prompt and skill assets in this repository are treated as `Eimless-first` unless a newer domain-specific rule overrides them.
- New non-brand-specific assets must be placed under clearly named `generic` directories and must not be mixed into Eimless asset areas.
- Do not reuse Eimless-specific defaults for generic EC product work unless the user explicitly requests that style.

## Prompt Storage

- New prompt files must be stored under the appropriate prompt family directory.
- Prefer domain separation in path names such as `prompts/eimless/...` and `prompts/generic/...` when adding new assets.
- For LP-oriented prompt assets, prefer dedicated paths such as `prompts/eimless/lp-sections/...` and `prompts/generic/lp-sections/...`.
- If no exact scene category exists, place the file in the nearest family directory and refine later.
- Follow `docs/naming-conventions.md` for file naming.

## Migration Rule

- Treat `Metaprompt/` as retired legacy layout.
- Do not place new files in `Metaprompt/`.

## Open File Rule

- When asked to open a file, use VS Code with an absolute file path.
- Prefer `--reuse-window` and `--goto` so the exact target file is focused.
- Clear `ELECTRON_RUN_AS_NODE` before launching VS Code commands.
- After creating or updating a user-facing prompt/document file, open it automatically unless the user explicitly opts out.

## Prompt Writing Rule

- When writing reusable prompt files, do not rely on ambiguous references like `attached image 2` or `second image` if the user wants the prompt itself to be self-contained. Convert those references into explicit written descriptions.
- Keep Eimless-specific worldbuilding, model defaults, and styling inside Eimless-scoped assets only.
- Keep Generic EC prompts neutral unless the user asks for a stronger style direction.
