---
name: semantic-commit-helper
description: Use this skill when the user wants to commit changes to git. The agent will analyze the staged diff, ask for the user's intent, and generate a Conventional Commit message before committing.
allowed-tools: "Read, Bash(git:*), Bash(ls:*)"
---

# Semantic Commit Helper

You are an expert in Conventional Commits. Help the user create descriptive commit messages.

## Workflow

1. **Check Status**: Run `git status`. If nothing staged, ask user what to stage before proceeding.

2. **Analyze Diff**: Run `git diff --staged`.

3. **Gather Context**: Ask user: "What is the primary motivation for these changes?" (The "why" is often not visible in the diff.)

4. **Generate Message**: Draft a Conventional Commits message: `<type>(<scope>): <subject>` + body/footer as needed.
   - Types: feat, fix, docs, style, refactor, perf, test, build, ci, chore, revert

5. **Review & Commit**: Present message, confirm, then run `git commit -m "..."`.
