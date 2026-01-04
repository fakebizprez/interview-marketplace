---
name: interview-add-to-roadmap
description: Interview to add a single new spec to the roadmap
model: opus
---

## Step 1: Understand Existing Roadmap

Read all files in `.claude/roadmap/` to understand:

- Existing specs and their numbering (e.g., `01-auth.md`, `02-dashboard.md`)
- Current priorities (P0/P1/P2)
- Dependencies between specs
- The overall roadmap structure from `roadmap.toml`
- Gaps or opportunities that haven't been addressed

## Step 2: Interview for New Spec

Use AskUserQuestionTool to conduct an open-ended, in-depth interview about the new feature they want to add. There is no limit to the number of questions—the goal is to build the best possible spec.

Be curious. Follow threads that seem interesting. Ask follow-up questions. Dig deeper on vague answers. Challenge assumptions. Let the conversation guide you toward what matters most for this particular feature.

Continue until you have a complete picture.

## Step 3: Create the Spec File

Based on the interview, create a new spec file in `.claude/roadmap/`:

- Use the next available number (e.g., if `04-*.md` exists, create `05-*.md`)
- Choose a clear, descriptive kebab-case name
- Include:
  - **Overview**: What this feature does and why
  - **Priority**: P0/P1/P2 with justification
  - **Dependencies**: Which specs must come before/after
  - **Technical approach**: High-level implementation strategy
  - **Key decisions**: Important choices made during interview
  - **Scope**: What's in and what's explicitly out
  - **Success criteria**: How we know it's done
  - **Risks/unknowns**: What could go wrong

## Step 4: Update Roadmap Overview

Update `.claude/roadmap/roadmap.toml` to:

- Add the new spec entry
- Adjust implementation order if needed

## Guidelines

- Ask strategic, non-obvious questions
- Focus on "why" and tradeoffs, not just "what"
- Don't rush—thorough discovery leads to better specs
- Respect existing architecture and roadmap structure
- Make dependencies explicit
- The goal is to build a fantastic spec.
