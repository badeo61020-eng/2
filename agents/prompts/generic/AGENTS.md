# AGENTS.md (Prompts Scope: Generic EC)

This file covers Generic EC prompt work.

## Scope

Use this scope for:
- non-branded products
- home and kitchen items
- household goods
- neutral miscellaneous EC items
- products that should not read as specifically masculine or feminine
- low-character, descriptive product imagery

## Core Rule

Generic EC prompts must stay neutral.
Do not import Eimless-specific brand tone, men's bag assumptions, model defaults, or scene conventions unless the user explicitly requests them.

## Prompt Direction

Prioritize:
- clarity
- cleanliness
- broad EC usability
- neutral styling
- simple material readability
- controlled lighting
- low-noise background treatment

Avoid:
- unnecessary personality
- brand-world storytelling
- gender-coded styling unless requested
- overly fashion-oriented composition for ordinary household products

## Skill Preference

Use only Generic-safe or shared skills for Generic EC work.

Prefer these Generic skills when they match the request:
- `generic-ec-product-metaprompt` for neutral non-branded EC product imagery
- `generic-home-kitchen-recompose` for home, kitchen, and household scene recomposition
- `generic-white-background-cleanup` for plain white-background product cleanup or regeneration

Shared utility skills may be used:
- image-request-terminology
- prompt-architect
- prompt-improver
- image-batch-convert

If a Generic-specific skill family is added later, prefer that over Eimless-oriented skills.

## Storage Rule

Save Generic EC prompts under `prompts/generic/...`.

Suggested family examples:
- `prompts/generic/ec-product/`
- `prompts/generic/home-kitchen/`
- `prompts/generic/white-background/`
- `prompts/generic/lifestyle-light/`

## Default Tone

Unless the user asks otherwise:
- no model
- no brand storytelling
- neutral interior or clean white-background context
- practical EC readability over mood
- soft controlled reflections
- realistic product proportions
- tidy, non-cluttered composition
