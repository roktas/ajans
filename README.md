# Ajans

Ajans is the canonical public agent configuration for this workspace. It keeps user-wide agent instructions, focused
reusable skills, client bootstrap instructions, and validation fixtures in one repository.

## Layout

- `agents/AGENTS.md`: public user-wide agent instructions.
- `agents/CHATGPT.md`: ChatGPT Project bootstrap and lazy skill-loading rules.
- `skills/<name>/SKILL.md`: reusable Agent Skills and their skill-local resources.
- `tests/`: skill-package validation and regression fixtures.

Private agent or workspace-specific state belongs outside this repository, normally in the private `home-` companion
repository or local runtime state.

## Installation

The maintainer setup uses Ajans as a sibling source checkout, like the Tilde control plane. Tilde projects
`agents/AGENTS.md` and the skill directories into the shared `~/.agents` surface. It does not install Ajans as a plugin
or a skill package.

Other users can install the portable skill collection with a compatible Agent Plugin client. They can also use the
Skills CLI:

```bash
npx skills add roktas/ajans
```

## Agent Plugins

Ajans is packaged as an [Agent Plugins v1](https://agent-plugins.org/) plugin. The root [`plugin.json`](plugin.json)
declares the v1.0.0 schema, and portable skills live at the standard `skills/<name>/SKILL.md` discovery location.
Client-specific files bundled inside a skill, such as `agents/openai.yaml`, remain skill-local metadata and are not
portable Agent Plugins component types.

## Validate

Run from the repository root:

```bash
ruby tests/skills.rb
ruby tests/skills.rb tests/fixtures/skills
```

The general audit validates skill frontmatter, OpenAI interface metadata, and package-local Markdown links. The fixture
invocation covers fenced and inline examples, comments, site-root URLs, and titled package links.

## Sources

### Grilling

[`skills/grilling`](skills/grilling) is adapted from Matt Pocock's
[`grilling`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grilling) skill and stays intentionally
close to the original. The local version makes fact discovery tool-agnostic so it can work across agent environments.
The upstream skill is MIT-licensed; its license notice is preserved in [`skills/grilling/LICENSE`](skills/grilling/LICENSE).

### Testing

[`skills/testing`](skills/testing) is adapted from Matt Pocock's
[`tdd`](https://github.com/mattpocock/skills/tree/main/skills/engineering/tdd) skill. Ajans keeps its behavioral testing,
public-seam, anti-pattern, mocking-boundary, and red-green ideas, but makes TDD an explicit test-first mode inside a
broader testing skill. The upstream skill is MIT-licensed; its license notice is preserved in
[`skills/testing/LICENSE`](skills/testing/LICENSE).

If these skills are useful to you, browse the broader [`mattpocock/skills`](https://github.com/mattpocock/skills)
repository. It contains other focused skills that are worth reviewing directly at the source.
