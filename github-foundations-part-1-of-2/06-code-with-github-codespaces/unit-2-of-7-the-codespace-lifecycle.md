# The Codespace lifecycle

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

GitHub Codespaces are configurable
> Codespaces provide a repeatable custom development environment

A Codespace can still run when you disconnect, and retain changes even when stopped
> Codespaces are customisable, repeatable and persistent for their lifecycle

![Codespace Lifecycle](https://learn.microsoft.com/en-us/training/github/code-with-github-codespaces/media/codespace-circular-lifecycle.png)

## Create a Codespace

You can create a Codespace on GitHub.com, GitHub CLI or Visual Studio Code, from a repo, branch, pull request or commit
> Codespaces are customisable, repeatable and persistent, and they can be created from a whole repository or a specific event

You can temporarily use a Codespace for testing, or keep it saved for long-running work
> Codespaces are configurable, repeatable and storable, and accessible from CLI, VS Code or the Web

You can create multiple Codespaces per repository or branch, but there is a limit on how many you can have at the same time
> Codespaces are configurable, repeatable and persistently stored, but there are limits on how many you can keep at once

When starting a new project, you can create a Codespace from a template and save it to a repository later
> Codespaces are configurable, repeatable and persistently stored, and you can save them to repos later

When working on a project, you should pull from default branch to get the latest commits and push your changes regularly
> Codespaces are configurable, repeatable and persistently stored, perfect for working on a long-term project

Repository admins can configure GitHub Codespaces prebuilds to speed up Codespace creation
> Codespaces are configurable, prebuildable, repeatable and persistent

### Codespace creation process

![Codespace Creation](https://learn.microsoft.com/en-us/training/github/code-with-github-codespaces/media/codespace-connection-editor.png)

1. A **virtual machine** and **storage** are assigned to your Codespace
2. A **container** is created
3. A **connection** is established
4. A **post-creation setup** is made

> Codespaces are configurable, prebuildable, repeatable and persistent environments that run in containers on virtual machines

### Save changes in a Codespace

On the web autosave is enabled, but in Visual Studio Code you must enable it if desired
> Codespaces are configurable, prebuildable, repeatable and persistent container environments that can autosave when accessed on the web

Your work is saved to a virtual machine, but to keep it after deleting the Codespace you must commit it to a repository
> Codespaces are prebuildable, configurable, repeatable, persistent container environments that save your work to a virtual machine

### Open an existing Codespace

You can open your active or stopped Codespaces from GitHub.com, GitHub CLI, Visual Studio Code or JetBrains
> Codespaces are prebuildable, configurable, repeatable, persistent container environments that save your work to a virtual machine and can be accessed from IDE, CLI or the Web

To resume an existing Codespace, go to the repo, select the `,` key and select *Resume this Codespace*, or select from [GitHub Codespaces](https://github.com/codespaces) on the Web
> Codespaces are prebuildable, configurable, repeatable, restartable, persistent environments that save your work to a virtual machine

### Timeouts for a Codespace

Inactive Codespaces timeout after 30 minutes by default
> Codespaces are prebuildable, configurable, repeatable, restartable, persistent environments that save work to a virtual machine while active

### Internet connection while using GitHub Codespaces

Codespaces require an internet connection, but they save uncommitted changes even during disconnection
> Codespaces are prebuildable, configurable, reusable, persistent environments that save work to a virtual machine and keep it when you disconnect

If your internet connection is unstable you should frequently commit and push your changes
> Codespaces are prebuildable, configurable, reusable, persistent environments that save work to a virtual machine, but they work best with a stable internet connection

## Close or stop a Codespace

The default timeout for a Codespace is 30 minutes, but you or your organisation can set your own timeout
> Codespaces are prebuildable, configurable, reusable, persistent environments that run in a container on a virtual machine and timeout when not in use

Running Codespaces incur CPU charges, but stopped Codespaces only incur storage charges
> Codespaces are prebuildable, configurable, reusable, persistent environments that run in a container on a virtual machine, with billing based on use

You need to restart your Codespace to apply changes (e.g. different VM type)
> Codespaces are prebuildable, configurable, reusable, persistent environments that run on a VM and can be changed between restarts

You can stop or restart your Codespace if you encounter an error or unexpected behaviour
> Codespaces are prebuildable, configurable, reusable, persistent environments that run in containers on VMs and can be started or stopped when you wish

## Rebuild a Codespace

You can rebuild your Codespace to implement changes to the dev container, and cache images will speed up this process
> Codespaces are prebuildable, rebuildable, configurable, reusable, persistent environments running in containers on VMs

When you rebuild the container, changes inside the `/workspaces` directory are preserved, when changes outside `workspaces` are cleared
> Codespaces are prebuildable, rebuildable, configurable, reusable, persistent environments running in containers on VMs that preserve everything in `/workspaces`

## Delete a Codespace

After you push changes to a remote branch it is safe to delete the Codespace
> Codespaces are prebuildable, rebuildable, configurable, reusable environments with persistent storage on VMs that can push to remote branches

If you try to delete a Codespace with unpushed commites you will be notified, so you can decide to push changes, export to a new branch or delete the changes along with the Codespace
> Codespaces are prebuildable, rebuildable, configurabe, reusable environments with persistent storage on VMs that can push to remote branches or even export to a new branch

Stopped Codespaces are deleted after 30 days of inactivity by default, but this can be reconfigured
> Codespaces are prebuildable, rebuildable, configurable, reusable environments in containers on VMs with persistent storage and the ability to push and export to GitHub repositories
