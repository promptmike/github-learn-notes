# Automated security

> 📘 Note: These notes follow a two-line progressive summary method.
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will discuss how administrators can automate security checks.
> Automated checks can improve security.

## Detect and fix outdated dependencies with security vulnerabilities

GitHub has features to help manage external dependencies.
> Automating external dependencies improves security.

### Repository dependency graphs

Dependency graphs like `package.json` or `requirements.txt` help you to recursively track dependencies.
> Automatic recursive dependency tracking improves security by keeping packages up to date.

![Dependency graph](https://learn.microsoft.com/en-us/training/github/maintain-secure-repository-github/media/2-dependency-graph.png)

[About the dependency graph](https://docs.github.com/en/code-security/concepts/supply-chain-security/dependency-graph)

### Dependabot alerts

Dependabot watches your dependency graphs to check for known vulnerabilities
> Recursive dependency tracking and automatic alerts reduce the risk of CVEs

![Dependabot alerts](https://learn.microsoft.com/en-us/training/github/maintain-secure-repository-github/media/2-dependency-alert.png)

### Automated dependency updates with Dependabot

Dependabot automatically makes pull requests to update dependencies from vulnerable versions
> Recursive dependency tracking and automated update requests reduce the risk of CVEs creeping in through out of date dependencies

[Configuring Dependabot security updates](https://docs.github.com/en/code-security/how-tos/secure-your-supply-chain/secure-your-dependencies/configure-security-updates)

### Automated code scanning

Code scanning automatically looks for known vulnerabilities in code.
> Code scanning improves code security and Dependabot improves dependency security.

Code scanning supports CodeQL so you can use custom queries on code as data.
> Code scanning looks for security vulnerabilities and fascilitates CodeQL queries, while Dependabot looks for dependency vulnerabilities and makes automated pull requests to fix them.

Enable code scanning from the Security tab:
![Security overview](https://learn.microsoft.com/en-us/training/github/maintain-secure-repository-github/media/security-overview.png)

[Learn more about code scanning and CodeQL](https://docs.github.com/en/code-security/concepts/code-scanning/code-scanning)

### Secret scanning

Secret scanning looks for secrets or credentials within the code.
>Use code scanning, secret scanning and Dependabot alerts to maximise security.

When secret scanning detects credentials, GitHub notifies the service provider who issued them.
>Use code scanning, secret scanning and Dependabot alerts to maximise trust and security.

[Learn more about secret scanning](https://docs.github.com/en/code-security/concepts/secret-security/secret-scanning)
