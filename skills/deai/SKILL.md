---
name: deai
description: >-
  Targeted review or removal of formulaic generative or AI-like writing artifacts while preserving meaning and voice.
  Use only when the user explicitly invokes `deai`, explicitly asks for de-AI, de-slop, humanization, or formulaic-
  artifact cleanup, or a more-specific project workflow explicitly requires such a pass. Do not activate automatically
  for ordinary drafting, revision, translation, or because prose merely appears polished or machine-written.
---

# De-AI

Remove recurring formulaic habits that weaken meaning, register, rhythm, terminology, structure, or genre fit. This is
an editing and review skill, not authorship detection: never infer who wrote the text or report an AI probability.

## Authority

Apply these constraints in order:

1. The user's current request and explicit preservation constraints.
2. Project, publication, genre, language, and supplied-voice requirements.
3. The source's facts, claims, evidence, certainty, attribution, terminology, citations, and protected material.
4. The language-specific calibration loaded below.

A de-AI pass does not authorize substantive claim changes merely because wording looks formulaic. Never invent a fact,
source, name, number, example, anecdote, opinion, reaction, first-person experience, quotation, or biographical detail to
make prose seem human.

## Method

1. Read the complete editable passage and any relevant source or voice sample.
2. Establish the genre, audience, register, language, protected material, and whether the task is review-only or editing.
3. Load the matching language reference completely when one is available.
4. Find recurring pattern clusters and identify the concrete weakness they create. A watched word, punctuation mark,
   sentence shape, or formatting choice alone is not enough.
5. For a substantial English rewrite, several cluster types, or a plausible false positive, also read
   [English examples](references/english-examples.md) before editing.
6. Repair the underlying weakness with the smallest coherent edit. Preserve useful irregularity and intentional form.
7. Audit the revision for lost meaning, changed claim strength, fabricated detail, flattened voice, regenerated
   scaffolding, unstable terminology, and remaining clusters.
8. Stop when the prose is natural, correct, faithful, and genre-appropriate. More editing can create a new formula.

## Calibration

- **Signals, not bans** — Treat recurring forms as diagnostic evidence, not forbidden vocabulary or punctuation. Look for
  repetition plus functional weakness.
- **Repair the problem** — Remove empty inflation, assistant framing, vague analysis, mechanical balance, generic
  transitions, synonym cycling, performed register, or diff narration only when they weaken the actual text.
- **Preserve claims** — Deflating promotional or formulaic wording does not authorize deleting its underlying assertion.
  Restate the claim directly and at the same strength unless substantive editing is explicitly in scope and the supplied
  evidence supports changing it.
- **Preserve attribution** — The absence of supporting evidence from an excerpt does not prove a claim or attribution is
  unsupported. Do not silently turn `experts argue` into the narrator's assertion, invent named experts, or delete the
  claim merely to make the prose cleaner.
- **Preserve voice** — Keep supplied cadence, deliberate repetition, justified asymmetry, useful asides, functional
  formality, and genre-native constructions. Do not replace a real voice with generic plain prose.
- **No performed humanity** — Do not inject slang, typos, fragments, jokes, first-person participation, sensory detail,
  random punctuation, artificial sentence-length variance, or deliberate imperfection.

## Language calibration

Load the matching reference for the prose being reviewed or edited:

- [English](references/english.md)
- [Turkish](references/turkish.md)

Do not translate one language's watch list into another. For other languages, apply only the core calibration unless
suitable language-specific guidance exists.

## Simple English

When `simple-english` also applies, preserve its ASD-STE100 terminology and structural constraints. Use `deai` only for
formulaic residue that remains within those constraints; do not reintroduce synonym variation, complex syntax, hedging,
or punctuation merely to make controlled technical prose sound less machine-written.

## Output

For review-only work, report concrete recurring clusters, their effects, and important false positives without rewriting
unless requested. For editing, return the requested revised artifact or format. If no meaningful cluster exists, leave
the prose unchanged rather than editing for activity's sake.
