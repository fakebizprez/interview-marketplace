---
name: interview-roadmap
description: Scan codebase and create development roadmap
model: opus
---

## Step 1: Scan the Codebase

Understand the following aspects:

- Current architecture and tech stack
- Database schema and migrations
- Existing patterns and conventions (even if inconsistent)
- Incomplete features or TODOs
- Technical debt areas
- Recent development patterns
- What's working well vs what's problematic
- Legacy code that may have hidden business logic
- Workflows
- Integrations

## Step 2: Interview the Developer

Use AskUserQuestionTool to interview me about:

- Feature requests from users/stakeholders
- Technical debt that's blocking progress
- Which existing patterns should we preserve vs refactor
- Why certain architectural decisions were made
- Integration requirements
- Performance or scalability concerns
- UI/UX improvements needed
- What's off-limits to change
- ANYTHING you think is relevant

## Step 3: Create Prioritized Roadmap

Based on the scan and interview, create a prioritized roadmap by generating separate spec files in `.claude/roadmap/`:

- `{feature-name-01}.md`, `{feature-name-02}.md`, etc. for each major initiative
- Include dependencies between specs
- Assign rough priority (P0/P1/P2)
- Note which specs require refactoring existing code vs greenfield
- Order them logically (prerequisites first)

## Step 4: Create Roadmap Overview

Create `.claude/roadmap/00-roadmap.md` with:

- Overview of all specs
- Dependency graph as mermaid diagram
- Recommended implementation order
- Notes on brownfield considerations

## Guidelines

- Make sure questions are strategic, not obvious
- Focus on "why" and tradeoffs, not just "what"
- Respect existing architecture unless there's clear justification for change
