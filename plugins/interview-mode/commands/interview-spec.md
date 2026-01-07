---
name: interview-spec
description: Interview me about the plan
argument-hint: [plan]
model: opus
---

Read the plan file at `.claude/planning/roadmap/$ARGUMENTS.md` and interview me in detail using the AskUserQuestionTool about literally anything: technical implementation, UI & UX, concerns, tradeoffs, etc. Make sure the questions are not obvious.

Be very in-depth and continue interviewing me until complete, then write the spec to the file `./claude/planning/spec/$ARGUMENTS-{{spec}}.md`