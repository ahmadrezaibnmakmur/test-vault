---
name: backup-main-merge
description: Backup the latest main branch, push the backup branch to origin, then merge the current Git branch into main and push main to origin. Use when the user asks to merge the current branch, active branch, feature branch, or any branch into main with a mandatory remote backup of main first; also use for release/update workflows that must preserve main before merging and publish main.
---

# Backup Main Merge

## Overview

Use this skill to make every merge into `main` start by creating and pushing a backup branch from the current `main`, then publish the merged `main` to `origin`.
The workflow is reusable from any non-main branch and is implemented by `scripts/backup_main_merge.sh`.

## Workflow

1. Confirm the repository is a Git worktree and detect the current branch.
2. Refuse to continue if the current branch is `main` or `master`; this skill merges a non-main branch into `main`.
3. Check for uncommitted changes. Stop unless the user explicitly asks to allow a dirty working tree.
4. Fetch remotes when available, then update local `main` from `origin/main`.
5. Create a backup branch from `main` using the pattern `backup/main-before-merge-<source-branch>-<timestamp>`.
6. Push the backup branch to the remote before changing `main`.
7. Merge the original source branch into `main`.
8. Push `main` to the remote with `git push origin main`.
9. Check out the original source branch again after a successful merge and push.
10. Report the backup branch name, merge result, push results, and current branch.

## Quick Start

Run from the repository while checked out on the branch that should be merged into `main`:

```bash
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh
```

Useful options:

```bash
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh --dry-run
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh --backup-prefix backup/main
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh --allow-dirty
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh --no-ff
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh --no-push-backup
bash ~/.codex/skills/backup-main-merge/scripts/backup_main_merge.sh --no-push
```

## Safety Rules

- Do not run destructive Git commands such as `git reset --hard` or forced checkouts as part of this skill.
- If the merge has conflicts, stop and tell the user that `main` now contains an in-progress merge that must be resolved or aborted.
- Do not delete the backup branch.
- Push the backup branch before merging the source branch into `main`.
- Push `main` after a successful merge unless the user explicitly asks for `--no-push`.
- Return to the original source branch after a successful merge and push.
- Preserve unrelated user changes in the worktree.

## Script Contract

The script accepts:

- `--dry-run`: print the planned commands without changing branches.
- `--main <branch>`: override the target branch; default is `main`.
- `--remote <remote>`: override the remote; default is `origin`.
- `--backup-prefix <prefix>`: override the backup branch prefix; default is `backup/main-before-merge`.
- `--allow-dirty`: allow uncommitted changes.
- `--no-fetch`: skip `git fetch`.
- `--no-ff`: use `git merge --no-ff`.
- `--no-push-backup`: skip `git push <remote> <backup-branch>`.
- `--no-push`: skip `git push <remote> <main-branch>`.

Prefer the script over manually retyping the workflow because branch detection, backup naming, and safety checks are easy to get subtly wrong.
