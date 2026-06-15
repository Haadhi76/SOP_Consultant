# Statement of Purpose Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A Claude Code skill for writing, drafting, structuring, and revising Statements of Purpose (SOPs), personal statements, letters of intent, and MFA / creative-program personal statements for graduate-school, fellowship, and scholarship applications.

Built on peer-reviewed genre analysis of real, successful SOPs — not a template.

## What it does

- Drafts full SOPs from scratch, rescues weak existing drafts, or reviews and gives feedback on a draft the applicant already wrote
- Adapts to program type: taught master's, research/PhD, fellowship/scholarship, career change, MFA / creative programs
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

- Statement of Purpose / SOP / personal statement
- Grad-school application essay / admissions essay
- Motivation letter / letter of intent / research proposal
- Fellowship statement / scholarship essay / grant personal statement
- MFA or creative-program personal statement
- Reviewing or giving feedback on any of the above

You can also trigger it explicitly: *"Use the statement-of-purpose skill to help me write my SOP for [program]."*

## Directory structure

```
statement-of-purpose/
├── SKILL.md                               # Main skill — workflow, hard rules, file routing
└── references/
    ├── move-framework.md                  # Rhetorical move taxonomy + appeals (ethos/logos/pathos)
    ├── style-and-voice.md                 # Register, authenticity, anti-generic-AI guidance
    ├── revision-checklist.md              # Checklist for critiquing or polishing a draft
    ├── use-case-taught-masters.md         # Taught / coursework master's calibration
    ├── use-case-research-phd.md           # Research master's and doctoral calibration
    ├── use-case-career-change.md          # Career-pivot modifier (layered on top of degree case)
    ├── use-case-fellowship-scholarship.md # Fellowship and scholarship calibration
    ├── fluency-fluent-or-native.md        # Guidance for fluent / native-English writers
    ├── fluency-advanced-l2.md             # Guidance for advanced non-native writers
    └── fluency-developing-l2.md           # Guidance for writers still building academic English
```

## How the reference files are used

`SKILL.md` is the entry point. The reference files are **deltas** — they are loaded on top of the core, not instead of it.

- `move-framework.md` and `style-and-voice.md` are read for **every** SOP.
- `revision-checklist.md` is read before revising any draft.
- `SKILL.md` contains inline routing tables that map program type → `use-case-*.md` file and fluency level → `fluency-*.md` file. Claude selects and loads those files directly — all reference files are one level deep from `SKILL.md`.

## Hard rules

This skill does not invent credentials, faculty names, or program details. It does not help disguise authorship or defeat AI-detection systems. The applicant's own truthful material is the only raw material. See `SKILL.md` for the full list of non-negotiable constraints.

## Sources

Samraj & Monk (2008), Chiu (2015, 2016), López-Ferrero & Bach (2016), Ganguly (2020, Missouri S&T thesis; published in *Xchanges* 2021), and institutional advice from university graduate schools.
