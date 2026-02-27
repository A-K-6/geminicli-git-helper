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
- `/gh.sync`: Fetches updates and analyzes potential conflicts before merging or rebasing.
- `/gh.fixup`: Identifies 'fixup!' commits and offers to automatically squash them using interactive rebase.
- `/gh.bisect`: Guides the user through git bisect to find the commit that introduced a bug.
- `/gh.worktree`: Manages Git worktrees for easy context switching without stashing.
- `/gh.explain`: Explains the 'why' behind a change by analyzing commit history and context.

## Standards
- Follow Conventional Commits for all generated messages.
- Prioritize correctness and security in reviews.
- Always ask for confirmation before executing `git commit`.
