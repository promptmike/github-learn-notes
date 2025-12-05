# Components of the GitHub flow

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will review branches, commits and pull requests as well as the difference between GitHub flow and Git flow
>Git flow is different to GitHub flow

## Components of GitHub Flow

GitHub flow builds on Git concepts, but is not the same as Git flow
>Git has a flow for managing repositories and GitHub builds on that

GitHub makes Git easier to use with features like branches, commits and pull requests
>Git has a flow for DVCS and GitHub builds on it with features for branches, commits, pull requests and much more

## What are branches

GitHub provides branches to let you safely work on code without editing the main branch
>Git is a DVCS with a flow for collaboration, while GitHub expands this with features that make coding safe and reliable

==Note==
Alternatively, you can create a new branch and check it out by using git in a terminal. The command would be:
`git checkout -b <insert-branch-name-here>`

## What are commits

Commits assign a UID to one or more changes on a branch so that they can be tracked
>Git provides DVCS for collaboration, while GitHub is a platform that hosts Git repos and offers additional features

**Make a commit**
`git commit -m "<insert-commit-message-here>"`

![Commits](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-commits.png)

An untracked file is not known to Git, while a tracked file will be monitored by Git as part of the repo
>Git is a DVCS for tracking files as part of a repo and GitHub is a platform that uses Git and adds many useful tools for repo management

A tracked file can be **Unmodified** (same as last commit), **Modified** (changed since last commit), **Staged** (ready to be committed) or **Committed** (in the repo database)
>Git is DVCS that tracks files through the VCS process (Unmodified-Modified-Staged-Committed), while GitHub is a platform that offers additional function for using Git repos

## What are pull requests?

A pull request signals that commits from one branch are ready to be merged into another branch
>Git DVCS tracks files through Unmodified, Modified, Staged and Committed, while GitHub offers additional functions through a GUI and automates CI/CD processes

The user submitting the pull request asks one or more reviewers to approve the merge, so they can check the code, comment on changes, add changes and discuss the project
>Git tracks files through the VCS process, while GitHub is a platform that helps people collaborate on Git repos in a GUI  using tools such as comments and reviews of pull requests

GitHub also allows draft pull requests before code is read for review
>Git tracks files through DVCS, GitHub provides additional tools and GUIs and pull requests allow commits to be drafted, reviewed and discussed before merge

When a pull request passes review, the source branch is merged into the base branch
>GitHub provides tools and GUIs for managing Git repos, pull requests allow commits to be drafted, reviewed and discussed and merging branches applies changes to the base branch

![Pull Request](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-pull-request.png)

## The GitHub flow

![Branching](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-branching.png)

The GitHub flow is a simple workflow for safe collaboration
>GitHub provides tools, GUIs and a simple workflow for managing Git repos with branches, pull requests and merges

==Note==
GitHub flow is one of several popular workflows. Others include Git flow and trunk-based development.

1. Create a branch (separate from main)
2. Make and test updates to your branch
3. Open a pull request
4. Review the comments and respond to feedback
5. Ask for approval to merge
6. Delete branch after merge

>GitHub provides tools and GUIs for managing Git repos on a robust platform with a simple Branch - Update - Pull Request - Merge workflow to encourage CI/CD

## Git flow

![Git Flow](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-git-flow-image.png)

Git flow is older than GitHub flow, and uses more structured branching appropriate to a release-based environment
>GitHub provides automation in a GUI for managing Git repos with a simple flow for CI/CD, while the older Git flow is more structured and suited to a release model

## Git flow Branch Types

- **master** is the default branch with the production-ready code
- **develop** is where you work on the next release
- **feature** is for new features - branched from and merged back to develop
- **release** prepares a new production release from develop
- **hotfix** to quickly patch bugs - branched from master

>GitHub flow is simple and suited to CI/CD, while Git flow designates specific branch types for each task and aims to deliver stable releases

## How the Git flow Process Works

1. Create feature branches from develop
2. Create a release branch from develop when ready - continue to work on develop
3. Bug fixes go in release, but major features wait for next release
4. Release branch is merged to master when ready
5. Release is also merged back to develop to keep in sync
6. ILf a critical bug is found, create a hotfix from master, fix the bug, then merge to master and develop

>Git flow is a very structured and stable system of branching and releases, while GitHub flow is simple and continuous

## When to Use Git flow

Git flow is ideal for slow, structured release cycles with multiple versions, LTS branches and scheduled releases
>GitHub flow is simple and continuous, but less structured than Git flow which is ideal for LTS and scheduling releases

==Note==
Git flow assumes merge commits for integrating branches. Using rebase or squash merges can interfere with its branch structure and history tracking.

Many teams find GitHub flow faster and easier, but those who need more stucture and predictability may prefer Git flow
Git flow is a tried and tested structure for predictable release schedules and LTS, while GitHub flow is a faster and easier system for unrestricted CI/CD
