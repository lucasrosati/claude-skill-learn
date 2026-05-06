# claude-skill-learn

> **Teach any topic to Claude Code using the Feynman Technique.** One slash command. Any domain.

[🇧🇷 Leia em Português](./README.pt-br.md)

---

## Table of Contents

1. [What is this](#what-is-this)
2. [Usage](#usage)
3. [Response structure](#response-structure)
4. [Installation](#installation)
5. [Contributing](#contributing)

---

## What is this

A custom skill for Claude Code that applies the Feynman Technique to any topic you want to learn.

Feynman's idea: if you can't explain it to a smart non-expert, you haven't understood it yet. This skill forces that process — simple explanation first, concrete analogy with explicit mapping, the mechanism underneath, where the simple version lies, common misconceptions, and active questions that force you to apply the concept rather than just repeat it.

---

## Usage

```
/learn "transformers"
/learn garbage collector
/learn how a database index works
```

Works for any domain: CS, math, physics, ML, economics, philosophy, distributed systems.

---

## Response structure

1. **Simple explanation** — no jargon, the core idea in plain language
2. **Central analogy** — concrete and everyday, with explicit mapping to the concept
3. **How it actually works** — the mechanism, the "why" behind the simple version
4. **Where the simple version lies** — what the simplification cut or distorted
5. **Common pitfalls** — misconceptions that show up in interviews, exams, or production bugs
6. **Active test** — 2-3 questions that require applying the concept, not reciting it

---

## Installation

**Option A: project-level (one project only)**

```bash
mkdir -p .claude/commands
cp learn.md .claude/commands/learn.md
```

**Option B: global (available in every project)**

```bash
mkdir -p ~/.claude/commands
cp learn.md ~/.claude/commands/learn.md
```

Then invoke inside Claude Code:

```
/learn "your topic here"
```

---

## Structure

```
claude-skill-learn/
├── learn.md       # The skill file
└── README.md
```
