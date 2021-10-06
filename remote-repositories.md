# Remote Repositories

When collaborating on Git projects, you must interact with remote repositories.
You also can work with multiple repositories, which you can have only read/write or read-only privileges. 
Teams also can use remote repositories to push information into and pull data from.

## Cloned Repositories

For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.

## Seeing Your Remotes

When running the git remote command, you will view the short names, such as “origin,” of all specified remote handles.

Using git **remote -v**, you can view all the remote URLs next to their corresponding short names.

**$ cd example**

**$ git remote -v**

remote1 https://github.com/remote1/example (fetch)

remote1 https://github.com/remote1/example (push)

remote2 https://github.com/remote2/example (fetch)

remote2 https://github.com/remote2/example (push)

remote3 https://github.com/remote3/example (fetch)

remote3 https://github.com/remote3/example (push)

## Adding Remotes

Create a new remote Git repository with a short name, use this following format:

**git remote add shortname url**

Examples:

- $ git remote**

origin

- $ git remote add js https://github.com/janesmith/project1

- $ git remote -v

- origin https://github.com/johndoe/project1 (fetch)

- origin https://github.com/johndoe/project1 (push)

- js     https://github.com/janesmith/project1 (fetch)

- js     https://github.com/janesmith/project1 (push)

These remote and short names allows you to use shortnames for Git collaboration.

## Fetching

Fetching is pulling data that you don’t have from a remote project.

The command for format:

**git fetch [remote-name]**

*Now, you should also possess the references to all branches for that remote (more on branching later).

Cloned Repositories

For cloned repositories, use the command git fetch origin to pull down any new changes that were pushed to the server since you cloned or last fetched from it.

*Note:* git fetch solely pulls new data to a local repository; it does not merge changes with or modify your local work. We will discuss merging in a later section. Later, we will also discuss git pull , which allows for fetching and automatic merging.

Webpage:[Git Tutorial: A Comprehensive Guide](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/)

