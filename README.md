# socratic-comprehension

A Socratic sparring-partner Agent Skill that helps you understand a difficult text, paper, or concept **to the point where you can explain it in your own words.**

It never summarizes or ghost-writes for you. Understanding only happens when you rebuild the logic yourself and put it into words — so this skill withholds the answer, makes you reconstruct, and pushes back sharply on how you phrase it.

## What it does

- **Separates the goal first** — figures out whether you want to *understand* or just want a *deliverable*
- **Shows the whole shape first** — breaks the target into reasoning steps (nodes) and lays out the path before starting
- **One node at a time** — prompts "restate this in your own words" and never writes the answer first
- **Names the drifting word** — pinpoints exactly where your wording slipped from the original meaning, not a vague "a little off"
- **Makes you grasp the crux** — has you resolve the underlying premise and central tension yourself
- **Term test** — checks whether you can define each key term in one sentence without borrowing the original phrasing
- **Critique layer** — separates "description" from "position-taking" and draws out your doubts and counterarguments (understanding ≠ agreement)

## When it activates

It triggers when you ask to understand or internalize something for yourself — e.g. "what does this mean", "I want to understand this myself", "help me make this click", "I want to organize this for my own use", "break this down". It also fires on the Japanese equivalents (「これどういうこと」「腹落ちさせたい」「噛み砕きたい」など). It does **not** fire when you clearly ask for a deliverable ("summarize this", "write an article") — instead it confirms your goal once before proceeding.

## Installation

Pick whichever fits your setup. For a **personal** install (available in every project), use a global/user-level option.

### Claude Code plugin (marketplace)

```
/plugin marketplace add kpab/socratic-comprehension
/plugin install socratic-comprehension
```

### skills.sh CLI (`npx skills`)

Via the [skills.sh](https://skills.sh) CLI ([vercel-labs/skills](https://github.com/vercel-labs/skills)). No install needed — run it with `npx`.

```
# Personal (user-level) install — works in every project:
npx skills add kpab/socratic-comprehension --global

# Or project-local (installs into the current directory):
npx skills add kpab/socratic-comprehension
```

> **Note:** without `--global`, the CLI installs **project-local** into the directory you run it from (`./.agents/skills/` plus a `.claude/skills/` symlink), *not* into `~/.claude/skills/`. If the skill "doesn't show up," you most likely want `--global`.

### Manual copy

Copy `skills/socratic-comprehension/` into your skills directory:

```
# Personal:
~/.claude/skills/socratic-comprehension/

# Project-only:
<project>/.claude/skills/socratic-comprehension/
```

## Structure

```
.
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
└── skills/
    └── socratic-comprehension/
        └── SKILL.md
```

## License

MIT © 2026 kpab
