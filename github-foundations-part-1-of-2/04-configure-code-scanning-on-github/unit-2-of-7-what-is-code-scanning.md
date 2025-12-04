# What is code scanning?

Code scanning is available for all public repos, and for private repos where GHAS is enabled
GitHub code scanning can automatically generate alerts for insecure code in public repos and in GHAS enabled repos

Scans can be scheduled for set times or triggered by events such as a push
Scheduling or triggering code scanning generates alerts to find existing vulnerabilities and prevent developers from introducing new ones

We will learn about CodeQL, adding the CodeQL workflow and the three ways to set up code scanning
There are three ways to set up code scanning to generate alerts on schedule or trigger to find vulnerabilities

## About code scanning with CodeQL

CodeQL is a code analysis engine that was developed by GitHub
GitHub uses CodeQL to scan code and generate alerts

You can run CodeQL with default option, advanced option for a custom workflow, or in an external CI to upload the results to GitHub
Code scanning can be done on GitHub with default option, a custom workflow file, or from an external CI

CodeQL outperforms static analysers by treating code as data, represented in a database you can query
Code scanning with CodeQL generates a database to represent your code, either from default option, custom workflow file or external CI

CodeQL supports a range of both compiled and interpreted languages
CodeQL supports compiled and interpreted languages, and generates a database to represent your code for code scanning

## Enable CodeQL in your repository with the Default Setup

![Security Tab](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/2-security-tab-screenshot.png)
![Setup Code Scanning](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-set-up-code-scanning-button-screenshot.png)

## Enable CodeQL in your repository with the Default Setup

![Security Tab](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/2-security-tab-screenshot.png)
![Setup Code Scanning](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-set-up-code-scanning-button-screenshot.png)

1. Mavigate to repo main page
2. Select *Security*
3. Select *Set up code scanning* (if not available ask for GHAS)
4. Select *Default*
5. Review options and select *Edit* in bottom-left if needed
6. Select *Enable CodeQL*

CodeQL supports compiled and interpreted languages, generates a database to represent code for code scanning, and can be enabled from the GUI

The default option is only one option for CodeQL
CodeQL can be enabled by the default option, the advanced option for custom workflow files, or from an external CI tool

Accounts have storage and minutes limits, so running code scanning beyond these will incur bills
CodeQL can be enable by the default option, the advanced option for custom workflow files, or from an external CI tool, within account limits or incurring extra billing

## About Billing for Actions

Code scanning uses GitHub Actions, so it is free for public repos and billed as Actions for private repos
CodeQL can be enabled by default option, advanced option with custom workflow file, or from an external CI tool, and it uses Actions minutes
