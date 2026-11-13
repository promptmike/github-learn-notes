# What is GitHub administration?

> 📘 Note: These notes follow a two-line progressive summary method.
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will learn the GitHub organisational hierarchy to keep repositories running smoothly for our users.
> We must administer repositories to maximise user experience outcomes.

## Administration at team level

![Teams tab](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/teams.png)

Add users to teams with cascading permissions.
> Use cascading team permissions to administer repos.

With GitHub Enterprise Cloud, you can use identity provider (IdP) groups.
> Use teams and IdP groups to manage cascading permissions.

Members with *team maintainer* or *admin* permissions can configure a team, decide who is included, and add the team to IdP groups.
> Team maintainers and repo admins must use teams and Idp groups to manage cascading permissions.

### Best practices for team-level administration

Use nested teams, interest-specific teams, and IdP with team synchronisation.
> Use nested teams for cascading permissions and separation of concerns.

## Administration at organization level

GitHub organisations are shared spaces for collaborating on many projects at once.
> Use nested teams and cascading permissions within organisations for separation of concerns.

*Owners* can decide who is included in their organisation, which teams they belong to and the permissions for each team.
> Organisation owners should use nested, interest-specific teams with appropriate cascading permissions.

You should own just one organisation, else they may incur extra setup workload and installation costs.
> You should own just one organisation, then divide it into many specific teams with appropriate cascading permissions.

## Administration at enterprise level

GitHub Enterprise Cloud and GitHub Enterprise Server provide central policy management for multiple organisations.
> You should own just one organisation with many teams, or use GitHub Enterprise to manage multiple organisations with many teams.

Members with *owner* permissions at the enterprise level can set common policy for organisations.
> Use GitHub Enterprise to set policy for organisations, divide organisation members into interest-specific teams and set appropriate cascading permissions.

## Learn more

[Nested Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams#nested-teams) 
