# Law Skills

Public, portable agent skills maintained by Lawrence Gimenez.

## Available Skills

| Skill | Description |
| --- | --- |
| `repo-plan` | Writes, reviews, and revises planning-only Markdown documents in a repository's `plans/` folder. |

## Install in Any Agent

The skills in this repository are plain Markdown folders. Any agent can use them if it supports one of these patterns:

- Loading a folder-based skill that contains `SKILL.md`.
- Loading a Markdown instruction file from a URL or local path.
- Pasting reusable instructions into an agent rules, memory, prompt, or custom-instructions file.

Use these stable public locations after the repository is published:

| Resource | URL |
| --- | --- |
| Skill folder | `https://github.com/lawgimenez/law-skills/tree/main/repo-plan` |
| Raw skill file | `https://raw.githubusercontent.com/lawgimenez/law-skills/main/repo-plan/SKILL.md` |
| Skill manifest | `https://raw.githubusercontent.com/lawgimenez/law-skills/main/skills.json` |

If you are installing from a branch or tag instead of `main`, replace `main` in the URL with that branch or tag.

## Generic Folder Install

Use this for any agent that has a local skills, rules, or custom-instructions directory:

```bash
agent_skills_dir="/path/to/your/agent/skills"
tmp_dir="$(mktemp -d)"
git clone --depth 1 https://github.com/lawgimenez/law-skills.git "$tmp_dir/law-skills"
mkdir -p "$agent_skills_dir"
cp -R "$tmp_dir/law-skills/repo-plan" "$agent_skills_dir/repo-plan"
rm -rf "$tmp_dir"
```

Restart or reload your agent after installation if it does not automatically detect new skill files.

## Generic Single-File Install

Use this for agents that accept one Markdown rules file but do not support skill folders:

```bash
curl -L https://raw.githubusercontent.com/lawgimenez/law-skills/main/repo-plan/SKILL.md \
  -o repo-plan-skill.md
```

Then add `repo-plan-skill.md` to your agent's custom instructions, reusable prompts, rules, or memory system.

## Codex Example

Codex users can ask:

```text
Use $skill-installer to install the repo-plan skill from https://github.com/lawgimenez/law-skills/tree/main/repo-plan
```

Restart Codex after installation so the new skill is loaded.

## Privacy

This repository should contain only portable skill files and repository-relative documentation. Do not commit local machine paths, secrets, tokens, private customer data, or environment-specific credentials.
