---
name: ruby
description: >-
  Ruby implementation judgment for runtime compatibility, public APIs, value models, gems and loading, Bundler, RBI/RBS,
  tests, RuboCop, visibility, and YARD. Use only when producing or materially revising substantive Ruby code. Do not
  activate for routine technical Q&A, repository browsing, read-only inspection, Ruby tool use, file types, fenced
  examples, project labels, or incidental Ruby mentions.
---

# Ruby

## Naming

Apply the general `naming` skill before creating, renaming, or proposing Ruby names or durable paths.

- Use `snake_case` for methods, local variables, and symbols; use `CamelCase` for classes and modules.
- Use `?` for predicates that return boolean-like results. Use `!` only when it communicates a meaningful dangerous or
  mutating distinction; do not add punctuation merely for emphasis.
- Preserve public method names, keyword names, constants, and serialized or reflective names as contracts unless changing
  that surface is in scope.

## Baseline

### Runtime contract

- Resolve the supported Ruby range from repository evidence such as `.ruby-version`, version-manager files, the
  gemspec's `required_ruby_version`, lockfiles, CI, and project rules before choosing syntax or APIs. The installed
  interpreter describes the current machine, not the compatibility floor.
- When no version evidence exists, use clear broadly supported syntax. State an assumption only when it can change the
  design or result; do not silently raise a project's Ruby floor.
- Treat public method names, positional and keyword parameters, block behavior, visibility, constants, exceptions,
  equality and hashing, serialization, load paths, executables, and type signatures as possible contracts rather than
  incidental syntax.

### Domain models

- Give each real concept, invariant, and behavior a coherent owner. Use the number of classes the domain requires; do
  not drain domain behavior into procedural services, hashes, conditionals, or caller knowledge merely to reduce class
  count. Avoid both speculative class hierarchies and anemic models.
- Use `Data.define` for record-like values only when the supported Ruby range and immutable-member semantics fit. Use
  `Struct.new` when its mutable, enumerable container behavior is part of the contract. Use a normal class when
  validation, invariants, behavior, inheritance, or a stable public API needs an explicit owner.
- Keep cohesive implementation helpers inside the owning namespace when that improves locality. Use `private_constant`
  for internal constants, but do not hide constants that are intentionally public or appear in public signatures.

### Loading and packages

- Preserve gem entrypoint boundaries. Keep `bin/foo` thin: require the established executable entrypoint, then invoke
  it. Do not reach into `lib` with `require_relative` unless bare-checkout execution is an explicit package contract.
- When bare-checkout execution is an explicit contract, allow `bin/foo` to prepend only its adjacent `lib/` directory to
  `$LOAD_PATH` when absent, then use the normal public `require`. Treat this as a narrow package-discovery bootstrap; do
  not use it to assemble library internals or search arbitrary paths.
- In an executable implementation, load the public library entrypoint such as `require "foo"` before executable-only
  features. Do not load the executable implementation from the public library entrypoint.
- Let each public library or independently loadable component entrypoint own its internal tree with `require_relative`.
  Use normal `require` for external gems and public component entrypoints. Avoid sibling requires in leaf files when an
  owner already establishes load order.
- Keep standard-library requires near the files that use them unless the repository consistently centralizes them.
- Before changing loading, inspect library entrypoints, executables, gemspec metadata, and package tests. Validate every
  promised mode: installed gem, Bundler-configured source, and bare checkout only when the repository supports it.
- Update named gems for a targeted dependency change. When intentionally updating the entire bundle, account for
  `update_requires_all_flag` and use explicit `--all` when the repository's Bundler configuration requires it. Inspect
  the lockfile diff and run the relevant tests.

### Tooling, tests, and types

- Preserve the repository's selected Minitest or RSpec framework and helper; do not translate frameworks merely to apply
  this guidance. Keep test paths, namespaces, and names consistent with the repository's established scheme.
- Before changing established behavior, add or verify characterization coverage for the current contract. Do not begin a
  major refactor until the materially affected behavior has enough coverage; test-helper and snapshot-policy work may
  justify a different order.
- Treat broad RuboCop autocorrection, especially `rubocop -A`, as unsafe until its complete diff is reviewed. Do not
  rename public keywords, abstract parameters, or CLI parameters merely to satisfy lint.
- Preserve the established RBI/RBS and Sorbet/Steep boundary. Update material signatures with implementation changes,
  and do not convert signature systems or adopt experimental RBS comments without an explicit project decision.
- For a cohesive lexical group of private singleton helpers, prefer a `private` section inside `class << self`. Keep
  `private_class_method` for isolated, inherited, generated, or deliberately post-defined visibility changes.

## References

- Prefer authoritative project documentation. For Ruby language and standard-library behavior, use
  <https://docs.ruby-lang.org/en/> for the project's supported version; do not use ruby-doc.org or APIdock as
  authoritative substitutes when official documentation is available. Do not preload or preserve a version table in
  this skill.
- For Bundler command behavior, consult <https://bundler.io/man/> when the installed/configured version matters.
- Load [style defaults](references/style.md) only when a Ruby source-style decision is material and repository rules, a
  configured formatter, or established surrounding style do not already settle it.
- Load [Minitest conventions](references/minitest.md) only when Minitest layout or naming is materially being created,
  changed, or reviewed. Do not load it for RSpec or for behavior-only test work whose established naming remains intact.
- Load [YARD](references/yard.md) only when writing or reviewing Ruby public API documentation.

## Verification and testing

Preserve the established Minitest or RSpec framework, helper, paths, namespaces, and naming scheme. Focus cases on the
observable Ruby contracts that are material to the task, such as positional versus keyword calls, blocks, exceptions,
equality and hashing, serialization, load modes, executable behavior, and the supported Ruby floor. Do not change
frameworks, broaden dependency updates, or expand the suite.

## Backward compatibility

Check the supported Ruby floor and the concrete public surface: positional versus keyword calls, optional arguments,
blocks, visibility, constants and inheritance, return values, exceptions, equality and hashing, Marshal or other
persisted representations, type signatures, gem entrypoints, executable behavior, and load paths. Do not replace
`Struct` with `Data`, change a method signature, or reorganize loading merely because the replacement looks newer; first
establish which observable contracts current consumers rely on.

## Smallest necessary change

Keep a focused Ruby change local to the owning method, class, entrypoint, signature, or test when that fully satisfies
the request. Preserve the supported Ruby floor, public shape, surrounding idiom, visibility, and load order. Avoid
incidental formatter churn, broad autocorrection, method reordering, new gems, new abstraction layers, and unrelated
modernization.

## Affected scope cleanup

After the requested change, inspect its Ruby-specific affected surface for stale requires, autoload entries, constants,
aliases, compatibility branches, visibility declarations, signatures, tests, fixtures, and gem metadata. Remove only
residue made obsolete by the change; do not turn local cleanup into repository-wide style or dependency work.

## Material simplification

Challenge metaprogramming, DSL layers, service objects, wrapper classes, callbacks, registries, and indirection whose
cost is not justified by current behavior. Preserve public calls, supported modes, fallbacks, errors, serialization,
loading, and extension points. Fewer classes or lines are not simpler when invariants lose an owner or behavior moves
into procedural services, hashes, conditionals, or callers.
