# GIT TUTORIAL NOTES

**Version Control** - system that allows you to revisit various versions of a file or set of files by recording changes.

- Local VCS (Version Control Systems) - one database
- Centralized VCS - single server storing all changes, accessible by various clients, enables collaboration
- Distributed VCS - prevents loss due to server failure in CVCS
**
  - Create mirrored repositories, or data backups, to replace lost information
  - Enables simultaneous workflows

- - -

## Git is a DVCS made up of snapshots

- Saved versions of projects are called commits
- Enables local operation as opposed to on the server
- Can detect file corruption

3 main states in Git

- Committed - securely stored locally
- Modified - changed but not committed
- Staged - flagged file’s changed version to be committed

Cloning a repository in terminal - `git clone “URL”`

3 components of local repository

1. Working directory: actual files (add)
2. Index: used for staging (commit)
3. Head: most recent commit

Files can be tracked (most recent snapshot) or untracked (not in the last snapshot or staging area)

Push transfers modifications from local to remote (origin)

Stashing (git stash) temporarily removes and hides changes if you are not ready to commit

- git stash apply will retrieve hidden changes

[back](../README.md)
