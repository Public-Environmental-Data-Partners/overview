# git tips

## install git

Go to git's offical [download page](https://git-scm.com/install/) to install the appropriate version of git for your machine. Follow any installation steps provided.

## using a GUI

If you don't want to use the command line for using git, you can always use Github's [desktop application](https://desktop.github.com/download/). If you do that, please follow Github's turotials.

## adding git to a project

If your project is not version-controlled through git yet and you want to add git, simply navigate to the root of that project directory in your terminal and run:

    git init

This will initialize git tracking in the repo and you can add/remove/commit files from here.

## working with an existing git project

If you're working with an existing git project, you'll need to clone that project to your local machine. If you're the repository owner and you want to work directly with the repo, then you can simply clone the repo:

    git clone <url>

If you're working on someone else's project, like a PEDP project, you will need to fork the repo and then clone your fork, and then follow the pull request described in our [CONTRIBUTING guide](/CONTRIBUTING.md#code-and-documentation-changes).

## stage files for commit

When you are ready to commit changes (i.e. save a version of your code), you need to stage (i.e. add) the files for commit.

To add specific file:

    git add <file>

To add all files in your current directory:

    git add .

To add all changes everywhere in the project:

    git add -A

## commit

Now that you've staged your files that you want to commit for this version, think of a short message that concisely communicates the changes you've made (e.g. "added ETL for EPA dataset").

To commit staged changes:

    git commit -m "Your message"

## push your latest version

Your commit has now saved locally, but your repo online still needs the update. Push your local version to the remote (i.e. online/Github) repo:

    git push

## pull the latest version

- Pull latest changes from remote
    - git pull

## view history

Use these commands to view the repo's commit history.

Full log:

    git log

Last 5 commits:

    git log -5

## Other Useful Commands

Check which files have been changed and which of those have been staged for commit:

    git status

See what has changed line-by-line in your files:

    git diff

## Useful Combinations

Quick commit all changes:

    git add -A && git commit -m "message" && git push

See the difference between what will be pushed and what is in the remote repo:

    git diff origin/master

Sync with upstream (for forks):

    git fetch upstream
    git merge upstream/master
