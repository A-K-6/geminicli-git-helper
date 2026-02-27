# PRD - Gemini CLI Git Helper

## Overview
A Gemini CLI extension and skill designed to assist users with Git workflows, specifically focusing on generating semantic commit messages and performing code reviews for pull requests.

## Objectives
- Automate the generation of commit messages based on staged changes.
- Provide a structured way to review code changes (PR reviews) using native Git commands.
- Ensure all actions require user confirmation.
- Rely primarily on native `git` commands.

## Key Features
1. **Commit Generator**:
   - Analyze staged changes using `git diff`.
   - Generate a semantic commit message.
   - Execute `git commit -m "<message>"` after user approval.
2. **Reviewer**:
   - Review changes between branches or specific commits.
   - Provide feedback on code quality, potential bugs, and style.
   - Use `git diff` and `git log` to gather context.

## Implementation Status
- **Skill**: Completed and packaged as `git-helper.skill`.
- **Extension**: Completed in the `extension/` directory.
- **Commands**: 
  - All git commands are located in `commands/git-helper/`.
  - `/commit`: Semantic commit generator.
  - `/review`: Detailed code reviewer.
  - `/changelog`: Automated release notes generator.
  - `/pr`: Pull Request assistant.
  - `/undo`: Safe Git undo/revert helper.
  - `/add`: Smart interactive staging.

## Installation Instructions
### Skill
```bash
gemini skills install ./git-helper.skill
```

### Extension
```bash
gemini extensions install ./extension
```
