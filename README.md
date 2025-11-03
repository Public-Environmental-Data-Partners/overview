# Overview

Welcome! This repo contains information and resources about Public Environmental Data Partners' Github use and open source practices to help people get involved in our work.


1. [Mission](#mission)
1. [How We Work](#how-we-work)
1. [Getting Started](#getting-started)
    1. [What should be a PEDP repo?](#what-should-be-a-pedp-repo)
    1. [Creating a repo](#creating-a-github-repo)
        1. [Archiving an external project](#archiving-an-external-project)
        1. [Building on an archived project](#building-on-an-archived-project)
        1. [Creating an original project](#creating-an-original-project)
    1. [License](#license)
    1. [Issue templates](#issue-templates)
1. [Getting Contributor-Ready](#getting-contributor-ready)
1. [Funding](#funding)
1. [Credits](#credits)


## Mission
The [Public Environmental Data Partners](https://screening-tools.com/) Github organization is primarily maintained by the Tool Dev Working Group. Our working group's mission is to strengthen our collective understanding of the climate and environment and promote science, participatory governance, and justice by designing and building useful and accessible open-source tools for communities, researchers, and the public.


## How We Work

This project is a collaborative endeavor. We respect one another and embrace a culture of learning and of gratitude. We are non-hierarchical. We share the responsibilities and workload of the project, and we share credit for the work that is accomplished. As a project team, we explicitly support science, data and information integrity, public access, democracy, and civic engagement. 

We use Github and Github Projects to manage our open source software development and archiving. 

We expect contributors to review and abide by our [Code of Conduct](/CODE_OF_CONDUCT.md) and [Contributor Guidelines](/CONTRIBUTING.md).


## Getting Started

**New to PEDP?** Visit our [Get Involved page](https://screening-tools.com/get-involved) to read our organizational Working Agreements, privacy guidance, and fill out our volunteer interest form. Once you've filled out the form, we will be in touch with next steps for orientation and onboarding to our communication tools. 

While onboarding to our chat may make communication about projects easier, you *do not* need to fill out the volunteer form to contribute to our open source projects. Feel free to check out our [repos](https://github.com/orgs/Public-Environmental-Data-Partners/repositories) and browse [good first issues](https://github.com/issues?q=is%3Aopen+is%3Aissue+label%3Agood-first-issue+user%3APublic-Environmental-Data-Partners) to get started!


For everyone, please refer the guidelines below for creating repositories and working on Github.

### What should be a PEDP repo?

* Any repo containing a software project created or maintained primarily through PEDP and/or funded by PEDP.
* Any project that has been archived/replicated by PEDP through our software preservation efforts

### Creating a repo
There are three typical scenarios for PEDP project repos on Github: [Archiving an existing project from another source](#archiving-an-external-project), [building on an existing archived (or forked) project](#building-on-an-archived-project), and [creating a new project containing original sourcecode](#creating-an-original-project).

Each project repository requires, at a minimum:

* License
* Readme with a note about project status and maintenance by PEDP

For each project that goes beyond simply archiving or replicating an external project, the repo additionally requires:

* Contributing Guidelines
* Code of Conduct

We also use the following standard repo configurations:

The default branch name should be `main`, not `master`. (See [GitHub’s docs on default branches](https://help.github.com/en/github/administering-a-repository/setting-the-default-branch) for instructions.)


#### Archiving an external project

Guiding principles and conventions for replicating or cloning another project:

* Honor what the project was originally for and preserve as much source information as possible, e.g. (potentially legacy) URLs, teams, associated organizations and offices. Project files such as READMEs may not always follow familiar conventions, but we want to preserve them or the information they provide regardless.
* Preserve identifying or contact information in repos: These are tacit forms of authorship attribution and provide a historical record. Leave unless an identified individual explicitly asks to have their information removed.
* License: Keep the original license file as is if you do not plan to make changes to the code. Follow guidance below if you intend to make substantive changes to the repo.

##### Steps for replicating:

When forking a Github repo:

1. Make sure you have the correct access to the PEDP Github organization.
1. Fork the repo to the PEDP Github organization.
1. Update the repo’s About to say: “PEDP’s working copy of” followed by the project name and info.
1. Update the repo’s README.md file to add the following text to the top of the file, filling in the relevant info and modifying as needed. Using Github’s UI to do this and committing directly to the main branch is simplest.


	This repo contains the code, processes, and documentation for the former PROJECT NAME. It was forked on DATE. This fork is maintained by the Public Environmental Data Partners. 


When obtaining code from outside of Github (e.g. FOIA request):

1. Make sure you have the correct access to the PEDP Github organization.
1. Make sure you have git installed locally.
1. Create a new empty repo with the desired project name.
1. Update the repo’s About to say: “PEDP’s working copy of” followed by the project name and info.
1. In your local environment, set up git for this project:
	1. If the project is not already using git, navigate to the project’s directory in the terminal or command line and run git init. Add everything to git (`git add .`) and commit (`git commit -m "Initial commit"`)
	1. If necessary, add an appropriate `.gitignore` file to avoid committing non-source files
	1. Add the remote, replacing URL with the Github repo’s https url : `git remote add origin URL`
	1. Push the code to github: git push origin main
1. Update the repo’s README.md file to add the following text to the top of the file (modifying as needed):

	This repo contains the code, processes, and documentation for the former PROJECT NAME. The contents of this repo was received from SOURCE by METHOD [e.g. FOIA request] on DATE. This repo is maintained by the Public Environmental Data Partners.


For all repos:

1. If the repo has no license and was originally created by the US Government: Add a `LICENSE.txt` file to the repo using the following text (fill out the relevant info).

	As a product of the US Government, the project REPO_NAME exists in the public domain and its copyright is held by the US Government as of DATE_OF_RETRIEVAL.

1. If the repo has no license and was **not** created by the US Government, contact the original owner to confirm licensing and copyright and update the repo accordingly.
1. If the project requires other tasks for proper archival, create a project board for the repo and add those tasks as issues to the backlog. Assign the proper labels to them (e.g. help wanted or good first issue).


#### Building on an archived project

Guiding principles for building on a project that was previously simply a replica or archive of an existing project:

* It should be clear in the repo what PEDP’s goals are for changes, as well as the current status of the project and how to get involved.
* It should be clear in the repo when PEDP started to make changes, and what commits are from PEDP versus from the original source.
* We want to ensure that new code and other enhancements we make to the project are protected by a strong copyleft license, to prevent others from using our work to create proprietary tools that further injustice.

##### Steps for Github changes:

1. Update README to provide more information about your goals and the status of the project.
1. Ensure the repo’s CONTRIBUTING file or similar information is up-to-date with the relevant info. You can use the PEDP [template for contributor guidelines](https://github.com/Public-Environmental-Data-Partners/template/blob/main/CONTRIBUTING.md).
1. Ensure the repo has an up-to-date CODE OF CONDUCT that is or complies with [PEDP’s](https://github.com/Public-Environmental-Data-Partners/overview/blob/main/CODE_OF_CONDUCT.md).
1. Update the LICENSE file to note PEDP as the new copyright owner after a given date and using the AGPL license for PEDP changes. **Note**: this assumes that the previous license does not require modifications to be released under the same license. If it does, leave out the text of the GNU AGPLv3 license and replaced “licensed under GNU AGPLv3” with the original license.

	Copyright for portions of this repository REPO NAME before DATE are held by the US Government and are licensed under LICENSE (link to license). Copyright for portions of REPO NAME created on or after DATE (beginning with commit COMMIT-SHA) are held by Public Environmental Data Partners and licensed under [GNU AGPLv3](https://github.com/Public-Environmental-Data-Partners/overview/blob/main/LICENSE).

1. Flesh out your project board with issues capturing the work to be done. Label issues appropriately, e.g. with “help wanted” or or “good first issue” 


#### Creating an original project

Sometimes we create new and original software tools to advance PEPD's mission. Those codebases should live as open source projects on Github and use the [template repo](https://github.com/Public-Environmental-Data-Partners/template) provided.

#### Steps for Github:

1. Create a Github repository (repo) 
1. Open PEDP org in Github
1. Click NEW 
	1. Enter Repository Name in [kebab case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case)
	1. Provide a Description of repo
	1. Choose the visibility (private/public). Projects should default to public unless there is a good reason to keep it private.
	1. Start with a template: select the PEDP template. This will set up the readme, code of conduct, license, etc, for your repo.
	1. Click Create repository
1. Add the project team as members to the PEDP organization and grant them appropriate access to the Github rep
1. Create a Github Project under the PEDP Organization and link it to your repo


### License
[AGPLv3](LICENSE) is our preferred license for PEDP code. 

When an archived project has another license, we maintain the original license in that project's repo. When we begin adding new code, content, or other material to the project, we update the license file to note that contributions after the date of archival (usually accompanied by a commit SHA) are licensed under AGPLv3. See the steps above for more detail.

### Issue templates
We recommend using issue templates for Github repos to make consistent, thorough issue creation easier. Our [template repo](https://github.com/Public-Environmental-Data-Partners/template) contains suggested [issue templates](https://github.com/Public-Environmental-Data-Partners/template/tree/main/.github/ISSUE_TEMPLATE, including Spanish versions.

## Getting Contributor-Ready

### Add your project's contributing guidelines
Your project repo should have a CONTRIBUTING.md file that looks a lot like [the one in our template repo](https://github.com/Public-Environmental-Data-Partners/template/blob/main/CONTRIBUTING.md), which links to the canonical guidelines available [here](/CONTRIBUTING.md) in our overview repo and leaves space for any additional guidelines specific to your project. 

Fill out that placeholder space with any additional info or steps that contributors should be aware of for your proejct, e.g. how to use custom issue templates.

### Flesh out your project plan
Your repo should have a linked project board that organizes issues into a kanban-style board so that your team and contributors can see what is planned and in progress. Create issues for your repo with a sufficient level of detail and context and then put them in the relevant columns in your project board. 

Identify which issues are "Good first issues" (see below), which you are lookijng for help to complete, which are bugs or features, etc, and label them appropriately.

### “Good first issues”
Good first issues are issues on your project repo that would be good for newcomers who have never contributed to your project before. They are intended to be good entrypoints to the project that help a new contributor get familiar with the codebase and get excited about becoming a regular contributor. They give a clear and quick path to that joyous satisfaction of having completed a task and feeling appreciated.

Traits of a good first issue:
* Can be completed by a new contributor in under a couple of hours
* Should require zero or minimal context gathering outside of what’s available in the github repo (e.g. docs, code, conversation in the issue)
* Is clearly documented with a concrete definition of done
* Is a standalone issue that is not a dependency or blocker to another issue or pull request getting resolved

Examples:
* Creating a translation of a webpage or documentation
* Adding documentation for a feature or technical task
* Fixing a small, not-critical bug
* Improving mobile responsiveness
* Changing the color of a component


## Funding

*Our work is made possible through volunteer labor, grants, and tax-deductible donations from the public.*

**[Donate to PEDP](https://screening-tools.com/donate)** 


