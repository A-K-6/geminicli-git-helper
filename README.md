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

## Usage

### Commands
- `/commit`: Analyze staged changes and commit them with a generated message.
- `/review`: Review the changes in the current branch against the base branch.

### Natural Language
Because of the `git-helper` skill, you can also use natural language:
- "Look at my staged changes and suggest a commit message."
- "Perform a code review on this PR."
- "What's the difference between my branch and main?"

## Development

- `PRD.md`: Project Requirements Document.
- `devlog.md`: Development history and progress.
- `git-helper/`: Source directory for the skill.
- `extension/`: Source directory for the extension commands.

## License
MIT
