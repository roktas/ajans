Project repository: `OWNER/REPOSITORY`

The GitHub repository `roktas/ajans` is the canonical source for public agent instructions and reusable Agent Skills.
Refer to it below as Ajans.

At the start of each conversation:

1. Read `agents/AGENTS.md` from Ajans before applying Ajans guidance.
2. If the project repository has a root `AGENTS.md`, read it next and apply it as project-specific instructions.
3. If the project repository has `.agents/skills`, scan `.agents/skills/*/SKILL.md`. Read only the YAML frontmatter and
   add each valid `name` and `description` to the conversation's available-skill list. Do not read the skill body yet.
4. Reuse the loaded instructions and project-skill list for the remainder of the conversation.
5. Do not fetch these bootstrap files again unless the user explicitly asks to refresh their repository context.

For each user request:

1. Decide whether the request plausibly matches an available project skill or an Ajans skill under
   `skills/<name>/SKILL.md`.
2. Do not activate a skill merely because its language, tool, file type, or name is mentioned.
3. On the first activation of a skill, read its current `SKILL.md` from its owning repository. Use its frontmatter
   `description` as the activation gate.
4. If both repositories define the same skill name, use the project skill.
5. Reuse a loaded skill for the remainder of the conversation. Do not fetch it again unless its repository context is
   refreshed.
6. If an active skill requires another skill, load that skill from its owning repository on its first activation.
7. Read referenced files only when an active skill makes them relevant.
8. If no skill clearly applies, answer normally without loading unrelated skills.

When the user asks to refresh Ajans, discard the loaded Ajans instructions and skill state, then reload them as needed.
When the user asks to refresh the project repository, discard its loaded instructions, skill list, and skill state, then
repeat the project bootstrap steps.
