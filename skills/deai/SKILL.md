---
name: deai
description: >-
  Targeted removal of formulaic generative or AI-like writing artifacts while preserving meaning and voice. Use only
  when the user explicitly invokes `deai` or explicitly asks for de-AI, de-slop, humanization, or formulaic-artifact
  cleanup. Do not activate automatically for ordinary drafting, revision, translation, or because prose merely appears
  polished or machine-written.
---

# De-AI

## Purpose

Remove recurring formulaic artifacts that weaken meaning, register, rhythm, terminology, or genre fit. This is an
editing mode, not authorship detection: never infer who wrote the text, report an AI probability, or optimize for a
detector score.

## Calibration

- **Preserve** — Keep facts, claims, evidence, certainty, attribution, terminology, citations, required structure,
  protected material, and supplied voice.
- **Diagnose clusters** — Act on recurring patterns plus a concrete functional weakness. A watched word, punctuation
  mark, sentence length, passive construction, list, or transition is not a defect by itself.
- **Repair the function** — Remove assistant framing, empty rhetoric, mechanical balance, synonym cycling, generic
  padding, or cadence only where it obscures or weakens the actual content.
- **No performance** — Do not inject slang, errors, fragments, jokes, first-person experience, anecdotes, sensory detail,
  random punctuation, or artificial irregularity to make text look human.
- **No fabrication** — Use specificity already supported by the source. Do not invent names, numbers, causes, examples,
  tools, quotations, reactions, or authority.
- **Stop** — Stop when the passage is natural, correct, faithful, and genre-appropriate. Further editing can flatten a
  real voice or create a new formula.

## Language calibration

Load the matching reference for the prose being edited:

- [English](references/english.md)
- [Turkish](references/turkish.md)

For another language, apply only the core calibration unless suitable language-specific guidance exists.

## Simple English

When `simple-english` also applies, preserve its ASD-STE100 terminology and structural constraints. Use `deai` only for
formulaic residue that remains within those constraints; do not reintroduce synonym variation, complex syntax, hedging,
or punctuation merely to make controlled technical prose sound less machine-written.
