# C style defaults

Load this reference only when a C source-style decision is material and repository rules, a configured formatter, or the
established surrounding style do not already settle it. These are working defaults, not universal C correctness.

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

Do not restyle unrelated code merely because this reference is active.
