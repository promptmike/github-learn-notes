# How to manage a successful InnerSource program

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will discuss the use of InnerSource for organisations
> Organisations can use InnerSource code as a compromise between Open and Proprietary source code

## What is InnerSource?

Open-Source projects share source code to benefit from community input
> Open-Source software tends to be very reliable, because everyone can contribute to solutions

Inner-Source projects apply Open-Source principles within a limited group of people
> Inner-Source software shares source code with and accepts contributions from a specific set of people

### InnerSource benefits

InnerSource offers benefits you cannot get from closed-source
> InnerSource software benefits from sharing source code with a select group of people

InnerSource helps groups across an organisation learn from one another
> InnerSource software benefits from **Internal Visibility**

InnerSource helps groups across an organisation make and propose changes to meet their needs, because they can see each other's source code
> InnerSource software benefits from **Internal Visibility** and **Reduced Friction**

InnerSource helps groups across an organisation to adopt consistent practices, because each group sees how the others operate
> InnerSource software benefits from **Internal Visibility**, **Reduced Friction** and **Standardised Practices**

**💡 ==Tip==**
Consider using GitHub Discussions and GitHub Projects to further support InnerSource collaboration across teams.

[An introduction to InnerSource](https://github.com/resources/articles/innersource)

## Set up an InnerSource program on GitHub

### Set repository visibility and permissions

**Visibility Levels**
- Public: Visible to everyone.
- Internal: Visible to members of the Enterprise that owns the repository.
- Private: Visible only to the owner and specific groups the owner adds.

**❗ ==Note==**
Internal repositories are only available to GitHub Enterprise customers. Use this visibility for InnerSource projects.

> GitHub has visibility levels to support Proprietary, InnerSource, and Open-Source code

**Permission Levels**

| Level    | Recommended Use                         |
| -------- | --------------------------------------- |
| Read     | Non-code contributors                   |
| Triage   | Manage Issues and Pull Requests         |
| Write    | Active contributors                     |
| Maintain | Project Managers                        |
| Admin    | Full access including sensitive actions |

> GitHub has visibility and permission levels to suit every level of an organisation for Proprietary, InnerSource or Open-Source code

### Create discoverable repositories

As an InnerSource project grows, it is important to make your work easy to find within your organisation
> GitHub has visibility levels, permission levels and discoverability to suit every level of an organisation for Proprietary, InnerSource or Open-Source code

**Best Practices**
- Descriptive repo name (e.g. `warehouse-api`)
- Concise description
- License the repo so everyone knows what they are allowed to do with it
- Include `README.md` for landing page

### Add a README file

**README outcomes**
- Purpose and vision of project
- Illustration of project (e.g. visual aids, screenshots, code samples)
- Link to production or demo version
- Show prerequisites and deployment procedures
- Cite and credit dependencies
- Markdown formatting

> GitHub has visibility levels, permission levels and markdown landing pages to support InnerSource projects

GitHub looks for README in the following order:
- `.github` directory
- root directory
- `docs` directory

> GitHub has visibility levels, permission levels, markdown, and automatic README loading to support InnerSource projects

[README examples](https://github.com/matiassingers/awesome-readme)

You can link to your landing page to promote your project
> GitHub offers visibility levels, permission levels, and markdown landing pages to support you in building, launching and promoting an InnerSource project

[About README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)

### Manage projects on GitHub

![Contributing Guidelines](https://learn.microsoft.com/en-us/training/github/manage-innersource-program-github/media/2-contributing-guidelines.png)

As projects grow they require more work to manage
> GitHub offers visibility, permission, markdown and scalability to support InnerSource projects

Use `CONTRIBUTING.md` in root, `/docs` or `/.github` to explain the contribution policy for your project
> GitHub supports InnerSource with internal visibility, permission levels, and discoverable documentation

If `CONTRIBUTINTG.md` exists, GitHub presents a link to it when users submit Issues or Pull Requests
> GitHub offers a range of visibility and permission levels, while encouraging contributors to follow project guidelines

[CONTRIBUTING.md examples](https://github.com/mntnr/awesome-contributing)

You can also add a `CODEOWNERS.md` file to define who is responsible for reviewing code
> GitHub offers a range of visibility and permission levels, while supporting scalability with discoverable documentation

### Create issue and pull request templates

![New Issue Template](https://learn.microsoft.com/en-us/training/github/manage-innersource-program-github/media/2-new-issue-template.png)

GitHub supports starter templates to provide initial description text for new Issues and Pull Requests
> GitHub supports InnerSource with visibility and permission settings, discoverable documentation and item templates

Write a template in `./github/ISSUE_TEMPLATE.md` and the user can fill it in like a form so they do not need to constantly reference `CONTRIBUTING.md`
> GitHub supports InnerSource with visibility and permission settings, discoverable docs and item templates for ease of contribution

For PRs, the path is `./github/PULL_REQUEST_TEMPLATE.md`
> GitHub supports InnerSouce development with visibility and permission settings, discoverable markdown docs and easy template creation

[Template examples](https://github.com/devspace/awesome-github-templates)

### Define workflows

A workflow specifies how branches and PRs should be used (e.g. the standard [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow))
> GitHub supports InnerSource development with visibility and permission settings, discoverable docs, templates, and workflows

Your workflow should explain how to manage branches and releases
> Use correct visibility and permission, provide README, CONTRIBUTING AND CODEOWNERS, write item templates, and communicate your strategy with a workflow

[Git branching guidance](https://learn.microsoft.com/en-us/azure/devops/repos/git/git-branching-guidance?view=azure-devops)

### Measuring program success

Think carefully about what metrics to track to see the success of InnerSource practices
> GitHub offers settings and tools to support InnerSource, while the user must measure the success of the practices carefully

Consider metrics that track external contribution (e.g. PRs external contributors, bugs fixed using external source, etc)
> GitHub offers settings and tools to support InnerSource, while the user must take responsibility for measuring external contribution

Bad metrics can be actively harmful
> Use all the tools GitHub provides to support InnerSource, while thinking carefully about the metrics you use to measure success

**Guidlines for metrics**
- Measure process, not output
    - Code review turnaround time
    - PR size
    - Work in progress
    - Time to open
- Measure against targets, not absolutes
- Measure teams, not individuals
    - Number of contributors
    - Number of projects reusing code
    - Number of cross-team @mentions

> Make full use of visibility and permission settings, markdown docs, templates and workflows, while thinking carefully about what metrics you track to benefit from InnerSource code

[InnerSource case studies](gist.github.com/githubteacher/9fe53687a5f173d1d64c24c68625349e)


