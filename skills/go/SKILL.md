---
name: go
description: >-
  Go implementation guidance for modern language and library idioms plus local Go conventions. Use only when producing
  or materially revising substantive Go code. Do not activate for routine technical Q&A, repository browsing, read-only
  inspection, Go tool use, file types, fenced examples, project labels, or incidental Go mentions.
---

# Go

## Modern Go

If `use-modern-go` is available, call the Skill tool with `use-modern-go` before writing or materially revising Go code.
Follow its version-specific guidance rather than duplicating modern-Go rules here.

If `use-modern-go` is unavailable, continue using project evidence and ordinary Go knowledge. Do not fabricate its
output or block the task solely because the skill is missing.

## Style

- **Language** — Keep code comments, identifiers, and file names in English unless an established project or external
  interface requires another language.

## Naming

Apply the general `naming` skill first, then refine it with these Go-specific conventions.

- **Case** — Use `camelCase` for unexported names and `PascalCase` for exported names; avoid snake case and all-caps
  naming.
- **Initialisms** — Keep initialisms consistently cased: `APIKey`, `userID`, `HTTPClient`, `parseXML`.
- **Export** — Keep names unexported by default. Export only when another package or an external contract needs access.
- **Shadowing** — Avoid shadowing builtins and imported package names.
- **Packages** — Use short lowercase package names, preferably one clear word. Avoid catch-all package names such as
  `common`, `util`, `utils`, `helper`, `helpers`, `types`, and `interfaces`.
- **Package chatter** — Avoid repeating the package name at call sites: prefer `customer.New()` over
  `customer.NewCustomer()`.
- **Receivers** — Use short, consistent receiver names derived from the receiver type; avoid `this`, `self`, and `me`.
- **Getters** — Omit `Get` from getters (`Address()`); use `Set` for setters (`SetAddress()`).
- **Interfaces** — Name single-method interfaces from their method when natural, commonly with an `-er` form such as
  `Reader` or `Writer`; do not append `Interface` merely to mark the type.
- **Files** — Prefer short lowercase filenames. For multiword filenames, follow repository convention; when none exists,
  prefer concatenation and reserve underscores for Go's meaningful filename suffixes.
