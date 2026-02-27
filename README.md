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
The extension adds specific `/commit` and `/review` commands to your CLI.
```bash
gemini extensions install https://github.com/A-K-6/geminicli-git-helper
```

### 3. Reload
If you are already in an interactive Gemini CLI session, reload to enable the new features:
```bash
/skills reload
/extensions reload
```

## Publishing to the Gallery

To have this extension automatically discovered and listed in the [Gemini CLI Extensions Gallery](https://geminicli.com/extensions):

1. Ensure the repository is **public**.
2. Go to your repository settings on GitHub.
3. In the **About** section, add the topic: `gemini-cli-extension`.

The Gemini CLI crawler will automatically find the `gemini-extension.json` at the root and add it to the gallery.

## Development

- `PRD.md`: Project Requirements Document.
- `devlog.md`: Development history and progress.
- `gemini-extension.json`: Extension manifest.
- `GEMINI.md`: Extension context/playbook.
- `SKILL.md`: Skill definition and workflow.
- `commands/`: Custom slash commands.

## License
MIT
