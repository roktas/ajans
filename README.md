# Ajans

Ajans is a small collection of focused agent skills. Each skill should add specific judgment or behavior without turning
ordinary work into a framework.

## Agent Plugins

Ajans is packaged as an [Agent Plugins v1](https://agent-plugins.org/) plugin. The root [`plugin.json`](plugin.json)
declares the v1.0.0 schema, and portable skills live at the standard `skills/<name>/SKILL.md` discovery location.
Client-specific files bundled inside a skill, such as `agents/openai.yaml`, remain skill-local metadata and are not
portable Agent Plugins component types.

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
