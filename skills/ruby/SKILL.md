---
name: ruby
description: >-
  Ruby implementation judgment for modern syntax, design, style, public APIs, gems and loading, Bundler, tests, typing,
  visibility, and YARD. Use only when producing or materially revising substantive Ruby code. Do not activate for routine
  technical Q&A, repository browsing, read-only inspection, Ruby tool use, file types, fenced examples, project labels,
  or incidental Ruby mentions.
---

# Ruby

## Naming

Apply the general `naming` skill before creating, renaming, or proposing Ruby names or durable paths.

- **Case** — Use `snake_case` for methods, local variables, and symbols; use `CamelCase` for classes and modules.
- **Predicates** — Use `?` for predicate methods. Use `!` when it distinguishes a materially more dangerous or surprising
  variant from a non-bang counterpart, or when an established API convention requires it; mutation alone does not require
  a bang suffix.
- **Contracts** — Preserve public method names, keyword names, constants, and serialized or reflective names unless
  changing that surface is in scope.

## Style

These are core Ruby working defaults. Explicit repository rules, configured formatters, and established local conventions
refine them and override them only for a concrete conflict.

- **Simplicity** — Prefer simple Ruby over clever Ruby. Favor direct language features over metaprogramming or indirection
  that does not earn its cost.
- **Formatting** — Use the formatter already configured by the repository. When none is configured, follow surrounding
  style and do not introduce a formatter incidentally. Do not hand-align code against formatter output.
- **Strings** — Use double quotes for strings by default.
- **Expression methods** — Use `def foo = ...` for a simple expression method when the supported Ruby range permits it
  and the form improves clarity.
- **Member order** — When no stronger local order exists, use:
  1. `include`/`extend`
  2. constants, alphabetically
  3. `attr_*`, alphabetically
  4. `initialize`
  5. public methods, alphabetically
  6. private methods, alphabetically
- **Ordering** — Alphabetize arrays, hashes, assignments, and methods only when order is semantically irrelevant and no
  surrounding convention requires another order.
- **Comments** — Keep code self-documenting. Do not add comments that merely repeat code, compensate for poor naming,
  narrate a code change, preserve commented-out code, or state the obvious. Comment non-obvious intent, constraints, or
  behavior that the code cannot express clearly itself.

Do not reorder or reformat unrelated Ruby merely because this skill is active.

## Runtime and contracts

- **Support floor** — Resolve the supported Ruby range from repository evidence such as `.ruby-version`, version-manager
  files, the gemspec's `required_ruby_version`, lockfiles, CI, and project rules. The installed interpreter describes the
  current machine, not the compatibility floor.
- **Default modernity** — When no version evidence exists, prefer modern idiomatic Ruby and do not invent compatibility
  constraints. State a version assumption only when it can materially change the design or result.
- **Public surface** — Treat positional and keyword parameters, block behavior, visibility, constants, exceptions,
  equality and hashing, serialization, load paths, executables, and type signatures as possible contracts.

## Design

- **Domain ownership** — Give each real concept, invariant, and behavior a coherent owner. Use the number of classes the
  domain requires; do not drain behavior into procedural services, hashes, conditionals, or caller knowledge merely to
  reduce class count.
- **Values** — Use `Data.define` for record-like values when the supported Ruby range and immutable-member semantics fit;
  use `Struct.new` when its mutable container behavior is part of the contract. Use a normal class when validation,
  invariants, behavior, inheritance, or a stable API needs an explicit owner.
- **Internal helpers** — Keep cohesive implementation helpers inside the owning namespace when that improves locality.
  Use `private_constant` for internal constants, but do not hide constants intentionally exposed through public APIs.
- **Abstractions** — Challenge metaprogramming, DSL layers, service objects, wrapper classes, callbacks, registries, and
  indirection whose cost is not justified by current behavior. Fewer classes or lines are not simpler when invariants
  lose an owner or behavior moves into callers.

## Loading and packages

- **Executables** — Keep `bin/foo` thin: require the established executable entrypoint, then invoke it. Do not reach into
  `lib` with `require_relative` unless bare-checkout execution is an explicit package contract.
- **Bare checkout** — When bare-checkout execution is promised, allow `bin/foo` to prepend only its adjacent `lib/`
  directory to `$LOAD_PATH` when absent, then use the normal public `require`. Do not use `$LOAD_PATH` to assemble
  library internals or search arbitrary paths.
- **Entrypoints** — In executable implementations, load the public library entrypoint such as `require "foo"` before
  executable-only features. Let each public library or independently loadable component entrypoint own its internal tree
  with `require_relative`; use normal `require` for external gems and public component entrypoints.
- **Requires** — Keep standard-library requires near the files that use them unless the repository consistently
  centralizes them. Avoid sibling requires in leaf files when an owner already establishes load order.
- **Validation** — Before changing loading, inspect library entrypoints, executables, gemspec metadata, and package tests.
  Validate each execution mode the repository actually promises.
- **Dependencies** — Pass gem names for targeted Bundler updates. When intentionally updating the entire bundle, use the
  explicit full-update form required by the configured Bundler version, inspect the lockfile diff, and run relevant tests.

## Tooling and types

- **Autocorrection** — Treat broad RuboCop autocorrection, especially `rubocop -A`, as unsafe until its complete diff is
  reviewed. Do not rename public keywords, abstract parameters, or CLI parameters merely to satisfy lint.
- **Signatures** — Preserve the established RBI/RBS and Sorbet/Steep boundary. Update material signatures with
  implementation changes; do not replace the repository's signature system without an explicit project decision.
- **Singleton visibility** — For a cohesive lexical group of private singleton helpers, prefer a `private` section inside
  `class << self`. Keep `private_class_method` for isolated, inherited, generated, or deliberately post-defined
  visibility changes.

## Testing

- **Framework** — Preserve the repository's selected Minitest or RSpec framework and helper. Do not translate frameworks
  merely to apply this guidance.
- **Characterization** — Before changing established behavior, add or verify characterization coverage for the affected
  contract when practical. Do not begin a major refactor without enough coverage of materially affected behavior.
- **Scope** — Run the narrowest test command that covers the change, then broaden when touched code is shared. Focus
  cases on observable contracts such as call shape, blocks, exceptions, equality, serialization, load modes, executable
  behavior, and the supported Ruby floor.
- **Minitest** — Load [Minitest conventions](references/minitest.md) when Minitest layout or naming is materially being
  created, changed, or reviewed. Do not load it for RSpec or behavior-only work whose established naming remains intact.

## Documentation

- **YARD** — Load [YARD](references/yard.md) when writing or reviewing Ruby public API documentation.
- **Authority** — Prefer project documentation first. For Ruby language and standard-library behavior, use the official
  Ruby documentation for the supported version. For Bundler behavior, use the official Bundler command documentation
  when the configured version matters.

## Compatibility and cleanup

- **Compatibility** — Check the concrete supported surface before modernization: calls, blocks, visibility, constants,
  return values, exceptions, equality and hashing, persisted representations, type signatures, gem entrypoints,
  executable behavior, and load paths. Preserve contracts with real consumers rather than hypothetical compatibility.
- **Residue** — After a change, inspect the affected Ruby surface for stale requires, autoload entries, constants,
  aliases, compatibility branches, visibility declarations, signatures, tests, fixtures, and gem metadata. Remove only
  residue made obsolete by the change; do not broaden cleanup into unrelated churn.
