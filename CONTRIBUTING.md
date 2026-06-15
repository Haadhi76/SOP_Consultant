# Contributing

Contributions are welcome — bug fixes, improved reference content, new use-case or fluency variants, and corrections to the research citations are all useful.

## What this skill is

A Claude Code skill that helps users write Statements of Purpose for graduate-school and fellowship applications. It follows the [Agent Skills Open Standard](https://agentskills.io/specification). The entry point is `SKILL.md`; all supporting content lives under `references/`.

## How to install locally for testing

```bash
git clone https://github.com/Haadhi76/SOP_Consultant.git
cp -r SOP_Consultant ~/.claude/skills/statement-of-purpose
```

Claude Code picks up skills automatically from `~/.claude/skills/` — no restart needed.

## Types of contributions

### Content fixes
Corrections to the research citations, typos, or factual errors in the reference files. Open a PR with the fix and a note on the source.

### Reference file improvements
Additions or corrections to `references/move-framework.md`, `references/style-and-voice.md`, `references/revision-checklist.md`, or the use-case / fluency leaf files. Ground claims in the cited literature where possible; if drawing on practitioner consensus, say so explicitly (the existing files model this convention).

### New use-case or fluency variants
New leaf files under `references/use-cases/` or `references/fluency/`. Follow the same delta format as the existing files — describe what changes relative to the base, not the full base workflow.

### SKILL.md changes
Changes to the main skill file affect every user. Keep the body under 500 lines. All file references must be one level deep from `SKILL.md` (i.e., `references/filename.md`, not `references/subdir/filename.md`).

## Workflow

1. Fork the repo and create a branch from `main`.
2. Make your changes.
3. Test the skill locally by triggering it in a Claude Code session.
4. Open a pull request. Describe what you changed and why.

## Style conventions

- Follow the description guidelines from the [Anthropic skill authoring docs](https://docs.anthropic.com/en/docs/agents-and-tools/agent-skills/best-practices): third-person, trigger-focused, no workflow summary in the description.
- Keep file references to one level deep from `SKILL.md`.
- Cite peer-reviewed sources where available. Mark practitioner guidance as such.
- No fabricated examples, credentials, or citations.

## Code of conduct

See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
