# Core

> 🧠 This file contains the facts that must be rote-memorised
> It is kept deliberately terse for ease of daily review

## Vocabulary

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

### Commands

**git status** displays the state of the working tree and staging area

**git add** specifies files to track (add to staging area)

**git commit** takes a snapshot of staged changes (makes a new commit)

**git log** displays previous commits

**git help** explains git *commands*

**--help** option explains a specific command

### GitHub vs Git

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

## GitHub Basics

`mentions:<username>` to find where you were @mentioned

*Watch* at top of repo page to configure repo notification

GHEC offers 99.9% uptime service agreement

Public repos are **free**

**Billing (private repos)**
- Actions: runner rates by the minute
- Packages: storage and transfer rates
- Enterprise: per active user
- GHAS: per active committer
- Copilot: per user

## Code Scanning

GitHub code-scanning supports Static Analysis Results Interchange Format (SARIF) version 2.1.0

The maximum code-scanning results upload is 5,000 results totalling 10 MB in a gzipped SARIF file

Scanning the merge commit is more accurate than scanning the head, so scan on PR is preferred

## Copilot

- `Tab` or `>` to accept Copilot suggestion | `Esc` or keep typing to reject
- `Ctrl + Shift + P` for *Command Pallete*
- `Ctrl + I` for inline chat
- `#Comment` a line with `#` for Copilot to convert to code
- `Alt + ]` to cycle through 💡 suggestions
- `Right click` selection to see options

### Slash Command examples

- `/explain`    selected code
- `/suggest`    in this context
- `/tests`      for selection or class
- `/comment`    to code snippet

### VS Code Command Palette examples

- `Copilot: Generate Unit Tests` generate unit tests
- `Developer: Open Log File` get VS Code logs
- `Diagnostics` > `GitHub Copilot: Collect Diagnostics` troubleshoot connectivity

## Codespaces

Codespaces are customisable, repeatable and persistent, retaining changes when stopped

Changes are saved locally even when disconnected

When the container is rebuilt, only the changes in `/workspaces` are preserved

You can customise a codespace from a dotfile or GitHub settings and extend it with IDE plugins
