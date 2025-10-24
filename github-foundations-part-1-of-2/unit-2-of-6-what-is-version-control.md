# What is Version Control?

A Version Control System (VCS) is a set of software used to track changes to a collection of files
A VCS helps many people collaborate on a complex project

A VCS is somtimes called a Software Configuration Management system (SCM) although version control is really only one part of SCM
A VCS helps groups of people collaborate on complex software or other projects such as books

You can track, merge and revert changes on multiple branches, see who made them and read their commit messages
The VCS is a crucial tool for keeping large complex projects manageable

## Distributed Version Control

Early VCS used a central server, introducing a single point of failure
A VCS can track all the changes to a set of files, even from a single server

Git is *distributed*, keeping the entire project history on both client and server
A VCS tracks the history of changes to a set of files, preferably with distributed storage

## Git Terminology

To understand Git you need to remember Git terminology
Git tracks the entire history of changes to a set of files and stores it on both client and server

The **Working Tree** is the directory stucture that contains the project
Git tracks the entire history of a working tree stored both client-side and server-side

The **Repository (repo)** is the project top-level domain, either at the top of a working tree or a treeless **bare repo** often used for sharing and backups
Git tracks the entire history of a repo with or without a working tree and stores it on both client and server

A **Hash** represents file contents as a number so that if the number changes Git will recognise the file has changed
Git tracks the history of all branches of a repo using 160 bit hashes

Git tracks 4 types of **Objects** - **Blobs** (files), **Trees** (directories), **Commits** (versions of the working tree) and **Tags** (names attached to commits)
Git tracks the objects in a repo using 160 bit SHA-1 hashes with distributed storage of the working tree

The word **Commit** can also be used as a verb to describe making a new commit object
Git tracks the objects in a repo and who committed them using 160 bit SHA-1 hashes and distributed storage

A **Branch** is a named series of linked commits, the latest commit in a branch is called the **head** and the default branch is usually **Main** or **Master**
Git tracks series of linked commits of objects with 160 bit SHA-1 hashes and distributed storage

A **Remote** is a named reference to a repo and the default repo is called **Origin**
Git creates a default project repo and tracks changes to all the remotes in a project for distributed version control

A **Command** runs a program from the terminal, a **Subcommand** specifies what you want it to do and **Options** give additional instructions
Git creates a default project repo and allows interaction with remote repos using commands such as git (command) push (subcommand) --force (option)

Reviewing Git commands is useful for taking full advantage of Git in the terminal
Git tracks changes to a project with distributed remote repos and a central default repo called origin allowing full version control from the terminal

## The Git Command Line

There are many GUIs that can interface with Git, but none of them can make full use of all Git features
Git tracks changes to a project and allows access to remote repos from the command line

The Git CLI works the same no matter what OS you use
Git tracks project changes and allows access to remote repos from the command line regardless of operating system

## Git and GitHub

Git is not the same as GitHub
Git provides distributed version control and is not the same as GitHub

Git is a **Distributed Version Control System (DVCS)** for synchronising local branches with a remote repo
Git is a DVCS that tracks changes to all objects in all repos of a project and is *not* the same as GitHub

**GitHub** is a cloud platform that uses **Git** to host remote repos
Git is a DVCS that tracks 4 types of objects and connects remote repos, while GitHub is a cloud platform that uses Git to offer repo hosting through a website

GitHub offers additional features such as Issues, Pull Requests and Notifications that you would not get with Git alone
Git is a DVCS that tracks 4 types of objects across remote repos using 160 bit SHA-1 hashes and GitHub is a cloud platform that uses Git to host repos and offer additional tooling
