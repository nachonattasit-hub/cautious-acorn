---
name: create-skill
description: "Create a reusable skill file (SKILL.md) for VS Code agent customization."
argument-hint: What should this skill produce?
---

# Create Skill

Use this skill when you need to generate a new `SKILL.md` file that packages a multi-step workflow, checklist, or agent customization pattern.

## What to ask first

- What outcome should the skill produce?
- Should the skill be workspace-scoped or personal?
- Should it be a quick checklist or a full multi-step workflow?

## Steps

1. Confirm the target scope:
   - Workspace: save under `.github/skills/<name>/SKILL.md`
   - User: save under `{{VSCODE_USER_PROMPTS_FOLDER}}/skills/<name>/SKILL.md`
2. Draft YAML frontmatter with:
   - `name`
   - `description`
   - optional `argument-hint`
3. Add a clear purpose section:
   - what the skill does
   - when to use it
   - expected inputs and outputs
4. Include a short usage guide and examples.
5. Validate the file path and frontmatter syntax.

## Validation

- Ensure the file exists at the chosen path.
- Ensure the frontmatter is valid YAML and contains a `description`.
- Ensure the skill name matches the folder name if applicable.

## Example prompt

"Create a `SKILL.md` that helps generate a new project scaffold for a TypeScript library."
