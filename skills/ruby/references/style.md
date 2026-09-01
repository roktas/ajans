# Ruby style defaults

Load this reference only when a Ruby source-style decision is material and repository rules, a configured formatter, or
the established surrounding style do not already settle it. These are working defaults, not universal Ruby correctness.

- **Formatting** — Use the formatter already configured by the repository. When none is configured, follow surrounding
  style and do not introduce a formatter as an incidental change. Do not hand-align code against formatter output.
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

Do not reorder or reformat unrelated Ruby merely because this reference is active.
