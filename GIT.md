GIT Commands
========

Workflow
There are many ways to start a GitHub project, but this is the way I've been doing it.  I'm a complete newb at this, so a lot of this information is probably wrong.  I'll update this as I gain more experience.


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


- master is the default branch for a newly created repo
- origin is your repo
- git have me errors when I tried to commit to a repo with a "." in it's name.