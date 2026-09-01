# Repository Instructions

## Skill design

- Keep skills compact, direct, and useful to a competent human as well as an agent.
- Keep core guidance in `SKILL.md`. Use `references/` only for conditional detail that benefits from progressive disclosure.
- Style is always core. Do not move style rules to `references/`; keep them in the owning `SKILL.md`.
- Do not duplicate strong external guidance. When an established external skill owns a domain well, delegate to it and keep only Ekler-specific guidance locally.

## Specialist boundaries

- Keep specialist skills focused on domain-specific judgment, not generic task modes or workflow controls.
- Do not mirror generic sections for debugging, compatibility review, minimal changes, cleanup, verification, simplification, polishing, or writing modes merely because those activities can occur in the domain.
- When a domain has unique guidance for one of those decisions, place only the domain-specific distinction under its natural subject heading instead of creating a generic workflow section.

## Bash maintenance

- Treat the established Bash guidance, working conventions, examples, and template code as a maintenance constraint rather than ordinary rewrite material.
- Preserve substantive Bash guidance, conventions, examples, and especially template code unless a concrete reason requires change.
- Do not opportunistically refactor, reformat, restyle, modernize, shorten, normalize, or replace Bash template code during unrelated work or routine maintenance.
- Do not remove a Bash convention merely because it looks personal or differs from another specialist; first determine whether it encodes deliberate Bash working practice.
- Keep metadata, packaging, activation, and other structural changes separate from substantive Bash rewriting when possible.
- When an explicit defect, unsafe pattern, stale fact, or clear contract conflict requires correction, make the smallest necessary change and preserve the surrounding established form.
- Treat broad cleanup of the Bash skill as out of scope unless the user explicitly requests it.

## Rule presentation

- Use short semantic leads such as `**Scope**`, `**Contracts**`, or `**Ordering**` when a list contains distinct decision surfaces and the lead makes the relevant rule easier to find.
- Do not add leads mechanically. A clear section or subsection heading already provides the same anchor when all following rules share one decision surface.
- Prefer concrete examples when they materially clarify a rule, especially for naming and other judgment-heavy guidance.

## Document transfer

- When asked to transfer, incorporate, or carry content into another document, transfer the substance rather than source-navigation artifacts.
- Do not add or preserve URLs, hyperlinks, source links, or similar references in the target document unless the user explicitly asks for them or the target document requires them as part of its contract.

## Repository language

- Describe the current desired state directly. Do not frame ordinary repository guidance in terms of migration history, legacy state, or what content used to be elsewhere.
- Use historical language only when history itself is necessary to understand a compatibility contract, user request, or documented decision.
- Avoid labels such as `legacy`, `old`, `new`, `migrated`, or `migration` when a present-tense description states the rule more clearly.

## Changes

- Preserve existing guidance unless the requested design change makes it obsolete or contradictory.
- Prefer the smallest structure that keeps important guidance visible. Do not add indirection, references, or coordination machinery without a concrete attention or context-loading benefit.
