# Introducing Helpful GitHub Features #

In the new few articles and tutorials, you will learn about some GitHub features that can seriously streamline your development process. These are tools to add after you’ve already grasped the basics!

## GitHub Issues ##

GitHub Issues adds project management right to your repository. You can list tasks and organize them into which are open and in progress. These issues can also be referenced in pull requests and even other issues.

https://static-assets.codecademy.com/Courses/learn-git-github/project-management/issues-board-docs.png

## GitHub CLI ##

The GitHub Command Line Interface (CLI) is a tool that allows you to directly access and. modify issues and pull requests right from your terminal!

    > gh issue create --title "Create tutorial for CLI" --body "We need a tutorial for GitHub CLI in our catalog."

## GitHub Actions ##

Want to add automated tests after a pull request is created? Want to trigger something after a branch is merged into main? We can use GitHub Actions!

Let’s learn a bit about these tools!

# Project Management: Issues and Projects #

Learn about issues and projects on GitHub, two features that make it easier to track tasks!

## The Issues Tab ##

When looking at a GitHub repository, we see a tab called Issues. This is a built-in GitHub tracking tool for all the bugs, errors, and potential small feature changes for the project living inside the repository. In one view, collaborators of the repository can see what needs to be worked on (open issues) as well as which tasks were resolved (closed issues). Take a look at the Codecademy docs Issue board:

https://static-assets.codecademy.com/Courses/learn-git-github/project-management/issues-board-docs.png

The issue board acts as a forum for all the collaborators of the repository. In some instances, issue boards are public and users of a project can submit and discuss bugs they’ve encountered.

## Labels ##

To help organize issues when more and more pop up in a project, we can use labels. bug and feature are common labels used to differentiate between errors and new features. In the Codecademy Docs repo Issue board earlier, we could see labels such as Good first issue, if a suggested entry to Docs is new or an edit, and what language the entry should be in, like C# or Java. Labels help us toggle between different types of issues at a glance and have short names.

## Creating an Issue ##

To create an Issue, we can click the New Issue button on top of the Issues board. This will take us to a new page where to set the title and content of the issue.

Issues are a bit like pull requests in that we want to keep the title specific but to the point. For descriptions, repositories often have their own guidelines (just like pull requests do) for including details. For example, if the issue is related to a bug, we should include the error message in the description. Check out a complete issue from the Facebook Folly repository:

https://static-assets.codecademy.com/Courses/learn-git-github/project-management/completed-issue.png

Once the issue is posted and now open, collaborators and other GitHub users can add to the discussion and reference this issue by the # in other issues and pull requests.

## GitHub Project Management ##

GitHub projects is a beta feature (as of late 2021) for project management. While other project management tools exist, like JIRA or even handwritten post-its, GitHub projects allow direct integration within the repository, letting developers stay within the same ecosystem. We can also create automated project boards that trigger the status of issues and pull requests. And… it’s completely free!

To try out projects, we can select the New Project option after clicking the + button on the upper right side of the GitHub dashboard. In most cases, projects are linked to repositories, which already have existing issues and pull requests, but in other cases, projects can be standalone.

https://static-assets.codecademy.com/Courses/learn-git-github/project-management/new-project.png

After filling out the name and description of the new project, a drop-down will appear asking what Project template we want to use.

https://static-assets.codecademy.com/Courses/learn-git-github/project-management/project-types.png

The options range from different types of Kanban boards that can host issues and pull requests to a Bug Triage, which gives details into which bugs are high priority, low priority, or need further investigation. Once the board is created, we will add issues and pull requests to it.

An example of a laid-out GitHub project board is Github’s own public roadmap project, shown next. This is an example of a Project with no repository, as a roadmap can be used for organizational purposes.

https://static-assets.codecademy.com/Courses/learn-git-github/project-management/github-project-board.png

## Conclusion ##

In this article, we learned about two GitHub features that can come in handy for teams: issues and projects. We can use GitHub issues to keep track of tasks that need to be worked on. Those issues can then be referenced in pull requests, comments, or projects. GitHub projects are an even newer feature for project management purposes and can be linked to repositories. We can choose from a variety of different board types to organize tasks.

We encourage you to try these out if you want to incorporate project management into your GitHub experience!
