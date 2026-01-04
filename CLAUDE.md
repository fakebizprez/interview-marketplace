# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Claude Code plugin that provides interview-driven strategic roadmap planning. It scans existing codebases, conducts developer interviews using `AskUserQuestionTool`, and generates prioritized development roadmaps with dependency tracking.

## Plugin Structure

```
plugin.json              # Plugin manifest (name, version, author)
plugins/
  interview-mode/
    commands/
      interview-roadmap.md   # Scans codebase + interviews → roadmap specs
      interview-spec.md      # Deep-dive interview for specific feature spec
```

## Commands

- `/interview-roadmap` - Scans codebase architecture, interviews developer about priorities/constraints, generates spec files in `.claude/roadmap/` with dependency graph
- `/interview-spec [plan]` - Reads `.claude/roadmap/$ARGUMENTS.md` and conducts detailed implementation interview before writing final spec

## Command Development

Commands are markdown files with YAML frontmatter:
- `name` - command name (matches filename)
- `description` - shown in command list
- `model` - which model to use (e.g., `opus`)
- `argument-hint` - placeholder text for arguments

The markdown body contains the prompt/instructions executed when the command runs.
