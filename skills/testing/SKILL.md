---
name: testing
description: >-
  Test design for behavior, public seams, regression coverage, integration tests, and test-first development. Use when
  writing or materially revising tests, reviewing test design, choosing test seams, or when tests are a substantive part
  of a bug fix or feature. Do not activate merely to run an existing test command or for routine verification. Apply the
  TDD loop only when the user explicitly requests TDD, test-first work, or red-green-refactor.
---

# Testing

Design tests that verify observable behavior and survive internal refactoring. Use project and language-specific test
conventions when they exist; this skill owns general test judgment, not framework syntax.

## Behavior

- Test behavior through public interfaces, not private methods or internal call structure.
- Write tests as specifications of capabilities and contracts: describe what callers can observe, not how the code
  implements it.
- Prefer a small set of tests at meaningful boundaries over broad coverage of incidental implementation detail.
- Use expected values from an independent source of truth such as a specification, worked example, known literal, or
  external contract. Do not recompute the expected value with the same logic as the implementation.
- Add regression tests for bugs at the highest stable seam that reproduces the behavior without depending on irrelevant
  internals.

## Seams

A seam is a stable public boundary where behavior can be observed without reaching inside the implementation.

- Prefer seams already established by the public API, command interface, protocol, file format, or project contract.
- Do not ask the user to reconfirm a seam that the governing contract already settles.
- When the interface itself is an unresolved material design choice, resolve that choice before writing tests.
- Test the critical paths and complex logic at the fewest useful seams. Do not create a test layer for every internal
  component merely because it exists.

## Anti-patterns

- **Implementation-coupled tests** — Avoid tests that mock internal collaborators, call private methods, assert internal
  call counts or order, or break when behavior-preserving refactors change structure.
- **Tautological tests** — Do not derive the expected result with the same algorithm or data transformation as the code
  under test. Such a test can agree with the implementation while both are wrong.
- **Side-channel verification** — Prefer observing behavior through the same public contract available to callers. Do not
  bypass that contract only to inspect internal state when a stable observable outcome exists.
- **Horizontal slicing** — Do not write a large imagined test suite first and implementation later. When working
  test-first, use vertical slices that let each passing test inform the next one.

## Mocking

Load [mocking guidance](references/mocking.md) when a test requires substitutes, fakes, stubs, clocks, random sources,
network services, databases, filesystems, processes, or other external boundaries. Do not load it when no boundary
substitution decision is material.

## TDD

Use this loop only when TDD, test-first work, or red-green-refactor is explicitly requested.

- **Red before green** — Write one failing behavioral test first and confirm that it fails for the expected reason.
- **One slice at a time** — Use one seam, one test, and the smallest implementation needed to make that test pass.
- **No speculative green** — Do not implement behavior for future tests before a failing test requires it.
- **Vertical progression** — Repeat test → implementation in small tracer-bullet slices instead of writing all tests and
  then all implementation.
- **Refactor after green** — Refactor only after the behavior is green. Keep behavior unchanged and rerun the relevant
  tests after refactoring.

## Verification

Run the narrowest relevant tests during development and broaden verification when shared behavior or risk warrants it.
Use the repository's existing framework, helpers, fixtures, build commands, and language-specific guidance rather than
introducing a new test stack for convenience.
