---
name: tex
description: >-
  TeX-family judgment for source and generated artifacts, engines, document classes, packages, macros, bibliography,
  build convergence, diagnostics, and rendered validation. Use only when producing or materially revising substantive
  TeX-family source whose TeX behavior matters. Do not activate for routine technical Q&A, repository browsing, read-only
  inspection, compiler or tool use, file types, fenced examples, rendered PDFs, project labels, or incidental TeX
  mentions.
---

# TeX

## Naming

Apply the general `naming` skill before creating, renaming, or proposing TeX names or durable paths.

- Follow the document or package's established schemes for commands, environments, counters, labels, citation keys, and
  other named TeX entities.
- Treat labels, citation keys, public commands, and environments as cross-reference or API contracts when they have
  consumers; do not rename them merely for stylistic consistency.
- Respect TeX tokenization and control-sequence syntax rather than forcing a general punctuation or word-separator style
  onto command names.

## Baseline

### Source and constraints

- Identify authoritative source files and distinguish them from generated `.aux`, `.bbl`, `.bcf`, `.blg`, `.fls`,
  `.log`, `.out`, `.run.xml`, `.synctex.gz`, `.toc`, and rendered outputs. Follow the repository's generated-file and
  clean-build policy rather than editing an intermediate artifact as if it were source.
- Inspect the main document, included sources, engine directives, `latexmkrc` or other build entry points, CI, document
  class, publisher template, package set, bibliography backend, fonts, language system, and supported TeX distribution
  before changing TeX behavior.
- Preserve the established engine, class, publisher requirements, bibliography workflow, package stack, and generated
  file policy unless the task explicitly makes one of them a migration surface. A locally installed engine or package
  does not establish the publication environment.
- Treat public commands, environments, counters, labels, citation keys, auxiliary-file formats, class options, and
  package options as possible contracts. Trace definitions and uses before changing their signatures or expansion.

### Source mechanics

- Respect TeX tokenization, grouping, category codes, expansion order, optional arguments, moving arguments, fragile
  content, and mode changes where they affect the task. Do not infer macro behavior from the rendered symptom alone.
- Preserve comments and line endings when they control whitespace, token joining, paragraph breaks, generated output, or
  tool directives. Conversely, do not claim every source line break is semantically significant.
- Follow the repository's TeX source formatting. When no source-format convention exists, indent nested TeX source with
  2 spaces.
- Keep language and font configuration compatible with the selected engine. `fontspec` is for XeLaTeX and LuaLaTeX; do
  not add it to a pdfLaTeX document. LaTeX has used UTF-8 as its default input encoding since the 2018 release, so add
  `inputenc` only for an actual older-kernel or non-default-encoding requirement.
- Keep the project's existing `babel` or `polyglossia` system unless changing it is the task. Package replacement,
  engine migration, and publisher-template modernization are migrations, not incidental cleanup.

### Build and validation

- Use the configured build entry point. Run enough passes for references, tables of contents, indices, glossaries, and
  bibliography data to converge; prefer the project's dependency-aware driver when it has one instead of guessing a
  fixed pass count.
- Read the first causal error and the relevant surrounding log context. Separate fatal errors from warnings, and
  distinguish stale auxiliary state from a source defect before deleting or regenerating build products.
- Inspect warnings made relevant by the change, including unresolved references or citations, multiply defined labels,
  missing glyphs, overfull or underfull boxes, font substitution, and rerun requests. Do not suppress warnings globally
  to conceal a local defect or promise a warning-free build when the established document has unrelated warnings.
- Validate the affected source diff and, when perception is material, the affected rendered pages at the intended size
  and medium. A successful compiler exit does not establish correct wording, hierarchy, line breaking, glyph coverage,
  pagination, or bibliography output.

## Fault diagnosis and correction

Start with the first causal diagnostic under the configured engine and build path. Reduce only when the full project
obscures the cause, retaining the class, packages, engine, auxiliary state, and input conditions needed to reproduce it.
Trace macro definitions, grouping, expansion, modes, counters, labels, and generated files before treating a visible
symptom or later cascade error as the defect.

## Backward compatibility

Check the concrete supported surface: engine and distribution floor, class and package options, public macro and
environment signatures, expansion behavior, counters, labels and citation keys, generated auxiliary formats,
bibliography backend, publisher workflow, and downstream source that imports the document or class. Preserve only real
consumers and requirements; distinguish source compatibility, build compatibility, and rendered-output stability.

## Smallest necessary change

Keep a focused TeX change local to the owning source, definition, configuration, and affected rendered pages when that
fully satisfies the task. Avoid unrelated reflow, package replacement, class or engine migration, global spacing
changes, generated-file churn, and wholesale preamble normalization.

## Affected scope cleanup

After the requested change, inspect the affected TeX surface for obsolete definitions and uses, unused package or class
options, stale labels and references, superseded bibliography entries, dead build inputs, and generated files that the
repository does not retain. Remove only residue made obsolete by the change; do not turn cleanup into a preamble or
typography campaign.

## Scholarly communication

Preserve citation keys, locators, attribution, cross-references, equation and theorem numbering, figure and table
captions, bibliography semantics, and publisher requirements. Check the rendered relationship among references, notes,
floats, and their subjects; do not repair a citation or claim by changing evidence without source authority.

## Local quality refinement

Refine the affected rendered area with the established class, grid, fonts, language support, and package vocabulary.
Judge line and page breaks, spacing, hierarchy, glyph coverage, floats, and neighboring pages together. Prefer local
source-level causes over global negative spacing or broad layout overrides that merely move the defect elsewhere.
