# Managing enterprise access, permissions, and governance

> 📘 Note: These notes follow a two-line progressive summary method.
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We must learn to manage security and permissions at a broader level.
> Permissions need to be managed at a broad level and a granular level.

## Organization permission levels

Organizations provide centralised control of permissions across an organisation.
> Permissions must be managed at both a repository and organization level.

Organizations have owners, members, moderators, billing managers, security managers and outside contributors.
> Organizations have different permissions for different types of contributor.

Set default permissions for members:

![Member repository permissions](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/org-base-permissions.png)

Depending on the size of your organization, you might give all member write permissions or only give read permissions by default.
> Organizations must set default permissions and permission levels.

## Enterprise permission levels

Enterprises contain multiple organizations, so organization members are also members of the containing enterprise.
> Permissions are managed at the *Enterprise*, *Organization* and *Repository* levels.

Enterprises have owners, members, billing managers and guest collaborators.
> Enterprise, organization and repository permissions are managed by default settings and permission levels.

Set default repository permissions across all organizations within the enterprise:

![Default permissions](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/enterprise-base-permissions.png)

Depending on enterprise size, you may choose to give write permissions to all members for all organizations, or only grand read permissions by default.
> It is important to set default permissions and permission levels appropriately at each level.

Enterprise accounts can create nested teams, and even automate team creation, permissions and auditing using Actions or the API.
> Repositories, Organizations, Enterprises and nested teams offer cascading permissions for granular permission management.

## Enterprise Permissions and Policies via Ruleset

Enterprise permissions can be managed using rulesets.
> Permissions can be set by default, granted on an *ad hoc* basis, automated by API or Actions or managed using rulesets.

### Weighing the pros and cons of deploying a single versus multiple organizations

A single organization offers centralised control and asset sharing, while also having limited flexibility and presenting a single attack surface.
> Permissions can be centralised for ease of management, or decentralised and cascaded for more flexibility.

A multi-organization enterprise offers granular permissions control and limits security risks, while also requiring larger administrative overhead.
> Permissions can be centralised for easy management and asset sharing, or cascaded for granular control and security.

### Setting default read versus default write across organizations

Default read reduces risk of unintended changes and offers easy auditing, while default write provides ease of collaboration and reduces bottlenecks.
> Default permissions must be set appropriately for the enterprise/organization size and level of collaboration required.

**Recommendation:** Use a default read permission model and grant write access selectively, ensuring adherence to the principle of least privilege.

### Team synchronization through Active Directory (AD)

AD makes user access and access control easier to manage.
> Use AD, default permissions, permission levels and cascading permissions to adhere to the principle of least privilege.

#### Why use AD sync?

AD sync keeps user identities, roles and permissions consistent across your organization.
> Use AD, GitHub API and Actions to automate permissions and keep them consistent.

#### Things to consider before implementing

Clearly define roles, set a sync schedule and log all changes.
> To automate permissions, we must clearly define roles, sync regularly and log changes to meet compliance requirements.

### Maintainability: scripting for multiple organizations and access rights

As an organization scales, automation is critical to maintainable permissions.
> Automate permissions with API, Actions and AD for long-term maintainability.

## Enterprise GitHub App ownership and API-driven automation

An enterprise-owned app can only be installed on the owning enterprise itself or on organizations within the owning enterprise.
> Automating and cascading permissions is critical to organization security.

GitHub Apps can be used with GitHub APIs to automate admin tasks at scale.
> Use Actions, API and Apps to automate admin and keep permissions maintainable at scale.

The REST API can be used to create integrations, retrieve data and automate workflows, while the GraphQL API allows more precise and flexible queries.
> GitHub Apps and APIs help administrators automate repetitive work and consistently manage permissions across large organizations.

## Granular bypass permissions

Some roles, teams or apps may need to bypass permissions set by a ruleset.
> Set appropriate default permissions and bypass as necessary applying the principle of least privilege.

Granular bypass permissions allow admins to define who can bypass a ruleset without relying on broader admin access.
> Even when permissions must be bypassed, we must apply the principle of least privilege.

Careful use of bypass permissions maintains strong governance while permitting approved exceptions.
> Automate permissions for maintainability and provide granular bypass where necessary.

### Key Practices

- Modularity
- Reusability
- Testing
- Logging
- Version Control

> Develop and test modular scripts in reusable modules with a version control system. Automate permissions where possible, provide granular bypasses where needed and log all changes. Principle of least privilege.
