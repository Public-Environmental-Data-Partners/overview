# Contributing Guidelines

We're thrilled you're interested in contributing to PEDP projects! There are multiple ways to contribute, such as:

* [Feedback, feature requests, and bug reports](#feedback-requests-and-bug-reports)
* [Code and documentation changes](#code-and-documentation-changes)
* [Security](#security)
* [Testing](#testing)
* [Translation](#translation)
* [Design system](#design-system)

For other types of contribution to PEDP, such as data preservation, advocacy, and promotion, please reach out using our [volunteer interest form]().

No matter the type or place of contribution, we expect contributors to agree and adhere to our organizational [Working Agreements](https://docs.google.com/document/d/1KyngJ8K7FMUlic2G3OonZEBwoTH85hWO88oX-38URKM).

As a collaborative organization maintaining open-source projects, we value and respect each community member. However, contributing doesn't guarantee that new changes will be merged or that feedback or requests will be prioritized. Factors that influence this decision include, but are not limited to, the contribution's quality, alignment with the project's goals or roadmap (which may change), impact on the codebase's stability, and the resources required to implement or support it.

We understand that putting time and effort into a contribution only for it to be rejected can be disheartening. However, the aim is always to ensure that our projects remain high-quality, maintainable, and focused on meeting the project's and its users' needs. *Please do not take the rejection of a specific contribution as a rejection of your participation in the project!*

_These guidelines are based on [EDGI's](https://github.com/edgi-govdata-archiving/overview/blob/main/CONTRIBUTING.md) and [RocketChat's](https://developer.rocket.chat/v1/docs/modes-of-contribution)._

## Feedback, requests, and bug reports
For submitting feedback, feature requests, or bug reports, you can begin the conversation in our chat or create an issue on the relevant project repo in Github. Each project repository generally maintains its own set of issues:

    https://github.com/Public-Environmental-Data-Partners/<repository-name>/issues

Some projects have additional templates or sets of questions for each issue, which you will be prompted to fill out when creating one.

Issues that relate to how we work overall are in the [Overview project board](https://github.com/Public-Environmental-Data-Partners/overview/projects?query=is%3Aopen).

For issues submitted in Github, project maintainers aim to review and respond to the submitted issue within a reasonable timeframe (projects tend to meet every week or every other week).


## Code and documentation changes

We love contributions, whether code or documentation (or both!). Our process for accepting changes operates by [Pull Request (PR)](https://help.github.com/articles/about-pull-requests/) and has a few steps:

1. If you haven't submitted anything before, and you aren't (yet!) a member of our organization, fork and clone the repo:

    $ git clone git@github.com:<your-username>/<repository-name>.git

Organization members should clone the upsteam repo, instead of working from a personal fork:

$ git clone git@github.com:Public-Environmental-Data-Partners/<repository-name>.git

2. Create a new branch for the changes you want to work on. Choose a branch name that reflects the subject of the change, e.g. `map-layers` for a branch tackling adding layers to a map.

	git checkout -b <branch-name>

3. Create or modify the files with your changes and commit them in Git. If you are fixing a known issue, include “fixes #123” (where “123” is the issue number) in one of your commit messages to help automatically link everything together.

4. Once your changes are ready for review, push your commits to GitHub and create a pull request (PR). If you aren’t ready for final review and just need some preliminary feedback, create the PR as a draft ([Screenshot]()), and then move it out of Draft status when you're ready for review.

5. Allow others sufficient time for review and comments before merging. We make use of GitHub's review feature to comment in-line on PRs when possible. There may be some fixes or adjustments you'll have to make based on feedback.

In general, we do our best to provide some feedback or review within about 3 days. (And hopefully much quicker most of the time!)

If you have commit rights on the repo, you should merge your own PR, but have someone else review it first:

* Allow up to 3 days for review. If you don’t get any feedback by then, you can merge it without review.
* If you have a urgent [hotfix](#hotfixes), please bug someone on Slack for rapid review, but you may merge without if nobody can.
* If you have a drastic change (e.g., one that might break everyone’s development environment), consider allowing extra time beyond 3 days for others to review. There aren’t hard rules here—being given commit rights is a sign of trust that you’ll make reasonable decisions. When in doubt, opt for more time & feedback rather than less.

Anyone with commit rights can review, but you are expected to be reasonable about whether you should. For example, you should probably ask someone else to review if you don’t know much about the part of the codebase being worked on. If you are reviewing a PR, think about whether others need to review it in addition to you and request them through GitHub or poke them on Slack.

If you don't have commit rights: 

Once you have integrated comments, or waited for feedback, a project maintainer should merge your changes in!

When merging PRs, we generally use the “squash and merge” feature on GitHub so that each PR has a single, clear commit, and so that the commit title links back to the PR by its number. This isn’t a hard rule. If you have a specific reason to do an actual merge or a rebase, then do so.

### Hotfixes

A hotfix is a quick solution to an active, serious problem that is causing unrecoverable data loss, whole systems to be unavailable, etc. The hotfix may be the minimum intervention necessary to address the failure, but will likely not be ideal (since it needs to be designed, programmed, and deployed quickly). It should be reviewed by someone else, but may be merged and deployed without review if nobody is available within a short timeframe. The hotfix should almost always be reviewed again after deployment and, if necessary, a better long-term fix should be planned.

To make the situation clear, you should prefix commit messages and PR titles with `HOTFIX:`.

## Security
Help keep our projects secure by improving security measures or reporting potential security issues. For code-related vulnerabilities, please report by creating issues in the relevant project's repo. We encourage you to also submit a pull request with a fix following the PR process described [above](#code-and-documentation-changes). 

For all other security concerns, please reach out by submitting our volunteer interest form and joining our chat.

## Testing
Participate in the testing process of our various projects. Your performance, usability, and overall experience feedback can help refine the platform and ensure a seamless user experience. Testing on multiple devices or operating systems 

Report bugs you encounter or any other usability feedback by creating issues following the [feedback process](#feedback-requests-and-bug-reports).

If you would like to contribute automated tests that run in CI/CD, please follow the [code change process](#code-and-documentation-changes).

## Translation
Assist in making PEDP projects accessible to non-English speakers by improving existing translations or introducing new ones. Your linguistic skills can help break down language barriers and make our projects more useful and impactful a broader spectrum of users.

The best way to propose new translations or large translation improvements is to begin a conversation with the project team before starting on translation work, either on our chat or by creating an issue outlining what you think is necessary. This way you can make sure you and the project team are aligned on community needs, user experience goals, and a testing/verification process.

For small translation improvements, please use the [bug reporting process](#feedback-requests-and-bug-reports) to request a change or [code change PR process](#code-and-documentation-changes) to submit one.


## Design System
We have a PEDP Design System whose work is being managed on [this project board](https://github.com/orgs/Public-Environmental-Data-Partners/projects/6). Please start a conversation about contributing by commenting on an existing issue on that board, creating a new one, or discussing with the project team on our chat.
