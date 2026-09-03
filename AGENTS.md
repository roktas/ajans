# Repository Instructions

## Skill design

- Keep skills compact, direct, and useful to a competent human as well as an agent.
- Keep guidance that applies whenever a skill is active in `SKILL.md`. Use `references/` for conditional detail that
  benefits from progressive disclosure, including language-, framework-, or task-specific calibration.
- Keep always-applicable style guidance in the owning `SKILL.md`; do not hide core style behind a reference.
- Prefer delegation when a strong external skill already owns a domain and can be used directly. When Ajans intentionally
  adapts or vendors external guidance for portability or a different local contract, keep the adaptation focused,
  preserve required attribution and license notices, and document the upstream source in `README.md`.

## Skill boundaries

- Give each skill one coherent domain, judgment surface, or behavior with a clear activation boundary.
- Cross-cutting skills are appropriate when they materially change agent behavior and remain focused, such as writing,
  de-AI editing, testing, or interactive decision stress-testing.
- Keep language and domain specialists focused on domain-specific judgment. Do not mirror generic sections for debugging,
  compatibility review, minimal changes, cleanup, verification, simplification, polishing, or writing modes merely
  because those activities can occur in the domain.
- When a domain has unique guidance for a cross-cutting concern, place only the domain-specific distinction under its
  natural subject heading instead of recreating the general skill or workflow.

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

## Changes

- Preserve existing guidance unless the requested design change makes it obsolete or contradictory.
- Prefer the smallest structure that keeps important guidance visible. Do not add indirection, references, or coordination machinery without a concrete attention or context-loading benefit.
