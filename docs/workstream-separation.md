# Workstream Separation

## Decision

Keep image editing work and LP prompt authoring in the same repository.

Do not split into a separate repository unless one of these becomes true:

- access control must differ
- release cadence becomes independent
- tooling dependencies diverge substantially
- prompt instructions and editing instructions begin to conflict often

## Why This Works In One Repo

The repository already separates reusable prompts, skills, references, and agent instructions.
The missing boundary is not repository-level. It is workstream-level.

Use two axes at the same time:

- domain: `eimless` or `generic`
- work type: `image-edit` or `lp-prompt`

This prevents prompt-writing requests from being mixed with direct image recomposition requests.

## Recommended Structure

```text
agents/
  root/
  image-edit/
    AGENTS.md
  lp-prompt/
    AGENTS.md
  prompts/
    AGENTS.md
    eimless/
    generic/

docs/
  naming-conventions.md
  workstream-separation.md

prompts/
  eimless/
    lp-sections/
    lp-hero/
    lp-gallery/
  generic/
    lp-sections/
    lp-hero/
    lp-gallery/
  amazon/
  meta-ad/
  natural-background-recompose/
  ...

references/
  lp-layout/
  lp-copy/
  product-notes/
  image-direction/

skills/
  eimless/
  generic/
  shared/
```

## Operating Model

### 1. Image Edit Work

Use this when the user wants the model to transform or regenerate an image asset itself.

Examples:

- remove or replace background
- clean white background
- recomposite product into a new scene
- adjust pose, angle, or lighting while keeping the source asset role

Primary outputs:

- image-generation prompts
- editing instructions
- asset-specific prompt variants

Preferred homes:

- reusable prompt family: `prompts/...`
- reusable references: `references/image-direction/...`
- workstream rules: `agents/image-edit/AGENTS.md`

### 2. LP Prompt Work

Use this when the user wants prompts that help build a landing page visual using one or more completed images.

Examples:

- create a hero visual prompt using three supplied product images
- define section-by-section prompt sets for LP composition
- write prompts for benefit blocks, comparison blocks, CTA area, or gallery sequencing
- translate source image attributes into LP-ready visual direction

Primary outputs:

- section-level prompt documents
- LP composition templates
- multi-image direction prompts
- visual planning notes tied to LP structure

Preferred homes:

- reusable prompt assets: `prompts/<domain>/lp-sections/...`
- LP references and layout notes: `references/lp-layout/...`
- workstream rules: `agents/lp-prompt/AGENTS.md`

## Routing Rule

Use this order when deciding where new work belongs:

1. Determine domain: `eimless` or `generic`
2. Determine work type: `image-edit` or `lp-prompt`
3. Save the output in the matching path

Examples:

- Eimless product cutout cleanup -> `image-edit`
- Eimless LP hero prompt using multiple finished assets -> `lp-prompt`
- Generic kitchen product scene recomposition -> `image-edit`
- Generic household LP comparison section prompt -> `lp-prompt`

## Naming Guidance For LP Prompt Files

Use filenames that encode LP role, not just image style.

Suggested pattern:

```text
lp-<section>_<subject>_<variant>.md
```

Examples:

- `lp-hero_slim-wallet_dual-angle.md`
- `lp-benefit-card_waterproof-zipper_detail-focus.md`
- `lp-cta_family-pouch_soft-neutral.md`

## When To Split Into Another Repo Later

Split only if the repository starts serving two teams with different review rules or if the prompt library for LP work becomes large enough that the shared references no longer help.

Until then, one repository with stronger routing rules is simpler and safer than two half-overlapping repositories.
