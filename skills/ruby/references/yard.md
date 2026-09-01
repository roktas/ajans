# YARD

Load this reference only when writing or reviewing Ruby public API documentation.

## Public contracts

- **Scope** — Document every public class, module, and method affected by the work. Do not turn a focused change into a
  repository-wide documentation sweep unless requested.
- **Semantics** — Describe observable behavior rather than implementation. Give each public class or module a concise
  responsibility summary.
- **Language** — Keep public API documentation in English unless the user, project, or publication contract requires
  another language.
- **Tags** — For each material public method contract, use the applicable tags:
  - `@param name [Type]` for parameters and `@option` for meaningful hash options;
  - `@return [Type]` for the exact return contract, including `[void]` when callers must not use the value; describe
    meaningful keys or members for structured returns;
  - one `@raise [Error]` for each caller-visible exception and its condition;
  - `@yield`, `@yieldparam`, and `@yieldreturn` when block behavior is public.
- **Call shape** — Document `self.call` separately from `#call`.
- **Examples** — Use `@example` for module-level constructs and whenever concise runnable usage clarifies semantics. Use
  `@see` instead of duplicating related API documentation.
- **Private API** — Document private methods only when non-obvious behavior needs explanation.
- **Special tags** — Use `@abstract`, `@deprecated`, `@api private`, and `@overload` only when they express a real
  contract.
- **Friction** — If a contract needs elaborate defensive prose, check whether avoidable API friction should instead be
  corrected in code.

## Workflow and validation

1. Identify affected public surfaces early enough that their documented contracts can inform implementation.
2. Update YARD blocks with the implementation and tests rather than postponing documentation until context is lost.
3. Run the repository's focused documentation check. Use `yard stats --list-undoc` or `yard doc` only when the project
   adopts those whole-project checks, and keep unrelated documentation gaps separate from regressions in the requested
   scope.
