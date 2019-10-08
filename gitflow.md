# Gitflow Workflow

Gitflow Workflow is a design that was first published and made popular by Vincent Driessen at nvie.The Gitflow Workflow
defines a strict branching model designed around the project release.This provides a robust framework for managing larger
projects.Gitflow is ideally suited for projects that have a scheduled release cycle. This workflow doesn’t add any new 
concepts or commands beyond what’s required for the Feature Branch Workflow. Instead, it assigns very specific roles to 
different branches and defines how and when they should interact. In addition to feature branches, it uses individual 
branches for preparing, maintaining, and recording releases. Of course, you also get to leverage all the benefits of the
Feature Branch Workflow: pull requests, isolated experiments, and more efficient collaboration.

## How it works

This workflow uses two branches to record the history of the project. The master branch stores the official release 
history, and the develop branch serves as an integration branch for features. It's also convenient to tag all commits 
in the master branch with a version number.A simple way to do this is for one developer to create an empty develop 
branch locally and push it to the server.This branch will contain the complete history of the project, whereas master 
will contain an abridged version. Other developers should now clone the central repository and create a tracking branch for
develop.When using the git-flow extension library, executing git flow init on an existing repo will create the develop 
branch