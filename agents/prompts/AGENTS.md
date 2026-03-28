# AGENTS.md (Prompts Scope)

This file covers work under `prompts/`.

## Domain Routing

Before creating or editing a prompt, classify the request into one of these domains:

- `Eimless`
- `Generic EC`

Use `Eimless` when the request clearly involves:
- the Eimless brand
- existing Eimless products
- men's bags or existing Eimless visual language
- continuity with existing repository prompt families

Use `Generic EC` when the request clearly involves:
- non-branded products
- home and kitchen items
- household goods
- neutral catalog-style product imagery
- products that should not feel specifically masculine or feminine
- low-character, descriptive EC imagery

If the request is ambiguous, do not silently default to Eimless branding assumptions.

## Work Type Routing

Before choosing a prompt family, classify the request into one of these work types:

- `image-edit`
- `lp-prompt`

Use `image-edit` when the prompt is meant to alter, regenerate, clean up, or recomposite an image asset itself.

Use `lp-prompt` when the prompt is meant to build an LP visual or a section-level LP composition from one or more finished images.

Do not route LP composition requests into image-edit families just because the inputs are images.
Do not route direct asset cleanup or recomposition requests into LP folders just because the output will later be used on a landing page.

## Available Skills

Existing skills in this repository should be treated as Eimless-oriented unless a dedicated Generic skill is added later.

Shared utility skills may be used across both domains when they do not inject brand-specific assumptions:
- image-request-terminology
- prompt-architect
- prompt-improver
- image-batch-convert

Do not use Eimless-specific metaprompt skills for Generic EC requests unless the user explicitly asks for that aesthetic.

## Storage Rules

- Save new prompt files under `prompts/<domain>/<family>/...` where possible.
- Save LP composition prompt files under dedicated LP families such as `prompts/<domain>/lp-sections/...` when applicable.
- Do not store new prompt files under `Metaprompt/`.
- Keep references out of `prompts/`; put them under `references/`.
- Keep scripts out of `prompts/`; put them under `tooling/`.

## Naming Rules

- Follow `docs/naming-conventions.md`.
- Keep the family name in the filename when it improves searchability.
- Prefix or path-separate Generic EC prompts clearly so they do not get confused with Eimless assets.

## Prompt File Format

Use this minimum structure unless the family already follows a different stable format:

1. `# <Title>`
2. `## Prompt`
3. `## Negative Prompt`

## Separation Rules

- Do not mix Eimless brand tone into Generic EC prompts.
- Do not mix Generic neutral catalog tone into Eimless prompts when brand direction matters.
- Do not carry over Eimless model defaults, urban scenes, or bag-specific styling into Generic product prompts.
- Keep Generic prompts neutral, clean, descriptive, and broadly reusable unless the user requests a stronger scene concept.
- Do not mix LP layout planning prompts with direct image-edit prompt families when they serve different work types.

## Working Notes

- If a prompt family grows too large, add or refine subdirectories before adding more files.
- Prefer family-level `README.md` files for discovery instead of putting operational notes next to prompt assets.
- After creating or updating a prompt file for the user, open that file in VS Code by default unless the user explicitly says not to.
- When the user asks to open a prompt file, open it in VS Code with an absolute path and `--goto`.
- Before launching VS Code, clear `ELECTRON_RUN_AS_NODE` and prefer reusing the existing workspace window.
- In prompt text, avoid vague attachment-dependent phrases such as `attached image 2`, `second attachment`, or similar shorthand when the user wants the content to stand alone. Replace them with explicit visual descriptions of the intended look, angle, motion, material, or lighting.
