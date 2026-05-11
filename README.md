# Claude_code_testing

A sandbox repository for testing and demonstrating [Claude Code](https://claude.com/claude-code) behavior on GitHub issues and pull requests.

## How it works

The workflow at [`.github/workflows/claude.yml`](.github/workflows/claude.yml) runs the [`anthropics/claude-code-action`](https://github.com/anthropics/claude-code-action) whenever an issue, issue comment, or PR review comment mentions `@claude`. Claude reads the thread, plans the work, and either answers in-thread or opens a PR with the proposed changes.

## Usage

1. Open a new issue describing what you want.
2. Mention `@claude` in the issue body or in a follow-up comment.
3. Claude responds in a comment with a todo list and progress updates, then (for implementation requests) pushes a branch and provides a PR-creation link.

## Conventions

See [`CLAUDE.md`](CLAUDE.md) for the full framework — branch naming, commit style, what Claude should and shouldn't do, and the review checklist.

## Requirements

- Repository secret `ANTHROPIC_API_KEY` with access to the Claude API.
- The Claude GitHub App installed on the repository.
