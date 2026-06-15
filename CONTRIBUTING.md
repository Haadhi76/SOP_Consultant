# Contributing

Contributions are welcome — bug fixes, improved reference content, new use-case or fluency variants, and corrections to the research citations are all useful.

## What this skill is

An agent skill — following the [Agent Skills open standard](https://agentskills.io/specification) — that helps users write Statements of Purpose for graduate-school and fellowship applications. It works with any compatible agent (Claude Code, Codex CLI, Gemini CLI, Antigravity, OpenCode, and others). The entry point is `SKILL.md`; all supporting content lives under `references/`.

## How to install locally for testing

Clone into the skills directory for your agent (folder name must be `statement-of-purpose`):

```bash
# Claude Code
git clone https://github.com/Haadhi76/SOP_Consultant.git \
  ~/.claude/skills/statement-of-purpose

# Codex CLI
git clone https://github.com/Haadhi76/SOP_Consultant.git \
  ~/.agents/skills/statement-of-purpose

# OpenCode
git clone https://github.com/Haadhi76/SOP_Consultant.git \
  ~/.config/opencode/skills/statement-of-purpose
```

Agents discover skills automatically from these paths — no restart needed.

## Types of contributions

### Content fixes
Corrections to the research citations, typos, or factual errors in the reference files. Open a PR with the fix and a note on the source.

### Reference file improvements
Additions or corrections to `references/move-framework.md`, `references/style-and-voice.md`, `references/revision-checklist.md`, or the use-case / fluency leaf files. Ground claims in the cited literature where possible; if drawing on practitioner consensus, say so explicitly (the existing files model this convention).

### New use-case or fluency variants
New leaf files under `references/` with the `use-case-` or `fluency-` prefix (e.g. `references/use-case-mba.md`). Follow the same delta format as the existing files — describe what changes relative to the base, not the full base workflow.

### SKILL.md changes
Changes to the main skill file affect every user. Keep the body under 500 lines. All file references must be one level deep from `SKILL.md` (i.e., `references/filename.md`, not `references/subdir/filename.md`).

## Workflow

1. Fork the repo and create a branch from `main`.
2. Make your changes.
3. Test the skill locally by triggering it in a session with your agent of choice.
4. Open a pull request. Describe what you changed and why.

## Style conventions

- Follow the [Agent Skills specification](https://agentskills.io/specification) for frontmatter: `name` matches the folder name, `description` is third-person, trigger-focused, and contains no workflow summary.
- Keep file references to one level deep from `SKILL.md`.
- Cite peer-reviewed sources where available. Mark practitioner guidance as such.
- No fabricated examples, credentials, or citations.

## Code of conduct

See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
