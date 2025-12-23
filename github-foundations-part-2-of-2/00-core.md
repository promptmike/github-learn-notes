# Core

> 🧠 This file contains the facts that must be rote-memorised
> It is kept deliberately terse for ease of daily review

Use [GitHub Search](https://github.com/search) to find projects to contribute to

Read the docs first - especially README, LICENSE, CONTRIBUTING AND CODE\_OF\_CONDUCT and check labels for help needed

Check for additional communication channels (e.g. an IRC)

**PR best practices**
- Be consise
 - Subject line under 50 characters
 - Commit small, isolated sets of changes
- Use the imperative, present tense
    - *Add*, not *Adds* or *Added*
- Show motivation
    - Contrast changes with existing code
    - Explain what merging your PR will do
    - **What** and **Why**, not merely **How**
- Use the sidebar
    - Add Reviewers or Assignees
    - Use labels
    - Link issues that may be closed by your PR
- Remember to set notifications for the updates you want

**Inclusive Verbs**

Important for accessibility. For example, a user with a screen reader *Selects*, but does not *Click* or *Swipe*. You should therefore only say *Click* when you are specifically refering to mouse input, not as a general term for selecting things.

- Open
- Close
- Leave
- Go to
- Select
- Select and hold
- `>`
- Clear
- Choose
- Switch, turn on, turn off
- Enter
- Move
- Move through
- Zoom, zoom in, zoom out

## Community

Use *Insights* or comments sections in a repo to find other active contributors

**Sharing Solutions**
- Library
- Mirror project
- Action or Workflow

## InnerSource

InnerSource software is a hybrid between Open-Source and closed source code that shares source code within a select group (e.g. organisation)

GitHub offers Internal repos for Enterprise customers to benefit from InnerSource

| Level    | Recommended Use                         |
| -------- | --------------------------------------- |
| Read     | Non-code contributors                   |
| Triage   | Manage Issues and Pull Requests         |
| Write    | Active contributors                     |
| Maintain | Project Managers                        |
| Admin    | Full access including sensitive actions |

GitHub looks for README in the following order:
- `.github` directory
- root directory
- `docs` directory

Use `CONTRIBUTING.md` in root, `/docs` or `/.github` - GitHub presents a link to it when users submit Issues or Pull Requests

Add a `CODEOWNERS.md` file to define who is responsible for reviewing code

Issue templates go in `/.github/ISSUE_TEMPLATE.md` and PR templates go in `/.github/PULL_REQUEST_TEMPLATE.md`

## Secure Repo

*Shift Left* - implement security practices earlier in the development cycle

Add a `SECURITY.md` file to inform contributors of security policy

Open *Security Advisories* to privately discuss and fix vulnerabilities, then publish them to the GitHub CVE list

Keep sensitive data out of the repo with `.gitignore` files at every level required

Set *Branch Protection* rules to enforce workflows

Configure *Required Reviewers* for PRs

Add `CODEOWNERS` in root, `docs` or `.github`
