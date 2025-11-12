# What is GitHub?

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will study an overview of GitHub, repositories, gists and wikis
>GitHub is an extensive platform that offers more than just hosting repos

## GitHub

Git is a DVCS, while GitHub is a platform that adds additional collaboration and automation features to use with Git
>Git is the core technology behind GitHub, which offers an extensive range of additional tools

![GitHub Platform](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/github-enterprise-platform.png)

The GitHub flow is optimised for helping developers and users to work together
>GitHub hosts Git repos and provides automation and collaboration tools to optimise flow

GitHub is centred on AI, Collaboration, Productivity, Security and Scale
>GitHub offers AI, Collaboration, Productivity, Security and Scaling tools for working on hosted Git repos

### AI

GitHub utilises AI to enhance pull requests, issues and security feedback
>GitHub has fully integrated AI into the workflow of collaborating on Git repositories

### Collaboration

GitHub streamlines collaboration
>GitHub has fully integrated AI to streamline collaboration on Git repositories

Repositories, Issues and Pull Requests support faster collaboration across roles
>GitHub integrates AI into Issues, Pull Requests and other tools to support collaboration on Git repos

### Productivity

Built-in CI/CD allows developers to spend more time on coding
>GitHub helps you spend more time coding by streamlining collaboration and CI/CD on an AI-powered platform

### Security

GitHub offers integrated security checks with CodeQL, secret scanning, Dependabot and security overview
>GitHub helps you spend more time coding by integrating collaboration, CI/CD and security tools on an AI-powered platform

GitHub meets global compliance standards for security, making it a reliable choice for projects of all sizes
>GitHub streamlines collaboration and CI/CD while helping you meet the best security practices on an AI-powered platform

### Scale

GitHub is a large and highly extensible platform with contributors from all over the world
>GitHub brings together developers worldwide for collaboration with AI-powered productivity and security tools

Insights from the diverse developer base help GitHub to continually evolve
>GitHub learns from its worldwide user base and develops AI-powered collaboration, CI/CD and security tools

GitHub strives to provide the best possible unified developer experience
>GitHub receives feedback from its worldwide user base and delivers a unified experience with AI-powered collaboration, security, CI/CD, and scaling tools

## Introduction to repositories

We will now review repository management
>GitHub delivers a unified developer experience worldwide for AI-powered collaboration on Git repos with best security, CI/CD and scaling practices

### What is a repository?

A repository contains all of your project's files and the revision history of each and every file
>GitHub delivers a unified developer experience with best practices for tracking and editing your projects using Git repos

### How to create a repository

![New Repo](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-new-repo-option.png)
![Repo Owner](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-selecting-repo-owner.png)
![Repo Name](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-repo-name-text-box.png)

1. Upper-right corner menu: select *New Repository*
2. Select an owner account from the drop-down menu
3. Type a name and an optional description
4. Choose visibility (Private/Public)
5. Select *Create Repository*

GitHub offers AI-powered tools for users to create public or private Git repos and collaborate on them securely with CI/CD and scalability

### How to clone a repository

![Code Button](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-selecting-code-button.png)

1. Start from the main repo page
2. Select the green *Code* button
3. Select either *HTTPS*, *SSH* or *GitHub CLI* and copy the URL
4. Open your terminal and navigate to the directory where you want the clone
5. `git clone <insert-url-here>`
6. `cd <insert-repo-name-here>`

GitHub offers secure, AI-powered hosting of Git repos that you can collaborate on using GitHub's array of CI/CD and Security tooling, or clone and work on remotely

### How to add a file to your repository

![Add File Button](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/add-file-options.png)
![Preview Option](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-preview-option-in-a-file.png)
![Commit Description](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-commit-description-box.png)
![Create Branch](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-create-a-new-branch.png)

1. Start from the main repo page
2. Browse to the directory you wish to add to
3. Select *Add file* and choose to create or upload from the dropdown
4. Type the name and extension in the file name field, using / to create subdirectories
5. Type or paste content in the file contents box
6. Select *Preview* to review
7. Select *Commit changes*
8. Type a brief description in the Commit message field
9. If you have multiple email addresses select one from the dropdown for the commit
10. Select a current branch or *Create a new branch* for your commit
11. Select *Commit changes* or *Propose changes*

GitHub provides an intuitive way to manage Git repos with GUIs for creating repos and commits using AI-powered tools and automated CI/CD and Security.

### What are Gists?

Gists are like mini repos that provide a lightweight way of sharing small amounts of information
>GitHub provides intuitive GUIs and automation for managing Git repos and additional features such as Gists

#### Key Features of Gists:

Like repos, gists can be public or private
>GitHub streamlines and automates Git repo management, security and scaling and offers mini repos called gists

Just like repos, gists are tracked so that you can see their history and revert them if needed
>GitHub offers AI, CI/CD, Security and Scaling tools to work on hosted Git repos or mini repos called gists

Gists can be forked and cloned just like repos
>GitHub hosts Git repos and mini repos called gists on an AI-powered collaboration and productivity platform with automated security and scaling tools

Gists can be embedded in web pages so they are ideal for sharing code examples
>GitHub hosts Git repos for secure, scalable collaboration and also mini repos called gists that can be embedded for easy sharing of code

Gists support Markdown, so they are ideal for adding context to code
>GitHub hosts Git repos and offers AI-powered productivity tools to manage them while also offering mini repos called gists that support embedding for easy sharing

Gists can be worked on by multiple users, making them an excellent option for lightweight collaboration
>GitHub provides AI-powered tools and hosts both full Git repos and mini repos called gists for lightweight sharing

#### Use cases for Gists:

Common use cases for gists include embedding examples in blogs, storing personal scripts and config, sharing logs or error reports and making code templates
>GitHub hosts Git repos for secure, scalable collaboration and mini repos called gists for easy sharing and embedding

##### ==!IMPORTANT==
**Never use gists to store sensitive or confidential data, such as passwords, secrets, or API keys—even in scripts or config files.**
Gists are not fully private: even secret gists can be accessed by anyone with the link. Always review your content carefully before sharing.

#### Limitations of Gists:

Gists are NEVER fully private, even if they are secret, so they should not be used for sensitive information
>GitHub offers AI-powered collaboration, productivity and security tools, hosts Git repos for scalable CI/CD and also hosts mini repos called gists for easy sharing and embedding

[Gists Documentation](https://docs.github.com/en/get-started/writing-on-github/editing-and-sharing-content-with-gists/creating-gists)

### Forking and cloning Gists

1. Navigate to the gist
2. Select *Fork* at the top-right of the gist page

To clone a gist: `git clone https://gist.github.com/<insert-gist-id-here>.git`

GitHub offers a GUI with powerful tools and automation for working on hosted Git repos and also mini repos called gists that can be forked and cloned just like repos

### What are wikis?

GitHub offers a documentation section called a wiki in every repository it hosts so you can provide additional information about your project
>GitHub is an AI-powered collaboration and productivity platform hosting Git repos with wiki docs and mini repos called gists

If your repo is private, only people with read access will be able to see the wiki
>GitHub is an AI-powered collaboration and productivity platform hosting both public and private Git repos with wiki docs and mini repos called gists

#### Creating, editing, and deleting wiki pages

**Create a wiki page**
1. Navigate to your repo
2. Select *Wiki* tab
3. Select *Create the first page* or *New Page*
4. Enter a title and content, then select *Save Page*

**Edit a wiki page**
1. Navigate to the wiki page
2. Select *Edit* in the top right
3. Make your changes, then select *Save Page*

**Delete a wiki page**
`git clone <insert-repo-url-here>`
`rm <insert-path-to-file-here>`
`git push`

GitHub is an AI-powered platform with tools and GUIs for managing Git repos, gists and wiki pages for documentation

[Wiki Pages Documentation](https://docs.github.com/en/communities/documenting-your-project-with-wikis/adding-or-editing-wiki-pages)

### What are Feature Previews?

Feature Previews give you early access to experimental features of GitHub so you can try them and provide feedback
>GitHub is an AI-powered CI/CD platform for hosting Git repos, gists and wiki pages, that provides a unified developer experience based on user feedback

**Choose Feature Previews**
1. Select your profile picture in the top-right
2. Select *Feature preview*
3. Toggle the features you want to try

GitHub is a powerful CI/CD platform hosting Git repos, gists and wiki pages, offering AI, collaboration, productivity, security and scale tooling and listening to user feedback

==Tip==
GitHub frequently adds new experimental features for users to explore, so keep an eye on the Feature review to discover new tools and enhancements.
