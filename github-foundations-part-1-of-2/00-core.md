# Core

> 🧠 This file contains the facts that must be rote-memorised
> It is kept deliberately terse for ease of daily review

**VCS** = Version Control System

**DVCS** = Distributed Version Control System

**SCM** = Software Configuration Management system

**VCS** is part of SCM

**Working Tree** = project directory structure

Git tracks 4 object types - **Blobs** (files), **Trees** (directories), **Commits** (versions of the *Working Tree*) and **Tags** (names attached to commits)

*Commits* are assigned unique **160 bit SHA-1** hashes

**Repository** = project top-level domain

**Branch** = named series of linked *commits*

**Head** = latest *commit* in *branch*

**Origin** = default *repo*

**Remote** = named reference to *repo* (local clone)

**Commands** run programs, **Subcommands** tell the program what to do, and **Options** say how to do it. For example:
```
git push --force
```

**git status** displays the state of the working tree and staging area

**git add** specifies files to track (add to staging area)

**git commit** takes a snapshot of staged changes (makes a new commit)

**git log** displays previous commits

**git help** explains git *commands*

**--help** option explains a specific command

Git is **NOT** GitHub

**GitHub Priorities:**

- AI
- Collaboration
- Productivity
- Security
- Scale

**Gist** = lightweight mini-repo offered by GitHub

*Gists* are **NEVER** fully private (do not use for sensitive info)

GitHub offers **Wikis** for repos

Tracked files have 4 states:
- **Unmodified** (same as last commit)
- **Modified** (changed since last commit)
- **Staged** (marked for inclusion in next commit)
- **Committed** (in the repo database)

Git flow has 5 branch types:
- **master** is the default branch with the production-ready code
- **develop** is where you work on the next release
- **feature** is for new features - branched from and merged back to develop
- **release** prepares a new production release from develop
- **hotfix** to quickly patch bugs - branched from master

GitHub flow is simpler, with **feature** branches merged directly back to **main**

Git flow assumes merge commits, so rebase or squash merges may interfere with branch structure and history tracking
