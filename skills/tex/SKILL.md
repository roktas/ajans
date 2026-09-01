---
name: tex
description: >-
  TeX-family judgment for source and generated artifacts, engines, document classes, packages, macros, bibliography,
  build convergence, diagnostics, and rendered output. Use only when producing or materially revising substantive
  TeX-family source whose TeX behavior matters. Do not activate for routine technical Q&A, repository browsing, read-only
  inspection, compiler or tool use, file types, fenced examples, rendered PDFs, project labels, or incidental TeX
  mentions.
---

# TeX

## Naming

Apply the general `naming` skill before creating, renaming, or proposing TeX names or durable paths.

- **Scheme** — Follow the document or package's established schemes for commands, environments, counters, labels,
  citation keys, and other named TeX entities.
- **Contracts** — Treat labels, citation keys, public commands, and environments as cross-reference or API contracts when
  they have consumers; do not rename them merely for stylistic consistency.
- **Syntax** — Respect TeX tokenization and control-sequence syntax rather than forcing a general punctuation or
  word-separator style onto command names.

## Style

These are core TeX source defaults when no stronger repository or publication rule settles the decision.

- **Simplicity** — Prefer publication-quality source with simple structure. Avoid macro layers, package additions, and
  layout overrides that do not earn their complexity.
- **Indent** — Indent nested TeX source with 2 spaces when the project has no established source-format convention.
- **Language** — Keep TeX comments, control-sequence names, labels, and file names in English unless the project or
  publication convention requires another language.
- **Comments** — Keep source self-explanatory. Do not add comments that merely repeat source, compensate for poor naming,
  narrate a code change, preserve commented-out code, or state the obvious. Preserve comments when they intentionally
  control whitespace, token joining, generated output, or tool directives.

## Source and environment

- **Authoritative source** — Distinguish source from generated `.aux`, `.bbl`, `.bcf`, `.blg`, `.fls`, `.log`, `.out`,
  `.run.xml`, `.synctex.gz`, `.toc`, and rendered outputs. Do not edit an intermediate artifact as if it were source.
- **Format** — Identify the actual TeX format before applying format-specific rules. Do not apply LaTeX class, package,
  or `latexmk` assumptions to ConTeXt or plain TeX; preserve the project's format and toolchain.
- **Environment** — Inspect the main document, included sources, engine directives, build entry points, CI, class or
  format setup, publisher template, package or module set, bibliography backend, fonts, language system, and supported
  TeX distribution before changing TeX behavior.
- **Engine** — Preserve an existing project's engine and publication environment unless the task changes them. For a new
  unconstrained Unicode LaTeX document, prefer LuaLaTeX when available; do not assume the current machine's engine exists
  in the target publication environment.
- **Contracts** — Treat public commands, environments, counters, labels, citation keys, auxiliary-file formats, class or
  format options, and package or module options as possible contracts. Trace definitions and uses before changing
  signatures or expansion. When compatibility is material, distinguish source compatibility, build or toolchain
  compatibility, and rendered-output stability.

## TeX mechanics

- **Expansion** — Respect tokenization, grouping, category codes, expansion order, optional arguments, moving arguments,
  fragile content, and mode changes where they affect the result. Do not infer macro behavior from a rendered symptom
  alone.
- **Whitespace** — Preserve comments and line endings when they control whitespace, token joining, paragraph breaks,
  generated output, or tool directives; do not assume every source line break is semantic.
- **Fonts** — Keep language and font configuration compatible with the selected engine. In LaTeX, use `fontspec` only
  with XeLaTeX or LuaLaTeX. For pdfLaTeX, distinguish input encoding from output font encoding: modern UTF-8 input
  defaults remove the usual need for `inputenc`, but an appropriate font encoding, commonly T1 for Latin-script text,
  remains a separate decision.
- **Languages** — In LaTeX, keep the project's established `babel` or `polyglossia` system unless changing it is part of
  the task. Do not replace packages or the engine merely as incidental cleanup.

## Build and rendering

- **Entry point** — Use the configured build entry point rather than assembling an ad hoc command when the project
  already defines one. For ConTeXt LMTX, preserve the project's `context` or `mtxrun` entrypoint rather than translating
  the build into LaTeX tooling.
- **Convergence** — Run enough passes for references, tables of contents, indices, glossaries, and bibliography data to
  converge; prefer a dependency-aware driver such as the project's configured `latexmk` workflow when present.
- **Diagnostics** — Read the first causal error and relevant surrounding log context. Distinguish a source defect from
  stale auxiliary state before deleting or regenerating build products, and trace macro definitions, grouping,
  expansion, counters, labels, and generated files when the visible symptom is downstream of the cause.
- **Warnings** — Inspect warnings made relevant by the change, including unresolved references or citations, multiply
  defined labels, missing glyphs, overfull or underfull boxes, font substitution, and rerun requests. Do not suppress
  warnings globally to hide a local defect.
- **Rendered output** — When perception matters, inspect the affected rendered pages at the intended size and medium. A
  successful compiler exit does not establish correct line breaking, glyph coverage, pagination, float placement, or
  bibliography output.

## References and floats

- **Cross-references** — Preserve meaningful labels, equation and theorem numbering, and downstream references when they
  are part of the document contract.
- **Bibliography** — Preserve citation keys, locators, attribution, bibliography semantics, and the configured backend.
  Do not repair a citation or claim by changing its evidence without source authority.
- **Floats** — Check figure and table captions, numbering, references, and placement together with the surrounding text;
  prefer source-level causes over broad spacing overrides that merely move a layout defect elsewhere.
