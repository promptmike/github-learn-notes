# Metered Usage Reports

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

GitHub has metered products billed separately from plans
Plans include features and CI/CD limits while metered products are billed separately

GitHub provides detailed reports on metered product billing
We must select the right plan while also monitoring metered products carefully

## GitHub Actions Minutes

Actions is a CI/CD tool billed by the minute
GitHub runs Actions on runners and bills by the minute for them

### Tracking Consumption

*Settings* > *Billing* > *GitHub Actions*
GitHub runs Actions on runners, bills by the minute and shows billing details in the GUI

### Billing Details

Public repos have unlimited Actions minutes, while private repos consume minutes from the plan and are then billed when over the plan limit
GitHub offers unlimited Actions for public repos, a limit of free Actions minutes varying by plan and billed minutes with price varying by runner

### Optimization Strategies

Use self-hosted runners for high volume jobs, cache dependencies, reduce redundant jobs and only trigger workflows when necessary
GitHub offers free Actions for public repos, limited free Actions for private repos, billing by minute and runner, and tracking tools to reduce costs

## Storage for GitHub Packages

GitHub Packages stores artifacts, images and dependencies, billed by storage and tranfer
GitHub Actions is free for public repos, plans have limited free Actions, Actions are then billed by minute and runner, while packages are billed by storage and transfer

### Tracking Consumption

*Settings* > *Billing* > *GitHub Packages* to view storage and transfer per repo
GitHub Actions are free for public repos and billed for private repos, plans have monthly free Actions and packages are billed by storage and transfer, trackable through the GUI

### Billing Details

GitHub Packages is free for public repos, while private repos are billed for anything beyond 2GB storage and 1GB data transfer
Actions and Packages are free for public repos and billed for private repos when minutes, storage or data transfer go over limits

[GitHub Pricing](https://github.com/pricing)

### Optimization Strategies

Delete unused packages, store centrally to reduce duplication and use compressed formats to reduce storage
Actions and Packages are free for public repos, billed for private repos, and can be optimised to reduce waste

## GitHub Enterprise (GHE) Licenses

GitHub Enterprise provides advanced features, billed by the number of active users
Actions and Packages are free for public repos and billed by minute/runner and storage+transfer for private, while Enterprise is billed by active users

### Tracking Consumption

*Enterprise Settings* > *Billing* to monitor license usage
Actions and Packages are free for public repos and billed for private repos, plans include varying amounts of free minutes and Enterprise licenses are billed by active users

### Billing Details

Each user with access to a private repository consumes one license and enterprises are billed by license
Actions and Packages are free for public repos and billed for private repos, plans include varying amounts of free minutes and Enterprises are billed by private repo users

### Optimization Strategies

Revoke unused licenses or automate user management using SSO or SCIM
Actions and Packages are free for public repos and billed for private, plans include free minutes, Enterprise features are billed by active user and user management can be automated

## GitHub Advanced Security (GHAS) Licenses

GHAS offers code scanning, secret scanning and dependency review
Actions and Packages are free for public repos, plans include free minutes, runner bills depend on OS, Enterprise features are billed by active user and GHAS offers extra security

### Tracking Consumption

Side Navigation > *Enterprises* > Name > *Billing* > *Advanced Security* to view usage, measured by users who have pushed to a GHAS enabled repo in the last 90 days (active committers)
Actions are billed by the minute and priced by runner OS, Packages by storage and data transfer, Enterprise licenses by active users and GHAS by active committers

### Billing Details

GHAS is charged per unique committer per month, regardless of how many repos each unique committer committed to
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users and GHAS by active committers, regardless of how many GHAS enabled repos they commit to

### Optimization Strategies

Limit GHAS to repos that need it, and use branch protections to limit unnecessary scans
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users and GHAS by active committers, all of which can be limited to reduce waste

## GitHub Copilot

Provides AI-powered completion and suggestions, billed per user
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers and Copilot per user

### Tracking Consumption

Organization settings > *Billing* > *Copilot* to track active users
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise and Copilot by active users, and GHAS by active committers

### Billing Details

Copilot is subscription based, with different subscription options
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers, and Copilot by user subscriptions

[Copilot Pricing](https://github.com/features/copilot#pricing)

### Optimization Strategies

Deactivate Copilot for users who don't need it, and only use it in projects that benefit from AI
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers, Copilot by users - all can be optimised to reduce waste

## Large File Storage (LFS)

GitHub LFS stores large binaries separate from repos
Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers, and Copilot by users, while LFS stores large binaries

### Tracking Consumption

*Billing* > *LFS Usage* to see storage and bandwidth usage
LFS stores large binaries, Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers and Copilot by users

LFS offers 1GB of free storage and 1GB of free bandwidth usage per month
LFS is free within limits, Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers and Copilot by users

[LFS Documentation](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage#about-storage-and-bandwidth-usage)

### Optimization Strategies

Use external storage, delete unreferenced files and enable Git LFS file pruning
LFS is limited by storage and bandwidth, Actions are billed by minute/runner, Packages by storage+transfer, Enterprise by active users, GHAS by active committers and Copilot by users
