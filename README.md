# Semantic Commit Helper Skill

This repository contains the `semantic-commit-helper` skill for the Gemini CLI agent.
This skill assists users in creating commit messages that adhere to the Conventional Commits specification.

## Features

- **Automated Analysis**: Analyzes staged changes (`git diff --staged`) to understand the "what".
- **Intent Gathering**: Asks the user for the "why" to ensure meaningful commit messages.
- **Conventional Commits**: Generates messages following the standard format (`type(scope): subject`).
- **Interactive Workflow**: Guides the user through staging, reviewing, and committing changes.

## Usage

To use this skill with the Gemini CLI agent:

1.  Ensure you are in this repository or have the skill configured in your agent's path.
2.  When you want to commit changes, simply ask the agent:
    > "Commit these changes"
    > "Help me commit"
3.  The agent will activate the `semantic-commit-helper` skill and guide you through the process.

## Skill Definition

The skill definition matches the prompt located in `.gemini/skills/semantic-commit-helper/SKILL.md`.
