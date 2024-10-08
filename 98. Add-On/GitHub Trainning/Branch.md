# Git branch #

Up to this point, you’ve practiced in a single Git branch. (Note: GitHub has changed the naming convention of the main branch from master to main.We will be updating the instructions and code workspaces soon to reflect that. In the meantime, master refers to main).

Git allows us to create branches to experiment with versions of a project. Imagine you want to create a version of a story with a happy ending. You can create a new branch and make the happy ending changes to that branch only. It will have no effect on the master branch until you’re ready to merge the happy ending to the master branch.

In this lesson, we’ll be using Git branching to develop multiple versions of a resumé. 

  `$git branch`

## Branching Overview ##

The diagram to the right illustrates branching.

   + The circles are commits, and together form the Git project’s commit history.
   + New Branch is a different version of the Git project. It contains commits from the main branch but also has commits that it does not have.

Right now, the Git project has only one branch: master.

To create a new branch, use:

 `git branch new_branch`

Here new_branch would be the name of the new branch you create, like photos or blurb. Be sure to name your branch something that describes the purpose of the branch. Also, branch names can’t contain whitespaces: new-branch and new_branch are valid branch names, but new branch is not.

The master and fencing branches are identical: they share the same exact commit history. You can switch to the new branch with

  `git checkout branch_name`

Here, branch_name is the name of the branch. If the branch’s name is "skill"

  `git checkout skill`

Once you switch branches, you will now be able to make commits on the branch that have no impact on "master". 

## Git merge ##

What if you wanted to include all the changes made to the fencing branch on the master branch? We can easily accomplish this by merging the branch into master with:

   `git merge branch_name `

For example, if I wanted to merge the skills branch to master, I would enter

   `git merge skills `

In a moment, you’ll merge branches. Keep in mind:

    Your goal is to update master with changes you made to fencing.
    fencing is the giver branch, since it provides the changes.
    master is the receiver branch, since it accepts those changes.

## Merge conflict ##

The merge was successful because master had not changed since we made a commit on fencing. Git knew to simply update master with changes on fencing.

What would happen if you made a commit on master before you merged the two branches? Furthermore, what if the commit you made on master altered the same exact text you worked on in fencing? 
When you switch back to master and ask Git to merge the two branches, Git doesn’t know which changes you want to keep. 
This is called a merge conflict.

Let’s say you decide you’d like to merge the changes from fencing into master.

Here’s where the trouble begins!

You’ve made commits on separate branches that alter the same line in conflicting ways. 
Now, when you try to merge fencing into master, Git will not know which version of the file to keep.

## Delete branch ##

In Git, branches are usually a means to an end. 
You create them to work on a new project feature, but the end goal is to merge that feature into the master branch. 
After the branch has been integrated into master, it has served its purpose and can be deleted.

The command

   `git branch -d branch_name `

will delete the specified branch from your Git project.

Now that master contains all the file changes that were in fencing, let’s delete fencing.

## Generalizations ##

Let’s take a moment to review the main concepts and commands from the lesson before moving on.

  + Git branching allows users to experiment with different versions of a project by checking out separate branches to work on.

The following commands are useful in the Git branch workflow.

  + `git branch`: Lists all a Git project’s branches.
  + `git branch branch_name`: Creates a new branch.
  + `git checkout branch_name`: Used to switch from one branch to another.
  + `git merge branch_name`: Used to join file changes from one branch to another.
  + `git branch -d branch_name`: Deletes the branch specified.

A remote is a Git repository that lives outside your Git project folder. Remotes can live on the web, on a shared network or even in a separate folder on your local computer.
The Git Collaborative Workflow are steps that enable smooth project development when multiple collaborators are working on the same Git project.
We also learned the following commands

  + `git clone`: Creates a local copy of a remote.
  + `git remote -v`: Lists a Git project’s remotes.
  + `git fetch`: Fetches work from the remote into the local copy.  
  + `git merge origin/master`: Merges origin/master into your local branch.
  + `git push origin <branch_name>`: Pushes a local branch to the origin remote.

Git projects are usually managed on Github, a website that hosts Git projects for millions of users. With Github you can access your projects from anywhere in the world by using the basic workflow you learned here.
