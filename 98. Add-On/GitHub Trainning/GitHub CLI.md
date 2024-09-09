# Tutorial: GitHub CLI (Command Line Interface) #

## In this article and tutorial, learn about how to interact with your repository’s GitHub Issues and pull requests, right from the terminal! ##

GitHub CLI is a powerful command-line tool that enables developers to handle several of the critical functionalities of GitHub from a terminal. We can see open issues, make pull requests, link pull requests to issues, and even merge pull requests without touching the GitHub UI.

In this tutorial, you’ll download the GitHub CLI and practice a few commands on an existing project.

## Installation ##

Download and execute the installer for your operating system from the  GitHub CLI public webpage. Once the installation is complete, open a new terminal and verify the default configuration: 

    gh --version 

Review the list of the supported APIs and functionalities: 

    gh --help

## GitHub CLI in action ##

Fork the try-GitHub-cli-off-platform-project repository to your GitHub account and clone it onto your local computer. Next, open a terminal and change the current directory to the directory of the cloned repository.

The repository contains a simple Python application for a Magic Eight Ball. The application, however, has a defect. The code tries to use the Python random library without importing it. 

Login to GitHub from your terminal using GitHub CLI and follow the instructions to complete the authentication.

    > gh auth login

Use the command line to create a GitHub Issue documenting the problem:


    > gh issue create --title "Fix magic8.py error" --body "The code for magic8.py uses the Python random library without importing it. This causes issues during runtime."


Follow the instructions in the terminal and select the forked repository to create the issue. 

https://static-assets.codecademy.com/Courses/learn-git-github/github-cli/github-CLI-create-issue.png

Once the issue is created, you can view it on GitHub web interface under the Issues tab. 

https://static-assets.codecademy.com/Courses/learn-git-github/github-cli/github-cli-resulting-issue.png

You can also use GitHub CLI to  list all opened issues so far:

    gh issue status

Let’s now create a new branch to actually fix the issue. 

    git checkout -b “fix-magic8 ”

Open the magic8.py file using an editor of your choice and add the following line at the beginning of the file to fix the defect: 

    import random

Commit and push your change to the remote. 

    git commit -a -m “Fixed magic8.py file by importing the proper required library”
    git push --set-upstream origin fix-magic8

Now that there’s a full solution to the problem in your branch, it’s time to create a pull request! You can use the command line to directly make a pull request:

    gh pr create

Follow the prompts and add the proper title and description for the pull request. Mention the id of the issue in the description following #[id] format so that GitHub automatically links the pull request to the issue. The following is an example description: 

This pull request imports the random library in magic8.py. Once merged, this resolves #1.

To check if this actually worked, you can check that the new pull request appears under the Pull Requests tab. Also, observe the state of the issue and see that the issue is now linked to the pull request. 

https://static-assets.codecademy.com/Courses/learn-git-github/github-cli/github-cli-linked-pull-request-to-issue.png

Assuming that your pull request is good to go, you can merge your pull request using the following GitHub CLI command:

    gh pr merge

Once the pull request is merged, check back the status of the issues and notice that the issue is now closed and no longer listed under the open issues: 

    gh issue status

## Conclusion ##

Well done! You’ve now successfully used terminal commands to interact with GitHub APIs. GitHub terminal commands streamline code development as they enable developers to integrate a repository’s pull requests and issues into terminal commands and bash scripts. GitHub CLI is a powerful and convenient tool!


Want to learn more about terminal commands? Check out our Bash courses.

