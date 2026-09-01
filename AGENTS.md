# Repository Instructions

## Skill design

- Keep skills compact, direct, and useful to a competent human as well as an agent.
- Keep core guidance in `SKILL.md`. Use `references/` only for conditional detail that benefits from progressive disclosure.
- Style is always core. Do not move style rules to `references/`; keep them in the owning `SKILL.md`.
- Do not duplicate strong external guidance. When an established external skill owns a domain well, delegate to it and keep only Ekler-specific guidance locally.

## Rule presentation

- Use short semantic leads such as `**Scope**`, `**Contracts**`, or `**Ordering**` when a list contains distinct decision surfaces and the lead makes the relevant rule easier to find.
- Do not add leads mechanically. A clear section or subsection heading already provides the same anchor when all following rules share one decision surface.
- Prefer concrete examples when they materially clarify a rule, especially for naming and other judgment-heavy guidance.

## Repository language

- Describe the current desired state directly. Do not frame ordinary repository guidance in terms of migration history, legacy state, or what content used to be elsewhere.
- Use historical language only when history itself is necessary to understand a compatibility contract, user request, or documented decision.
- Avoid labels such as `legacy`, `old`, `new`, `migrated`, or `migration` when a present-tense description states the rule more clearly.

## Changes

- Preserve existing guidance unless the requested design change makes it obsolete or contradictory.
- Prefer the smallest structure that keeps important guidance visible. Do not add indirection, references, or coordination machinery without a concrete attention or context-loading benefit.
