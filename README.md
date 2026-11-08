# claude-cc-skill-strategic-compact-skill

A Claude Code skill focused on strategic compaction of development context so long-running work can continue with less noise and fewer repeated details.

## Overview

Long development sessions accumulate decisions, implementation details, logs, and exploratory notes. Not all of that information needs to remain in active context. Strategic compaction means preserving the information required for the next steps while reducing low-value detail.

The current skill definition is intentionally concise. This README describes the intended context-management use and should be read together with `SKILL.md`.

## Why Strategic Compaction Matters

- Long sessions can accumulate redundant information.
- Repeated details consume context without improving decisions.
- Important constraints can become difficult to locate.
- Exploratory paths may no longer be relevant.
- Work may need to continue after a context reset or handoff.

## What to Preserve

A useful compact project summary should retain:

- The current objective.
- Important user requirements and constraints.
- Decisions already made and why.
- Files and components changed.
- Current implementation state.
- Tests already run and their results.
- Known bugs and unresolved questions.
- Next actions in priority order.

## What to Reduce

Consider removing or summarizing:

- Repeated explanations.
- Failed approaches that are no longer relevant.
- Large raw logs after extracting the important error.
- Temporary exploration notes.
- Details already recorded in stable project documentation.
- Unrelated conversation history.

Do not remove a failed approach if it explains an important constraint or prevents repeating a costly mistake.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-cc-skill-strategic-compact-skill.git ~/.claude/skills/cc-skill-strategic-compact
```

## Usage

Use the skill when a development session is becoming long or when preparing a handoff:

```text
/cc-skill-strategic-compact
```

Review `SKILL.md` for the exact skill instructions.

## Suggested Compact Summary

```markdown
# Current Work

## Objective
What the project is trying to achieve.

## Constraints
Requirements that must not be violated.

## Decisions
Important choices and their rationale.

## Implementation State
Files changed and current behavior.

## Validation
Commands run and actual results.

## Open Issues
Known failures and unresolved questions.

## Next Steps
Ordered actions to continue the work.
```

## Quality Checklist

- Summary is understandable without the full conversation.
- User requirements are preserved accurately.
- Decisions and constraints are explicit.
- Current implementation state is factual.
- Test results are not overstated.
- Open issues are visible.
- Next steps are actionable.
- Important context is not discarded.

## Repository Contents

- `SKILL.md`: Main strategic compaction skill definition.
- `suggest-compact.sh`: Helper script for the configured compaction workflow.
- `README.md`: Context preservation guidance and summary structure.

## Practical Principle

Compact context, not meaning. The best summary is short enough to be useful and complete enough that the next step can proceed without guessing.
