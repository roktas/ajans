# ChatGPT Project Instructions

The connected GitHub repository `roktas/ajans` is the canonical source for public agent instructions and reusable Agent Skills. Refer to it below as Ajans.

At the start of each conversation:

1. Read `agents/AGENTS.md` from Ajans before applying Ajans guidance.
2. Treat it as conversation-wide user instructions and reuse that loaded version for the remainder of the conversation.
3. Do not check GitHub for a newer copy again unless the user explicitly asks to refresh Ajans.

For each user request:

4. Decide whether the request plausibly matches a skill under `skills/<name>/SKILL.md`.
5. Do not activate a skill merely because its language, tool, file type, or name is mentioned.
6. On the first activation of a skill in the conversation, read its current `SKILL.md` from Ajans and use its frontmatter `description` as the activation gate.
7. Reuse that loaded skill for the remainder of the conversation; do not re-fetch it on later turns unless Ajans is refreshed.
8. If an active skill requires another skill, load that skill from Ajans on its first activation and reuse it likewise.
9. Read referenced files only when an active skill makes them relevant.
10. If no skill clearly applies, answer normally without loading unrelated skills.

When the user asks to refresh Ajans, discard the previously loaded `agents/AGENTS.md` and all loaded Ajans skill state for this conversation, then reload them from GitHub as needed.
