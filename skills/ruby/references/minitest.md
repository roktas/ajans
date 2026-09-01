# Minitest conventions

Load this reference only when Minitest test layout or naming is materially being created, changed, or reviewed and the
repository has not already established a stronger convention. Do not apply it to RSpec or use it to rename unaffected
tests during behavior-only work.

- Follow the repository's selected helper and Minitest style. Mirror the runtime file path under `test` and put the test
  class in the same namespace as the code under test when the project does not establish another layout.
- Name test methods as compact behavior contracts. Optimize for failure output: the name should identify the failed
  contract while relying on file, class, and namespace context instead of restating everything.
- Prefer `test_<subject>_<behavior>` when the subject helps group output. Use stable domain or method words and behavior
  verbs such as `returns`, `raises`, `rejects`, `extracts`, `preserves`, `caches`, `exposes`, and `allows`.
- Name the observable result, not merely the setup. Avoid bare labels such as `simple`, `basics`, `usual`, `default`,
  `empty`, `valid`, `invalid`, `with_*`, or `without_*` unless the complete name still states the contract.
- Use `with_*` or `without_*` only for a meaningful variant of a behavior already named by the rest of the method.
- Use punctuation suffixes only when they are part of the public API under test, such as bang methods or predicates.
- Keep the complete method name, including `test_`, at 60 characters or less. Short names are fine when context makes
  the behavior clear.
- Do not put every assertion from a table in the method name or split one coherent table-driven behavior into tiny tests
  merely to name every case. A focused table is valid when all rows exercise the same contract. For compact
  expected/actual pairs, prefer `each_slice(2)` when it keeps one behavior readable and matches repository style.
- When renaming a test, keep its body and placement unchanged unless a separate rule requires another change.
- Do not leave placeholder tests, unexplained skips, commented-out assertions, or commented-out test bodies. Specify the
  behavior now or remove the placeholder.
