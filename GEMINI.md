# Git Helper Extension

This extension provides commands to help with Git workflows.

## Commands
All commands are located in `commands/gh/`.
- `/gh.commit`: Generates a semantic commit message for staged changes and commits them after approval.
- `/gh.review`: Reviews the code changes in the current branch.
- `/gh.changelog`: Generates a categorized changelog from recent semantic commits.
- `/gh.pr`: Summarizes changes and generates a Pull Request draft.
- `/gh.undo`: Safely helps you undo or revert the last Git action.
- `/gh.add`: Interactively steps through and stages changes.

## Standards
- Follow Conventional Commits for all generated messages.
- Prioritize correctness and security in reviews.
- Always ask for confirmation before executing `git commit`.
