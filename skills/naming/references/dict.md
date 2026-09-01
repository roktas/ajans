# DICT.md format

Load this reference only when creating or updating a project `DICT.md`.

## Structure

```md
# Dictionary

{One or two sentences describing the domain covered by this dictionary.}

## Terms

**Order**
A request from a customer for one or more products.
_Avoid_: Purchase, transaction

**Invoice**
A request for payment after delivery.
_Avoid_: Bill, payment request
```

Use additional term-group headings only when natural domain clusters have emerged. Keep a flat `## Terms` section when
one cohesive vocabulary is enough.

## Rules

- Be opinionated. Choose one canonical term for a concept; put competing or deprecated terms under `_Avoid_` when that
  distinction helps future naming decisions.
- Keep each definition to one or two sentences. Define what the concept is and the distinction that matters; do not turn
  entries into implementation notes or workflows.
- Include only project-domain vocabulary and project-specific distinctions. General programming terms and generic
  engineering concepts do not belong merely because the project uses them.
- Preserve the exact canonical spelling, casing, plurality, and abbreviation that names should reuse.
- Keep one concept per entry and one canonical term per concept. If two entries overlap, resolve the domain distinction
  instead of documenting synonyms as separate concepts.
- Keep entries concise. Add examples only when a short example is necessary to disambiguate the term.
- When ordering is not semantically useful, keep terms alphabetical within a section.

`DICT.md` is a vocabulary contract. Do not use it as a design document, architecture log, task list, implementation spec,
or general style guide.
