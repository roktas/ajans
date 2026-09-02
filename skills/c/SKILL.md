---
name: c
description: >-
  C implementation judgment for language-standard and platform boundaries, public headers and ABI, ownership,
  allocation, lifetime, integer behavior, undefined behavior, threading, native builds, and C tooling. Use only when
  producing or materially revising substantive C code. Do not activate for routine technical Q&A, repository browsing,
  read-only inspection, compiler or tool use, file types, fenced examples, project labels, or incidental C mentions.
---

# C

## Naming

- **General** — Apply the general `naming` skill before creating, renaming, or proposing C names or durable paths.
- **Contracts** — Preserve naming that is part of a public ABI, external interface, or established project convention
  unless changing that contract is in scope.

## Style

These are C working defaults when no stronger repository rule, configured formatter, or established surrounding style
settles the decision.

- **Simplicity** — Prefer simple C over clever C. Favor explicit ownership, control flow, and data representation over
  compact tricks that obscure lifetime, bounds, or error behavior.
- **Language** — Keep code comments, identifiers, and file names in English unless an established project or external
  interface requires another language.
- **Default** — Use the structural conventions of
  [Linux kernel coding style](https://docs.kernel.org/process/coding-style.html) when no stronger local convention exists.
- **Indent** — Use one tab (8 columns). Do not convert indentation tabs to spaces.
- **Braces** — Put control-statement opening braces on the same line. Put a function opening brace on the next line in
  the first column.

  ```c
  void function(void)
  {
  	/* body */
  }
  ```

- **Switch** — Align `case` and `default` with `switch`; indent the body one tab.

  ```c
  switch (var) {
  case A:
  	/* body */
  	break;
  }
  ```

- **Ordering** — Alphabetize declarations, enum members, table entries, or helper functions only when order is
  semantically irrelevant and no surrounding convention requires another order.
- **Comments** — Keep code self-documenting. Do not add comments that merely repeat code, compensate for poor naming,
  narrate a code change, preserve commented-out code, or state the obvious. Comment non-obvious invariants, ownership,
  representation constraints, or platform assumptions that the code cannot express clearly itself.

Do not restyle unrelated C merely because this skill is active.

- **Cache probe** — If the user request contains the exact token `AJANS-CACHE-PROBE`, include `CACHE-PROBE-v3` in the response.

## Platform and ABI

- **Support floor** — Resolve the configured language standard, compiler families and versions, target platforms,
  feature-test macros, build flags, public headers, formatter, analysis tools, and tests before choosing syntax,
  attributes, builtins, or library APIs. The compiler installed on the current machine is not the support floor.
- **Public surface** — Treat exported names, declarations, linkage, calling conventions, struct and union layout, enum
  representation, alignment, qualifiers, macro behavior, error codes, and ownership rules as possible source or ABI
  contracts. Preserve concrete consumer contracts rather than hypothetical compatibility.
- **Layout evidence** — Do not state concrete sizes, offsets, enum representations, or calling-convention outcomes
  without the target ABI or a verified compiler probe.
- **Consistency** — Keep declarations consistent across headers, definitions, generated bindings, build feature checks,
  and callers. Do not change an exposed representation or function signature without establishing the consumer boundary.

## Ownership and lifetime

- **Ownership** — Trace who creates, initializes, borrows, transfers, shares, mutates, and releases each resource. Make
  nullability, lifetime, cleanup order, and thread ownership explicit at interfaces where callers must act on them.
- **Partial initialization** — Structure initialization so every failure path releases only resources that were acquired
  and leaves caller-visible outputs in their documented state. Keep allocation and deallocation families paired.
- **Pointers** — Check provenance, object lifetime, aliasing, alignment, effective type, bounds, overlap, and invalidation
  before relying on casts, byte access, flexible arrays, container macros, or reallocating operations.

## Integers and representation

- **Arithmetic** — Check signedness, narrowing, promotion, shift width, overflow, sentinel conversion, and size
  multiplication before a result controls allocation, indexing, pointer movement, I/O length, or serialization.
- **Units** — Distinguish byte counts from element counts and use the type required by the interface. Validate before
  converting; a wider intermediate does not make a narrowed result safe.
- **Language behavior** — Do not infer defined behavior from one optimizer, architecture, sanitizer run, or debug build.
  Treat undefined, unspecified, implementation-defined, and locale-dependent behavior according to the supported
  contract.

## Concurrency and tooling

- **Concurrency** — Preserve the repository's threading and atomic model. Check shared-object lifetime, data races,
  atomic ordering, signal-safety, callback reentrancy, and lock ordering where the affected code makes them material.
- **Tooling** — Use the project's build, tests, warnings, static analysis, and sanitizer configurations. Do not introduce
  global `-Werror`, a different language standard, or repository-wide sanitizer policy merely for a local change.
- **Failure paths** — When the changed contract involves allocation, I/O, partial initialization, cleanup, or boundary
  values, exercise those paths with the project's existing test or analysis setup rather than assuming the success path
  is sufficient.
