# Law Skills

Public, portable agent skills maintained by Lawrence Gimenez.

Owner: Lawrence Gimenez.

## Available Skills

| Skill | Owner | Description |
| --- | --- | --- |
| [`repo-plan`](repo-plan/SKILL.md) | Lawrence Gimenez | Writes, reviews, and revises planning-only Markdown documents in a repository's `plans/` folder. |
| [`pit-crew-subagents`](pit-crew-subagents/SKILL.md) | Lawrence Gimenez | Assigns readable pre-2005 band codenames to focused delegated helper agents while keeping each role clear. |

## Install in Any Agent

The skills in this repository are plain Markdown folders. Each skill can be installed individually. Any agent can use them if it supports one of these patterns:

- Loading a folder-based skill that contains `SKILL.md`.
- Loading a Markdown instruction file from a URL or local path.
- Pasting reusable instructions into an agent rules, memory, prompt, or custom-instructions file.

Use these stable public locations. Replace `<skill-name>` with `repo-plan` or `pit-crew-subagents`:

| Resource | URL |
| --- | --- |
| Skill folder | `https://github.com/lawgimenez/law-skills/tree/main/<skill-name>` |
| Raw skill file | `https://raw.githubusercontent.com/lawgimenez/law-skills/main/<skill-name>/SKILL.md` |
| Skill manifest | `https://raw.githubusercontent.com/lawgimenez/law-skills/main/skills.json` |

If you are installing from a branch or tag instead of `main`, replace `main` in the URL with that branch or tag.

## Generic Folder Install

Use this for any agent that has a local skills, rules, or custom-instructions directory:

```bash
agent_skills_dir="/path/to/your/agent/skills"
skill_name="pit-crew-subagents"
tmp_dir="$(mktemp -d)"
git clone --depth 1 https://github.com/lawgimenez/law-skills.git "$tmp_dir/law-skills"
mkdir -p "$agent_skills_dir"
cp -R "$tmp_dir/law-skills/$skill_name" "$agent_skills_dir/$skill_name"
rm -rf "$tmp_dir"
```

Restart or reload your agent after installation if it does not automatically detect new skill files.

## Generic Single-File Install

Use this for agents that accept one Markdown rules file but do not support skill folders:

```bash
skill_name="pit-crew-subagents"
curl -L "https://raw.githubusercontent.com/lawgimenez/law-skills/main/$skill_name/SKILL.md" \
  -o "$skill_name-skill.md"
```

Then add the downloaded Markdown file to your agent's custom instructions, reusable prompts, rules, or memory system.

## Agent-Specific Example

These skills are agent-neutral. Codex is one supported consumer; Codex users can ask:

```text
Use $skill-installer to install the pit-crew-subagents skill from https://github.com/lawgimenez/law-skills/tree/main/pit-crew-subagents
```

Restart Codex after installation so the new skill is loaded.

## Privacy

This repository should contain only portable skill files and repository-relative documentation. Do not commit local machine paths, secrets, tokens, private customer data, or environment-specific credentials.
