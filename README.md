# Statement of Purpose Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A Claude Code skill for writing, drafting, structuring, and revising Statements of Purpose (SOPs), personal statements, and letters of intent for graduate-school, fellowship, and scholarship applications.

Built on peer-reviewed genre analysis of real, successful SOPs — not a template.

## What it does

- Drafts full SOPs from scratch or rescues weak existing drafts
- Adapts to program type: taught master's, research/PhD, fellowship/scholarship, career change
- Adapts to the applicant's English-fluency level
- Grounds every essay in the applicant's own truthful material
- Applies the rhetorical move framework found in admitted-applicant SOPs

## Installation

Copy the skill into your Claude Code skills directory:

```
~/.claude/skills/statement-of-purpose/
```

The directory must contain `SKILL.md` and the full `references/` folder. Claude Code discovers skills by scanning that directory — no further configuration required.

## Triggering the skill

Claude will load this skill automatically when you mention:

- Statement of Purpose / SOP
- Personal statement
- Grad-school application essay
- Admissions essay / motivation letter
- Letter of intent

You can also trigger it explicitly: *"Use the statement-of-purpose skill to help me write my SOP for [program]."*

## Directory structure

```
statement-of-purpose/
├── SKILL.md                          # Main skill — workflow, hard rules, file routing
└── references/
    ├── move-framework.md             # Rhetorical move taxonomy + appeals (ethos/logos/pathos)
    ├── style-and-voice.md            # Register, authenticity, anti-generic-AI guidance
    ├── revision-checklist.md         # Checklist for critiquing or polishing a draft
    ├── use-cases/
    │   ├── README.md                 # Human reference: source notes and routing table
    │   ├── taught-masters.md         # Taught / coursework master's calibration
    │   ├── research-phd.md           # Research master's and doctoral calibration
    │   ├── career-change.md          # Career-pivot modifier (layered on top of degree case)
    │   └── fellowship-scholarship.md # Fellowship and scholarship calibration
    └── fluency/
        ├── README.md                 # Human reference: source notes and routing table
        ├── fluent-or-native.md       # Guidance for fluent / native-English writers
        ├── advanced-l2.md            # Guidance for advanced non-native writers
        └── developing-l2.md          # Guidance for writers still building academic English
```

## How the reference files are used

`SKILL.md` is the entry point. The reference files are **deltas** — they are loaded on top of the core, not instead of it.

- `move-framework.md` and `style-and-voice.md` are read for **every** SOP.
- `revision-checklist.md` is read before revising any draft.
- `SKILL.md` contains inline routing tables that map program type → use-case file and fluency level → fluency file. Claude selects and loads those files directly — no intermediate README hop.

The `use-cases/README.md` and `fluency/README.md` files are human-readable reference docs (source notes, extended routing rationale) and are not part of Claude's load path.

## Hard rules

This skill does not invent credentials, faculty names, or program details. It does not help disguise authorship or defeat AI-detection systems. The applicant's own truthful material is the only raw material. See `SKILL.md` for the full list of non-negotiable constraints.

## Sources

Samraj & Monk (2008), Chiu (2015, 2016), Ganguly (2020), López-Ferrero & Bach (2016), *Xchanges* (2021), and institutional advice from university graduate schools.
