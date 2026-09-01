---
name: naming
description: >-
  Naming judgment for durable names across code, files and directories, paths, commands, skills, modules and packages,
  types, functions, variables and fields, APIs, configuration keys, assets, and named concepts. Use whenever creating,
  renaming, or proposing such a name, even when naming is incidental to a larger task. Do not activate for ordinary prose
  wording or read-only inspection of existing names.
---

# Naming

Apply this guidance before choosing a name, not as cleanup after implementation.

## Project dictionary

Treat established project vocabulary as part of the naming contract.

- **Lookup** — Before naming, look for a project `DICT.md`. Also inspect applicable `AGENTS.md` sections named `Lexicon`,
  `Glossary`, `Dictionary`, or `Vocabulary`. Apply their canonical terms, definitions, distinctions, and usage rules.
- **Canonical terms** — Reuse the canonical term for an existing concept instead of inventing a synonym. Use one name for
  one concept and do not reuse that name for unrelated concepts.
- **Conflicts** — If the user or current work uses a term that conflicts with the project dictionary, surface the
  conflict immediately rather than silently choosing one meaning.
- **Precision** — When language is vague, overloaded, or collapses distinct domain concepts, propose a precise canonical
  term before encoding it into names.
- **Evidence** — When relevant, check existing code, documentation, schemas, APIs, and sibling names for how the concept
  is actually represented. Surface contradictions between stated domain language and the repository instead of
  normalizing them silently.
- **Update** — When repository mutation is already authorized and a canonical domain term, distinction, or definition
  becomes settled during the work, update the applicable `DICT.md` immediately rather than batching vocabulary changes
  for later. Without edit authorization, surface the proposed dictionary change but do not modify the repository.
- **Creation** — When repository mutation is already authorized, create `DICT.md` lazily only after a durable domain term
  or distinction has actually been established and no applicable project dictionary exists. Do not create it merely
  because this skill is active. Without edit authorization, recommend creation when useful but do not create it.
- **Format** — When creating or updating `DICT.md`, load [the dictionary format](references/dict.md) before editing it.
- **Scope** — Keep `DICT.md` focused on domain vocabulary and term-specific usage. It is not an implementation spec,
  scratchpad, architecture log, or home for general naming rules.

Match sibling names in the same scope for vocabulary, grammatical form, style, length, and specificity. When an active
language skill has a `## Naming` section, apply it as a language-specific refinement of this skill.

## Core rules

- **Simplicity** — Prefer one simple, meaningful word when context allows.
- **Context** — Do not repeat context already supplied by the containing project, directory, namespace, module, class,
  document, component, or command.
- **Compounds** — Before using `-`, `_`, `:`, `/`, camel case, Pascal case, or another multiword form, check whether a
  simpler one-word name expresses the same concept.
- **Public names** — Keep public or user-facing names short, polished, and memorable. Internal names may be plainer or
  more explicit.
- **Scope** — Let name length follow scope: longer when surrounding context is weak, shorter when local context
  disambiguates.
- **Qualifiers** — Add a qualifier only when it separates real sibling concepts in the current scope; do not add one
  merely to sound more precise.
- **Role** — Name by stable domain role or purpose rather than container type, implementation shape, or temporary workflow
  stage unless that distinction is itself part of the contract.
- **Representation** — Do not encode a value's type, representation, storage, or transport form in its name unless that
  distinction is materially useful, such as when two representations coexist during conversion.
- **Durability** — Prefer names that remain true as implementation and contents evolve. Do not encode an incidental tool,
  format, date, status, or temporary stage unless it is a durable distinction.
- **Generic roles** — Avoid generic modeling words such as `manager`, `handler`, `helper`, `util`, `common`, `data`,
  `info`, `object`, or `service` when a domain name states the responsibility more precisely.
- **Consistency** — Before finalizing introduced names, check the affected scope for synonyms, repeated context,
  inconsistent siblings, superseded names, and paths whose components no longer describe their role.
- **Exceptions** — Break these rules only for a concrete convention, contract, interoperability requirement, or clarity
  reason.

## Examples

Use these as patterns, not literal replacements:

- In a `provision` context, prefer `Plan` over `ProvisionPlan`: the surrounding scope already supplies `Provision`.
- Prefer `bash` over `lang-bash` when `lang-` is only a category prefix and does not distinguish a real sibling concept.
- Prefer `smoke` over `lxd-smoke` when LXD is only the current backend. Add the backend only when multiple backend-specific
  smoke helpers coexist.
- Prefer `target_module` over `link_target_list_module` when link/list mechanics are implementation detail rather than a
  domain distinction that must separate siblings.
- Prefer a contextual path such as `state/hosts/` over repeating the parent concept in a child such as
  `state/host-state/`.

## Paths

Treat durable file and directory paths as naming decisions with an additional portability contract.

- **Components** — Apply the core naming rules to every path component that is being created or renamed.
- **Relative paths** — Prefer repository-relative or component-relative paths for repository content when the consumer
  supports them.
- **Home paths** — Do not persist machine-specific expanded home directories in tracked artifacts unless the contract
  requires that exact absolute path.
- **Tilde** — Use `~` only when the target consumer is known to expand it; do not assume shell tilde expansion in
  configuration, APIs, libraries, service files, or documents.
- **Runtime paths** — Keep runtime-discovered or environment-specific absolute paths in runtime state, generated output,
  or local/private configuration rather than portable repository defaults.
- **Grammar** — Preserve consumer-specific path grammar. Do not normalize Windows paths, URLs, package paths, or similar
  forms merely for visual consistency.
- **Boundaries** — When a durable path crosses a repository, publication, or ownership boundary, make that boundary
  explicit when it affects portability, privacy, or maintenance.
- **Resolution** — Verify an external tool's path expansion and resolution semantics before encoding them into a durable
  artifact.
