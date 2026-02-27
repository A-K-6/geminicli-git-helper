---
name: git-helper
description: Git assistant for generating semantic commits and performing code reviews. Use when the user wants to commit changes, review pull requests, or needs help with Git workflows.
---

# Git Helper

## Overview
This skill helps you manage Git workflows efficiently. It specializes in:
1. **Semantic Commit Generation**: Analyzing staged changes and creating meaningful commit messages following Conventional Commits.
2. **Code Review**: Performing deep analysis of changes to identify bugs, performance issues, and architectural improvements.

## Workflow Decision Tree

### 1. Generating a Commit
When the user wants to commit changes:
1. **Check Staged Changes**: Run `git diff --staged` to see what is being committed.
2. **Check Unstaged Changes**: Run `git diff` to see if there are important changes not yet staged. If so, inform the user.
3. **Generate Message**: Analyze the staged changes and generate a commit message following the [Conventional Commits](https://www.conventionalcommits.org/) specification (e.g., `feat: add user authentication`).
4. **Present and Confirm**: Show the proposed message to the user and ask for permission to commit.
5. **Execute**: If approved, run `git commit -m "<message>"`.

### 2. Reviewing Changes (PR Review)
When the user wants to review changes (e.g., "review this PR" or "review my changes"):
1. **Identify Range**: Determine the branch or commit range to review. Default to `main...HEAD` if not specified.
2. **Get Diff**: Run `git diff -U5 <range>`.
3. **Analyze**:
   - Summarize the intent of the changes.
   - Look for logic bugs, security risks, and performance bottlenecks.
   - Check for architectural consistency and readability.
4. **Feedback**: Provide structured feedback with severity levels (CRITICAL, HIGH, MEDIUM, LOW) and suggested code changes.

### 3. Generating a Changelog
When the user wants to generate release notes:
1. **Identify Range**: Find the last tag or specified commit range.
2. **Analyze Commits**: Parse commit messages for semantic types.
3. **Format**: Group by type and format as Markdown.
4. **Update File**: Ask to prepend to `CHANGELOG.md`.

### 4. Pull Request Assistant
When the user wants to prepare a PR:
1. **Gather Data**: Get diff stats and commit list.
2. **Generate Draft**: Create a structured title and description.
3. **GitHub CLI**: If available, offer to create the PR directly.

### 5. Safe Undo
When the user wants to "undo" something:
1. **Diagnose**: Analyze `git status` and recent history.
2. **Clarify**: Identify what specifically should be undone.
3. **Safe Command**: Propose the specific `reset`, `revert`, or `restore` command.

### 6. Smart Staging
When the user wants to stage changes:
1. **Iterate**: Go through unstaged changes file by file.
2. **Explain & Stage**: Explain the change and ask for confirmation to stage.

## Guidelines for Commit Messages
- **Format**: `<type>(<scope>): <description>`
- **Types**: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`.
- **Subject**: Use imperative, present tense ("change" not "changed" nor "changes"). No period at the end.

## Guidelines for Reviews
- **Context**: Read relevant files beyond the diff to understand dependencies.
- **Actionable**: Provide concrete code suggestions in diff format.
- **Objective**: Focus on substantive issues over stylistic nits.
