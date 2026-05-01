# Paul Graham Skills

Six principles distilled from Paul Graham's two decades of essays, packaged as Claude Code skills. Loadable. Composable. Loop-ready.

This project does for PG what [andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills) did for Karpathy: it takes a body of work that everyone knows is important, and turns it into something you can actually feed to a Claude agent and have it apply in real conversations.

## What Is Inside

```
paul-graham-skills/
├── README.md            ← you are here
├── PRINCIPLES.md        ← the essay-form distillation, for humans
└── skills/
    ├── follow-genuine-curiosity/
    │   └── SKILL.md
    ├── optimize-the-thing-not-the-metric/
    │   └── SKILL.md
    ├── keep-identity-small/
    │   └── SKILL.md
    ├── work-on-the-right-thing/
    │   └── SKILL.md
    ├── write-to-finish-thinking/
    │   └── SKILL.md
    └── start-before-ready/
        └── SKILL.md
```

Each `SKILL.md` is a self-contained skill file with YAML frontmatter that Claude can load to decide when to invoke the principle, and content that tells Claude how to apply it in conversation.

## The Six Principles

1. **[Follow Genuine Curiosity (Not Prestige)](skills/follow-genuine-curiosity/SKILL.md)** — Curiosity is the engine, not the fuel.
2. **[Optimize for the Thing, Not the Metric](skills/optimize-the-thing-not-the-metric/SKILL.md)** — Effort that *looks* like progress is the most dangerous form of waste.
3. **[Keep Identity Small](skills/keep-identity-small/SKILL.md)** — The more labels you claim, the dumber they make you.
4. **[What You Work On Matters More Than How Hard You Work](skills/work-on-the-right-thing/SKILL.md)** — The choice of problem is the most important decision.
5. **[An Idea Is Not Finished Until It Is Written](skills/write-to-finish-thinking/SKILL.md)** — Writing is not how you express thoughts; it is how you find out what you think.
6. **[Good Work Compounds — Start Before You Are Ready](skills/start-before-ready/SKILL.md)** — You will never feel ready. Readiness is downstream of doing the work.

For the full essay-form treatment, see [PRINCIPLES.md](PRINCIPLES.md).

## Installation

To make these skills available globally to Claude Code:

```bash
git clone https://github.com/WinterDDo/paul-graham-skills.git
cp -r paul-graham-skills/skills/* ~/.claude/skills/
```

Claude will auto-discover the skills at session start. The frontmatter `description` field tells Claude when each skill should activate.

To install only specific principles, copy individual skill directories:

```bash
cp -r paul-graham-skills/skills/keep-identity-small ~/.claude/skills/
```

To use these in a single project rather than globally:

```bash
cp -r paul-graham-skills/skills/* /your/project/.claude/skills/
```

## Why Skills, Not Just Essays

PG's essays are already widely read. Knowing the ideas is not the bottleneck. The bottleneck is invoking them at the right moment — when you are about to commit to a prestigious-but-hollow project, when you are about to optimize the wrong metric, when identity is quietly capturing your reasoning.

A skill file is a trigger. The frontmatter description tells Claude when the principle is relevant in the conversation. The content tells Claude what to do when it activates. That is the difference between *knowing* a principle and *applying* it.

## How These Were Distilled

Source material: 18 of PG's most thinking-oriented essays plus several auxiliary pieces (Founder Mode, How to Disagree, The Right Kind of Stubborn, Four Quadrants of Conformism, A Project of One's Own).

The distillation followed a strict three-domain test: a candidate principle had to apply meaningfully in at least three unrelated contexts (software development, business strategy, personal life decisions) to qualify. Principles that worked in only one domain were treated as instances rather than principles.

The goal was not to produce a comprehensive index of PG's ideas. It was to find the smallest set of ideas that, if internalized, would change how a thinking person operates. Six is what survived the cut.

## Contributing

Found a principle that should be added or refined? Open an issue. The bar is the same: it has to pass the three-domain test, and it cannot be already covered by an existing skill.

## Source

All ideas trace to essays by [Paul Graham](https://paulgraham.com/articles.html). This project distills them into a form Claude can actually use during collaboration. The principles are PG's; the packaging is the contribution.

## License

MIT. Use, fork, modify freely.
