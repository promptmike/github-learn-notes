# How to maintain a secure GitHub repository

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will learn repo admin tools
> Repo admins are responsible for security

**❗ ==Note==**
This content focuses on important security considerations, tools, and features to use within a GitHub repository.

## The importance of a secure development strategy

Application security is important to avoid data breaches
> Repo admins must support application security

We must make sure that information is only accessed, altered or destroyed when appropriate
> Repo admins must protect information

We must authenticate those who access information and keep logs for future triage
> Repo admins must authenticate access to information and keep logs

**Considerations:**
- **General knowledge:** Developers and staff must be educated on security practices
- **Code security:** Features designed with security in mind, implemented with secure code.
- **Compliance:** Code must meet rules and regulations

### Security at every step

![GitHub Security](https://learn.microsoft.com/en-us/training/github/maintain-secure-repository-github/media/github-security.png)

Security must be implemented at every stage of development; you cannot just add it later
> Repo admins must take responsibility for secure development practices

**Shift left** - complete processes earlier in the development cycle
> Repo admins should *shift left* on security, ensure authentication and keep logs

Security concepts were often neglected in the past in favour of faster development
> Repo admins should shift left, authenticate access and keep logs to respond to current security considerations

DevOps practices make it easier to integrate security into the whole development process
> Security should be part of day-to-day operations, shifting left to stay ahead

DevOps catches issues earlier, saving time later
> DevOps security should authenticate access, keep logs, and always shift left

Security should centre on developers
> DevOps security should authenticate access, communicate with developers, keep logs and always shift left

### Security tab features

![Security Tab](https://learn.microsoft.com/en-us/training/github/maintain-secure-repository-github/media/security-tab.png)

**Security Tab**
1. GitHub.com > Main Page
2. Select *Security* under the repository name

> We can access GitHub security features in the security tab

**Security feature examples**
- **Security policies:** Use `SECURITY.md` to explain how to report a vulnerability
- **Dependabot alerts:** Get notified of malware and vulnerable dependencies
- **Security advisories:** Privately discuss, fix and publish information
- **Code scanning:** Find, triage and fix errors
- **Secret scanning:** Detect tokens, credentials and secrets committed

> GitHub has automated security tools to enable a DevOps workflow

[GitHub Security Features](https://docs.github.com/en/code-security/getting-started/github-security-features)

## Communicate a security policy with SECURITY.md

Contributors should responsibly disclose vulnerabilities using the policy in `SECURITY.md`
> GitHub has automated security tools for DevOps and a dedicated place for security policy in every repo

[Adding a Security Policy to your repository](https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository)

## GitHub Security Advisories

Security advisories are initially a private space to discuss and fix a vulnerability, then become public after publishing to the CVE list to help those affected by the bug
> GitHub authentication, logs, security policies and security advisories for secure DevOps

[About repository Security Advisories](docs.github.com/code-security/security-advisories/working-with-repository-security-advisories/about-repository-security-advisories)

## Keep sensitive files out of your repository with .gitignore

`.gitignore` helps avoid accidentally commiting sensitive data by instructing client tools to exclude specific paths and patterns
> DevOps should set authentication, security policies and `.gitignore`, open security advisories and make use of logs

**Example `.gitignore`**
```
# User-specific files - Ignore all files ending in ".suo"
*.suo

# Mono auto generated files - Ignore all files starting with "mono_crash."
mono_crash.*

# Build results - Ignore all files in these folders found at any folder depth
[Dd]ebug/
[Rr]elease/
x64/
x86/

# Root config folder - Ignore this directory at the root due to leading slash
# Removing the slash would ignore "config" directories at all depths 
/config

# Ignore intermediate JS build files produced during TypeScript build at any 
# folder depth under /Web/TypeScript. This won't ignore JS files elsewhere. 
/Web/TypeScript/**/*.js
```

A repo can have multiple `.gitignore` files, inheriting settings from parent directories
> DevOps should set security policies and make thoughtful use of `.gitignore` structures

[Ignoring files](https://docs.github.com/en/get-started/git-basics/ignoring-files)
[gitignore starter templates](https://github.com/github/gitignore)

## Remove sensitive data from a repository

`.gitignore` is not a guarantee, so remain alert to sensitive data in commits
> DevOps should set security policies, open security advisories and always be alert to vulnerabilities.

**❗ ==Important==**
You should assume that any data committed to GitHub at any point has been compromised. Simply overwriting a commit isn't enough to ensure the data won't be accessible in the future. For the complete guide to removing sensitive data from GitHub, see [Removing sensitive data from a repository](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)

## Branch protection rules

Branch protection rules allow you to protect a branch by requiring a specific workflow
> DevOps should set careful security policy, attend to security advisories and use branch protection

**Example rules:**
- Run a build to verify code changes can be built
- Run a linter
- Run automated tests

## Required reviewers in pull requests

You can make a repo more secure by requiring reviews of all pull requests
> DevOps should keep everyone informed of current security policy, while guarding the codebase against errors and malware

**Configure required reviewers:**
1. GitHub > Repository
2. *Settings* > *Branches*
3. *Add rule* to branch
4. Select *Require pull request reviews before merging*
5. Optionally:
    - *Require review from Code Owners*
    - *Dismiss stale pull request approvals when new commits are pushed*
    - *Require approval from someone other than the last pusher*

Required reviews cannot be bypassed without admin permissions, so the codebase is protected
> DevOps should always shift left with authentication, security policy, security advisories and branch protections

[About Protected Branches](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches)

## Add a CODEOWNERS file

You can add people as code owners in `CODEOWNDERS` to require them for PR reviews
> DevOps should shift left with authentication, security policy, security advisories, branch protections, and assigning code owners

**Example `CODEOWNERS`**
```
# Changes to files with the js extensions need to be reviewed by the js-owner user/group:
*.js    @js-owner

# Changes to files in the builds folder need to be reviewed by the octocat user/group:
/build/ @octocat
```

You can create the `CODEOWNERS` file in root, `docs` or `.github`
> DevOps should assign code owners, authenticate access, provide security policy, open security advisories, configure branch protections, and always shift left
