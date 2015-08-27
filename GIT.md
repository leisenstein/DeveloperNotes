GIT Commands
========

Workflow
There are many ways to start a GitHub project, but this is the way I've been doing it.  I'm a complete newb at this, so a lot of this information is probably wrong.  I'll update this as I gain more experience.

```sh
UPDATE: For Visual Studio Solutions, add and sync the .gitignore file BEFORE creating/adding the project and solution files.  This will ensure the files that should be ignored won't get added to the repository before the .gitignore file is in place.  If these files (DLL, Bin, Obj, EXE, etc.) are added before the .gitignore file is in place, they will need to be manually removed from the repo.
```

First, I create a Repo on GitHub.  Let's call is project-name

I open a command prompt and go to the directory on my computer where the project exists.
I type the command below to create the repo on my local computer.
```sh
git init
```


I check the status of the repo on my local computer.  It's newly created, so nothing is being tracked or committed.
```sh
git status
```

I add everything to my local repo so it is being tracked.  This is called the Staging area.
It is now being tracked, but has not been committed to my local repo.
```sh
git add .
```

I commit the changes to my local repo.
Now, there are no more un-committed changes.  
```sh
git commit -m "Committing to the local repo"
```


Now, I pull the repo from the project I created to get them in sync.
```sh
git pull https://github.com/leisenstein/project-name
```

On the remote server, I add my changes to that repo.  The changes are now staged, but not committed.
```sh
git remote add origin https://github.com/leisenstein/project-name.git
```

Now, I push the changes from my local repo to the master branch of the remote repo.
```sh
git push -u origin master
```

Now, I do a pull to make sure everything is in sync.
```sh
git pull origin master
```


- workspace is your local directory
- index is your local "staging area". You add/remove files to your staging area.
- local repository is a subdirectory named .git that contains all your neccessary repository files. files are committed to the local repo, from your workspace. 
- upstream repository is a version of your project hosted on a remote server ensuring all your changes are available to other developers. The default is "origin", a typical branch is "master"
- pull from an upstream repo fetches changes and merges them into the current branch
- clone downloads a repo from an upstream server and check the HEAD of the master branch
- master is the default branch for a newly created local repo
- origin the name of your repo that you create on github

----

To RollBack Uncommitted Changes
```sh
# Revert changes to modified files.
git reset --hard

# Remove all untracked files and directories.
git clean -fd
```
