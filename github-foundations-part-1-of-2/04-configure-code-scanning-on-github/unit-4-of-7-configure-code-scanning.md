# Configure code scanning

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

You can configure the frequency of code scans to fit your project
> Configuring Code Scanning saves time and resources

Selecting the Advanced Setup option generates a custom workflow file that you can save to your repository
> Code scanning can be configured with a custom workflow or external CI

You can set the frequency of scans, languages, directories or file types to scan, and what to look for in the scan
> Each code scanning workflow can be customised (e.g. configure CodeQL to scan at 12pm, then another tool to scan at 1pm)

## Switching from Default to Advanced Code Scanning Setup

1. *Settings* > *Code security and analysis* > *Code scanning* section
2. **...** overflow icon
3. Select *Switch to advanced* from drop-down
4. Follow the prompts
5. Disable CodeQL and re-enable it with Advanced Setup

> Even if you already have CodeQL Default Setup, you can switch to Advanced Setup for a custom workflow

## Edit code-scanning workflow

GitHub saves workflow files in the *.github/workflows* directory of your repository
> We should configure workflows for CodeQL and other tools to customise them for our needs

![Edit Button](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/2-edit-button-screenshot.png)
![Commit Changes](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/4-commit-changes.png)

1. Open the workflow file editor
2. Make changes to suit your needs
3. Save the file and commit changes 

> You can edit a workflow file the same as any other file, customising the code scanning for your repo

### Configure frequency

You can configure workflow frequency on a schedule to stay up to date with the latest vulnerabilities, and also by trigger events to prevent mistakes being introduced
> We should configure workflows for CodeQL and other code scanning tools to stay up to date, catch mistakes early and meet all our security requirements

#### Scan on Push

By default CodeQL scans on push for the default branch and protected branches, but a branch must have a copy of the workflow for this to work
> We should configure custom workflows for code scanning and make sure the workflows exist in the required branches

Code scanning alerts will appear in the *Security* tab, and for open pull requests they will also appear with the other pull request alerts
> We should configure custom workflows for code scanning, make sure they exist in every branch we want to scan, and regularly check alerts

#### Scan on PR

The CodeQL default is to scan on pull requests targeted against the main branch, but it can only do this with PRs from forks if running workflows from forks is enabled in repo settings
> Code scanning workflows can be configured to scan on schedule, on push and on PR, but the workflow must exist and workflows be able to run on the branches where scanning is needed

Scanning the merge commit is more accurate than scanning the head of the branch, so scan on PR is preferred to scan on push when possible
> Code scanning workflows should, where possible, scan on PR to prevent mistakes and on a schedule to keep up to date with the latest CVEs

### Define the severities causing pull request check failure

By default only alerts with security level `Error` or security severity level of `Critical` or `High` cause a PR check to fail, but this can be changed
> Code scanning workflows allow us to trigger scans by event, set regular scanning schedules and define criteria for merging code

![Settings](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-severities-2-settings-screenshot.png)
![Security Analysis](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-severities-3-security-analysis-screenshot.png)
![Severity](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-severities-4-level-severity-screenshot.png)

1. Go to your repository Settings
2. In the left sidebar, select *Code security and analysis*
3. *Code scanning* section > *Protection rules* subsection > use the drop-down menu

> Custom workflows can trigger scans on push, on pull request and on a regular schedule, but PR check criteria are set in repo settings

### Avoid unnecessary scans of pull requests

You can use `on:pull_request:paths` and `on:pull_request_paths-ignore` to specify which paths need scanning, so if a PR has no changes to them it will not be scanned
> Custom workflows are configured to schedule scans to stay updated, trigger scans by event to prevent mistakes and ignore paths that don't need scanning to avoid unnecessary scans

```
on:
   push:
      branches: [main, protected]
   pull_request:
      branches: [main]
      paths-ignore:
         - '**/*.md'
         - '**/*.txt'
```

### Adjust scanning schedule

The default CodeQL schedule scans once per week at a randomly generated time, but we can change this with the `cron` value
> Custom workflows can be configured to set the schedule, the trigger events and the necessary paths to scan, while PR check criteria can be changed in repo settings

For example, the following workflow scans every push to the default and protected branches, every PR to the default branch, and the the default branch at 14:20 UTC every Monday:

```
on:
   push:
      branches: [main, protected]
   pull_request:
      branches: [main]
   schedule:
      - cron: '20 14 * * 1'
```

> Code scanning workflows are configured with push and pull request events to trigger scans, cron for scheduling scans, and the paths to scan
