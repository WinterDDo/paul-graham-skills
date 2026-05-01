# Paul Graham, Distilled

Two outputs from the same source material, serving two different purposes.

## What Is Inside

```
paul-graham-skills/
├── README.md             ← you are here
├── PRINCIPLES.md         ← human-readable essay: six principles for thinking and life
└── skills/               ← Claude Code skills: five behavioral disciplines for AI execution
    ├── plain-output-not-polished/
    ├── discover-not-persuade/
    ├── distrust-the-surface/
    ├── change-method-not-goal/
    └── mark-what-you-dont-know/
```

The two outputs come from different filters applied to the same body of essays.

**PRINCIPLES.md** is a compression of PG's work into six principles for *human cognition*. The filter: if you had ten minutes to transmit what matters most about how a person should think, work, and live, what would you say? Six is what survived. This is reading material — for humans, by humans.

**skills/** is a different compression, for *Claude*. The filter: what describes a discipline that an AI agent should embody when working with a user — something that addresses a specific Claude failure mode and produces measurable difference when applied? Five SKILL.md files, each loadable directly into Claude Code.

These are not the same content. They are different distillations because they answer different questions.

## The Five Skills

Each is a comprehensive SKILL.md with description, trigger conditions, behavioral instruction, push-back guidance, self-tests, and source essays.

1. **[plain-output-not-polished](skills/plain-output-not-polished/SKILL.md)** — Decoration covers seams. Plain prose is an honesty test.
2. **[discover-not-persuade](skills/discover-not-persuade/SKILL.md)** — Investigation and persuasion are opposite modes. Don't switch under pressure.
3. **[distrust-the-surface](skills/distrust-the-surface/SKILL.md)** — The user's request, the elegant solution, the clean dataset — all are hypotheses, not conclusions.
4. **[change-method-not-goal](skills/change-method-not-goal/SKILL.md)** — When stuck, the failed method is the problem. The first method is the least informed.
5. **[mark-what-you-dont-know](skills/mark-what-you-dont-know/SKILL.md)** — Distinguish direct evidence from pattern-match. They look identical from outside.

## The Six Principles (for humans)

For the essay-form distillation aimed at human readers, see **[PRINCIPLES.md](PRINCIPLES.md)**.

## Installation (Skills)

To make these skills available globally to Claude Code:

```bash
git clone https://github.com/WinterDDo/paul-graham-skills.git
cp -r paul-graham-skills/skills/* ~/.claude/skills/
```

Claude will auto-discover them at session start. The frontmatter `description` field tells Claude when each skill should activate.

To install only specific skills, copy individual directories:

```bash
cp -r paul-graham-skills/skills/discover-not-persuade ~/.claude/skills/
```

To use these in a single project rather than globally:

```bash
cp -r paul-graham-skills/skills/* /your/project/.claude/skills/
```

## Why Two Outputs

The original temptation was to make the skills *be* the principles for humans, in a different format. That was a category error. Principles for human cognition (curiosity, identity, what to work on) do not translate into AI execution skills, because they are about how to *select* — what to think about, what to pursue. AI execution skills are about how to *act* — what to do when the work is happening.

The two outputs preserve both. PRINCIPLES.md is for the question *how should I think and live?* The skills are for the question *how should Claude work?* Both are derivable from the same essays, but only by reading PG with two different intentions.

## Source

All ideas trace to essays by [Paul Graham](https://paulgraham.com/articles.html). Roughly 37 essays were read for these distillations. The principles and skills are PG's; the compression and packaging are the contribution.

## License

MIT. Use, fork, modify freely.
