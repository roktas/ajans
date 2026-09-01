# Ekler

Ekler is a small collection of focused agent skills. Each skill should add specific judgment or behavior without turning
ordinary work into a framework.

## Sources

### Grilling

[`skills/grilling`](skills/grilling) is adapted from Matt Pocock's
[`grilling`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grilling) skill and stays intentionally
close to the original. The local version makes fact discovery tool-agnostic so it can work across agent environments.
The upstream skill is MIT-licensed; its license notice is preserved in [`skills/grilling/LICENSE`](skills/grilling/LICENSE).

### Testing

[`skills/testing`](skills/testing) is adapted from Matt Pocock's
[`tdd`](https://github.com/mattpocock/skills/tree/main/skills/engineering/tdd) skill. Ekler keeps its behavioral testing,
public-seam, anti-pattern, mocking-boundary, and red-green ideas, but makes TDD an explicit test-first mode inside a
broader testing skill. The upstream skill is MIT-licensed; its license notice is preserved in
[`skills/testing/LICENSE`](skills/testing/LICENSE).

If these skills are useful to you, browse the broader [`mattpocock/skills`](https://github.com/mattpocock/skills)
repository. It contains other focused skills that are worth reviewing directly at the source.
