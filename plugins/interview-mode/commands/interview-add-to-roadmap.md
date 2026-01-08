---
name: interview-add-to-roadmap
description: Interview to add a single new spec to the roadmap
model: opus
---

## Step 1: Understand Existing Roadmap

Read `.claude/planning/roadmap/roadmap.toml` and scan existing spec files to understand:

- Current numbering scheme (e.g., `01-auth.md`, `02-dashboard.md`)
- Existing priorities and dependencies
- Where this new item fits

## Step 2: Quick Capture Interview

Use AskUserQuestionTool to ask **2-4 focused questions** to capture:

1. **What** is this feature? (one sentence)
2. **Why** does it matter? (the problem it solves)
3. **Priority** relative to existing items
4. **Dependencies** on other roadmap items

Keep it brief. This is idea capture, not implementation planning.

## Step 3: Create Roadmap Entry

Create a new file in `.claude/planning/roadmap/`:

- Use next available number (e.g., `05-feature-name.md`)
- Keep it concise:

```markdown
# Feature Name

## Overview
1-2 paragraphs: what this does and why it matters.

## Priority
P0/P1/P2 with one-sentence justification.

## Dependencies
- Requires: [list specs that must come first]
- Enables: [list specs that depend on this]

## Scope Boundaries
- **In**: [key things included]
- **Out**: [explicitly excluded for now]
```

## Step 4: Update Roadmap

Add the new entry to `.claude/planning/roadmap/roadmap.toml`.

## Guidelines

- **This is quick capture, not spec building.** Keep it under 5 minutes.
- Save deep technical details for `/interview-spec` when ready to implement.
- Focus on "what" and "why", defer "how" to spec phase.
- One paragraph beats three. Brevity is a feature.
