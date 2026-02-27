# Gemini CLI Git Helper

A comprehensive extension and skill for [Gemini CLI](https://github.com/google/gemini-cli) designed to streamline Git workflows. It automates semantic commit message generation and provides deep code reviews using native Git commands.

## Features

- **Semantic Commit Generator (`/commit`)**:
  - Automatically analyzes staged changes (`git diff --staged`).
  - Generates commit messages following the [Conventional Commits](https://www.conventionalcommits.org/) specification.
  - Requires explicit user approval before executing the commit.
- **Deep Code Review (`/review`)**:
  - Reviews changes between branches or specific commits.
  - Identifies logic bugs, security vulnerabilities, and performance bottlenecks.
  - Provides actionable code suggestions in diff format.
- **Smart Staging (`/add`)**:
  - Interactively steps through and stages changes.
- **Pull Request Assistant (`/pr`)**:
  - Summarizes changes and generates a Pull Request draft.
- **Changelog Generator (`/changelog`)**:
  - Generates a categorized changelog from recent semantic commits.
- **Undo/Revert Helper (`/undo`)**:
  - Safely helps you undo or revert the last Git action.
- **Workflow Skill**:
  - Enhances the agent's native understanding of Git procedures.
  - Triggers on natural language requests like "Review my changes" or "Help me commit this."

## Installation

### 1. Install the Skill
The skill provides the procedural knowledge for the agent to handle Git tasks effectively.
```bash
gemini skills install https://github.com/A-K-6/geminicli-git-helper
```

### 2. Install the Extension
The extension adds specific commands like `/commit`, `/review`, `/add`, `/pr`, `/changelog`, and `/undo` to your CLI.
```bash
gemini extensions install https://github.com/A-K-6/geminicli-git-helper
```

### 3. Reload
If you are already in an interactive Gemini CLI session, reload to enable the new features:
```bash
/skills reload
/extensions reload
```

## Gallery & Discoverability

To make this extension and skill discoverable in the Gemini CLI gallery, ensure the following topics are added to your GitHub repository:
- `gemini-extension`
- `gemini-skill`

## Development

- `PRD.md`: Project Requirements Document.
- `devlog.md`: Development history and progress.
- `gemini-extension.json`: Extension manifest.
- `GEMINI.md`: Extension context/playbook.
- `SKILL.md`: Skill definition and workflow.
- `commands/`: Custom slash commands.

## License
MIT
