---
name: c
description: >-
  C implementation judgment for language-standard and platform compatibility, public headers and ABI, ownership,
  allocation, lifetime, integer bounds, undefined behavior, threading, native builds, and C-oriented validation. Use only
  when producing or materially revising substantive C code. Do not activate for routine technical Q&A, repository
  browsing, read-only inspection, compiler or tool use, file types, fenced examples, project labels, or incidental C
  mentions.
---

# C

## Baseline

### Contract and platform

- Resolve the configured language standard, compiler families and versions, target platforms, feature-test macros, build
  flags, public headers, formatter, analysis tools, and tests before choosing syntax, attributes, builtins, or library
  APIs. The compiler installed on the current machine is not the support floor.
- Treat exported names, declarations, linkage, calling conventions, struct and union layout, enum representation,
  alignment, qualifiers, macro behavior, error codes, and ownership rules as possible source or ABI contracts.
- Do not state concrete sizes, offsets, enum representations, or calling-convention outcomes without the target ABI or a
  verified compiler probe. When the target is unknown, identify the dependency and risk without inventing a layout.
- Keep declarations consistent across headers, definitions, generated bindings, build feature checks, and callers. Do
  not change an exposed representation or function signature without establishing the supported consumer boundary.

### Ownership and lifetime

- Trace who creates, initializes, borrows, transfers, shares, mutates, and releases each resource. Make nullability,
  lifetime, cleanup order, and thread ownership explicit at interfaces where callers must act on them.
- Design partial initialization so every failure path releases only resources that were acquired and leaves caller-
  visible outputs in their documented state. Keep allocation and deallocation families paired.
- Check pointer provenance, object lifetime, aliasing, alignment, effective type, bounds, overlap, and invalidation
  before relying on casts, byte access, flexible arrays, container macros, or reallocating operations.

### Arithmetic and representation

- Check signedness, narrowing, promotion, shift width, overflow, sentinel conversion, and size multiplication before an
  arithmetic result controls allocation, indexing, pointer movement, I/O length, or serialization.
- Distinguish byte counts from element counts and use the type required by the interface. Validate before converting; a
  wider intermediate does not make a narrowed result safe.
- Do not infer defined behavior from one optimizer, architecture, sanitizer run, or debug build. Treat undefined,
  unspecified, implementation-defined, and locale-dependent behavior according to the supported contract.

### Concurrency and validation

- Preserve the repository's threading and atomic model. Check shared-object lifetime, data races, atomic ordering,
  signal-safety, callback reentrancy, and lock ordering only where the affected path makes them material.
- Use the project's build, tests, warnings, static analysis, and sanitizer configurations. Do not introduce global
  `-Werror`, a new language standard, or a repository-wide sanitizer policy merely for local validation.
- Test success, boundary values, allocation or I/O failure, partial initialization, cleanup, and supported platform or
  compiler variants in proportion to the changed contract.

## References

Load [style defaults](references/style.md) only when a C source-style decision is material and repository rules, a
configured formatter, or established surrounding style do not already settle it. Do not load the reference for
behavior-only work whose style remains unchanged.

## Verification and testing

Use the project's existing build, test, warning, static-analysis, and sanitizer setup. Focus evidence on the material
contract, including success and boundary behavior, allocation or I/O failure, partial initialization, cleanup, ownership
and lifetime, and supported compiler or platform variants when they can change the conclusion. Do not introduce
repository-wide warning, sanitizer, language-standard, or platform matrices.

## Backward compatibility

Check the configured standard and concrete public surface: headers, declarations, macro expansions, calling convention,
symbol visibility and versioning, struct or union size and layout, enum values, qualifiers, ownership, error behavior,
serialized data, plugins, FFI bindings, and build flags. Separate source compatibility from binary compatibility and
preserve only contracts with real consumers.

## Smallest necessary change

Keep a focused C change local to the owning declaration, definition, resource path, build rule, and test when that fully
satisfies the request. Preserve the support floor, public representation, ownership model, error convention, and local
style. Avoid unrelated header churn, formatter changes, warning-policy expansion, new portability layers, and broad
rewrites.

## Affected scope cleanup

After the requested change, inspect the affected C surface for stale declarations, forward declarations, macros, feature
checks, enum values, switch arms, ownership comments, cleanup labels, error branches, build inputs, bindings, tests, and
fixtures. Remove only residue made obsolete by the change; do not turn local cleanup into a style campaign.

## Fault diagnosis and correction

Reproduce the failure under the relevant build and configuration, then trace values, ownership, lifetime, control flow,
and optimizer-sensitive assumptions to the first invalid operation or broken contract. Check integer bounds, allocation
failure, partial initialization, use-after-lifetime, double release, aliasing, alignment, races, and undefined behavior
where evidence points; do not mask the fault with initialization, retries, or null checks that leave its cause intact.
