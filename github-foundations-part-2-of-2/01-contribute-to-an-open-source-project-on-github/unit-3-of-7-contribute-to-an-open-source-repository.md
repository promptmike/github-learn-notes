# Contribute to an open-source repository

> 📘 Note: These notes follow a two-line progressive summary method.  
> The apparent repetition is intentional — each line consolidates previous material to reinforce recall.

We will learn how to offer contributions and make pull requests
> Following best practices improves the chance your PR will be accepted

Communication is highly important to collaborating on a project
> We must follow best practices and communicate with others

Frequent communication avoids duplication of work and contributions that do not advance the project's goals
> We must communicate often and check each project's best practices

Be patient and open minded - maintainers usually have day jobs and private lives to tend to
> We must communicate often, patiently await response and check best practices for each project

## Communicate your intent to maintainers

[Check Issue](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-checks.png)

Indicate intent to contribute before you begin using the issue tracker, unless directed otherwise by the README
> We must communicate our intentions and check project best practices

Check assignees and linked PRs to check no one is already working on an issue, then post a comment to indicate your intent to work on it
> We avoid duplications by communicating our intentions and following project guidelines

If you want to work on a new feature, create a new issue and ask for the maintainers' approval
> We avoid duplications and unwanted feature work by communicating our intentions and following project guidelines

## Create a pull request on a GitHub repository

**Pull Request contents**
- Title and description of changes
- One or more commits
- Comments for discussion of changes
- Code reviews for feedback
- Status checks

> We avoid duplications and unwanted work by communicating our intentions, following project guidelines and crafting careful pull requests

A PR can be updated with new commits, comments or code reviews until it is closed (either rejected or merged)
> We avoid duplications and maximise code quality by communicating our intentions, following project guidelines and contributing thoughtfully to PRs

### Create a pull request step by step

[Fork](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-fork.png)
[Repositories](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-my-repositories.png)
[Clone](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-clone.png)
[PR Suggestion](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-pr-suggestion.png)
[Create PR](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-create-pr.png)
[Issue Number](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-issue-number.png)

1. Open GitHub page of project
2. Select *Fork*
3. Select *Your Repositories* from the profile menu
4. Select the repository fork
5. Select the *Code* button
6. Use a clipboard icon to copy the URL you want and paste in your terminal
    - `git clone <REPOSITORY_URL>`
    - add credentials to URL if needed
7. `cd <PROJECT_FOLDER>`
8. (Optional) Create a new branch
    - `git checkout -b <BRANCH_NAME>`
    - Optional, but recommended for making multiple contributions
9. Make changes and commit
    - `git add .`
    - `git commit -m "<COMMIT_MESSAGE>"`
    - Describe your changes accurately and check the CONTRIBUTING file for commit message guidelines
10. Push to remote
    - `git push --set-upstream origin <BRANCH_NAME>`
    - This creates a new branch on the upstream repo (your fork) and pushes your commits to it
11. Open your fork on GitHub and select *Compare & pull request**
12. Write a title and description, then select *Create pull request*
    - Provide context for maintainers to understand changes
    - Link related issue by `#<ISSUE NUMBER>`
    - If there is a PR template, fill in all the details carefully

> Use the proper procedures for PR, communicate intentions clearly and follow project guidelines

**❗ ==Note==**
When we talk about an upstream repository, we refer to the remote repository linked to your local repository. The `origin` is the default alias for the repository URL, which was created by Git in step 4.

## Pass the status checks

[PR Checks](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-pr-checks.png)

Maintainers implement automated checks to ensure quality.
> Communicate intentions clearly, follow project guidelines and write high quality code

If a status check fails, you can select the *Details* button to learn about the failure
> Communicate intentions clearly, follow project guidelines and investigate failures to improve code quality

If you don't know how to fix a failing check, you can use the comments or speak to the maintainers to ask for help
> Communicate intentions clearly, follow project guidelines, investigate failures and ask for help when needed

## Ask for guidance or reviews on pull requests

[Draft PR](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-draft-pr.png)

You can ask for guidance by commenting on your PR or even creating a draft PR
> Communicate intentions clearly, follow project guidelines, investigate failed status checks and use the comments to ask for more guidance

**Review Outcomes**
- Changes approved: PR merged
- Requires changes: Read the feedback and make the requested changes
- Reviwer comments: Usually indicates more details are needed

### Respond to comments on your pull request

Be respectful and follow the code of conduct
> Communicate intentions clearly, follow project guidelines, investigate failed status checks, use comments to ask for more guidance and engage respectfully with others

DO NOT reach out to maintainers privately hoping for a faster response (stand in line with everyone else)
> Communicate intentions clearly, follow project guidelines, follow best practices, investigate status checks, use comments to ask for more guidance and engage respectfully
