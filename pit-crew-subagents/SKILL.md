---
name: pit-crew-subagents
description: Assign random pre-2005 metal, hardcore, punk, post-hardcore, metalcore, grindcore, or crossover band codenames to focused agent subagents or helper agents. Use whenever an agent will spawn, name, rename, describe, or coordinate delegated helpers, especially security, performance, regression, architecture, refactor, CI, or audit investigations where helper names are visible.
license: MIT
metadata:
  owner: Lawrence Gimenez
---

# Pit Crew Subagents

Use this skill to make subagent or helper-agent names more memorable while keeping each assignment clear and professional. This skill is agent-neutral: use it with any assistant or automation system that supports delegated subagents, helper agents, workers, reviewers, investigators, or similar focused roles.

## Agent-Neutral Usage

- Apply these rules to the visible name, label, or assignment title for each delegated helper.
- If the platform uses a different term, such as worker, reviewer, helper, or investigator, keep the platform term in the surrounding instructions and still use the naming format below.
- The band name is flavor only. The role is the functional part of the name and must stay understandable without extra explanation.
- This skill does not require Codex and should not depend on Codex-specific tools, thread behavior, or syntax.

## Naming Rules

1. Use this skill only when subagents or delegated helpers are already warranted by the active instructions or the user explicitly asks to name them.
2. Do not spawn extra subagents or helpers just to use a band name.
3. Do not override a user-provided subagent, helper, worker, reviewer, or investigator name.
4. Name each delegated helper with this format: `<Band Name> <Role>`.
5. Keep the role specific to the assignment, such as `Security Reviewer`, `Performance Investigator`, `Regression Analyst`, `CI Investigator`, `Architecture Reviewer`, `Refactor Planner`, or `Accessibility Auditor`.
6. Choose a different band for each delegated helper in the same task unless the pool is exhausted.
7. Use bands formed before 2005. If unsure whether a band qualifies, pick another name from the pool.
8. Preserve common band capitalization. Drop punctuation only when it makes the subagent name easier to read.
9. Avoid names that are likely to distract in the task context, including shock-value, slur-like, or unusually sensitive names.

## Preferred Band Pool

Use this curated pool first. The bands are pre-2005 and readable as delegated-helper prefixes.

### Metal

- Black Sabbath
- Judas Priest
- Iron Maiden
- Motorhead
- Metallica
- Megadeth
- Anthrax
- Pantera
- Sepultura
- Carcass
- Morbid Angel
- Entombed
- At the Gates
- Meshuggah
- Neurosis
- Converge
- Botch
- Cave In
- Mastodon
- High on Fire
- The Haunted
- Opeth
- Baroness
- Lamb of God

### Hardcore and Metalcore

- Minor Threat
- Bad Brains
- Black Flag
- Agnostic Front
- Sick of It All
- Gorilla Biscuits
- Youth of Today
- Cro-Mags
- Judge
- Quicksand
- Integrity
- Earth Crisis
- Snapcase
- Hatebreed
- Terror
- Bane
- Have Heart
- Throwdown
- Poison the Well
- Zao
- Shai Hulud
- Every Time I Die
- Dillinger Escape Plan
- Norma Jean

### Punk and Post-Hardcore

- Ramones
- The Clash
- Buzzcocks
- The Damned
- X
- Bad Religion
- Descendents
- Jawbreaker
- Fugazi
- Rites of Spring
- Drive Like Jehu
- Refused
- At the Drive-In
- Hot Water Music
- Alkaline Trio
- Against Me
- The Bronx
- Rocket From the Crypt
- Husker Du
- Minutemen
- Operation Ivy
- Rancid
- NOFX

## Examples

- `Converge Security Reviewer`
- `Power Trip Performance Investigator` is not allowed because Power Trip formed after 2004; use `Mastodon Performance Investigator` instead.
- `Minor Threat Regression Analyst`
- `Botch Architecture Reviewer`
- `Fugazi Refactor Planner`
- `Bad Brains CI Investigator`
- `Snapcase Test Auditor`
- `At the Drive-In Accessibility Auditor`
