# How does GitHub organization and permissions work?

> 📘 Note: These notes follow a two-line progressive summary method.
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

GitHub permission hierarchy: Enterprise -> Organization -> Team -> Repository
> We must use the permission hierarchy to grant appropriate access.

## Repository permission levels

GitHub permission levels: Admin > Maintain > Write > Triage > Read
> We must issue the correct permission levels at each hierarchy level.

You can provide a permission level to a member, an outside contributor or an entire team.
> Use the permission levels and hierarchy to grant each individual and group only the permissions they need.

Admins in GitHub Enterprise can create custom roles by extending one of the base roles with extra permissions.
> Issue the minimum permissions needed to each individual and group at each level of the permissions hierarchy.

### What is repository forking?

A fork is a copy of someone else's repo that you can modify without affecting the original.
> Issue minimum permissions and use forks to safely experiment.

You can keep your fork up to date by pulling from the upstream repo.
> Issue only necessary permissions to each individual and group, while using forks to safely experiment with code.

**Fork a repo**
1. GitHub.com -> Repo main page
2. Upper-right corner -> *Fork*
3. Choose fork owner
4. Choose name and branches to include
5. *Create fork*

![Fork repo button](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/fork-repo-option.png)

### Managing fork permissions (for admins)

Public repos can always be forked, while private repo forking may be restricted to members and internal repos can be restricted to forking from within same enterprise account.
> The permissions hierarchy, forks and fork permissions help to keep code secure.

**Configure fork settings**
1. Org repo -> *Settings*
2. Left sidebar -> Access -> *Member privileges*
3. *Repository forking* options

![Repo forking options](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/fork-repo-manage.png)

==💡 **Tip**==
==If you disable forking for a private repo, even organisation members cannot fork it.==

[Fork a repository](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/fork-a-repo)

## Viewing Repository Insights

Insights help you track repo health, security and bottlenecks.
> Use the appropriate permissions, use forks to experiment outside of the upstream and use insights to keep track of your repos.

### Steps to View Repository Insights

1. Repository page
2. *Insights* tab
3. Explore:
  - Contributors
  - Traffic
  - Commits
  - Code Frequency
  - Dependency Graph

### Best Practices for Using Repository Insights

- Monitor Contributions
- Track Traffic
- Address Vulnerabilities

Insights should be leveraged to make data-driven decisions.
> Use permissions hierarchy, forks and insights to make data-driven decisions for your repos and their users.

## Ways Users Receive Repository Access

### Actions of a User Given a List of Their Repository Permissions

A user inherits permissions from their role, team and organisation membership.
> Use roles, teams and orgs to provide appropriate permissions, use forks to experiment with code and use insights to make data-driven decisions.

GitHub combines permission sources and applies the highest permission level.
> Carefully assign roles, teams and org membership, set fork permissions and use insights for decision making.

### Repository Membership Options

Users can become collaborators by adding them explicitly to a repo or by adding them to a team or organisation that has permissions.
> Be careful when assigning roles, teams and org membership as the highest permission level will apply.

### Monitoring and Auditing Repository Access

Regularly audit repo settings, org logs, enterprise logs while using scripts (e.g. GraphQL API, REST API) to list permissions and look for anomalies.
> Assign appropriate roles, teams and org memberships while regularly auditing permissions.

**Tip: Branch protection rules and required reviews add another layer of security.**

### Team permission levels

GitHub teams provides the ability to organise contributors into specific groups and centrally control their permissions.
> Make use of roles and teams for efficient permissions config and regularly audit all permissions.

Child teams inherit permissions from parent teams allowing for cascading permissions mirroring org structure.
> Leverage roles and teams for cascading permissions and regularly audit all permissions.

Team maintainers can do everything a team member can do, plus configure the team itself in various ways.
> Leverage roles and teams, assign team maintainers and take advantage of cascading permissions with responsible auditing.

Audit repo access from settings:
![Manage Access options](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/manage-access-overview.png)

#### Permission Models

Permission Models: Admin > Maintain > Write > Triage > Read
> Leverage roles and teams, assign team maintainers and provide the correct permissions model to the team itself when granting repo access.

**Tip: Always follow the Principle of Least Privilege.** This will reduce the risk of accidental or unauthorised changes.
