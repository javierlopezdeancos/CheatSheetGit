
<img src="images/anoluke.png" width="100px"> 

#Git Cheatsheet

"...How many anosluke you need for feel the force..."


## Basic commands

### Create

##### Git init

	$ git init
	
### Link

#####  Add to remote repository

This command takes a remote name and a repository URL

    $ git remote add origin https://github.com/try-git/try_git.git

##### Adding Files with change status to Stage

To tell Git to start tracking changes made to <file.extension>, we first need to add it to the staging area by using git add.

    $ git add .
    $ git add <file.extension>    
    $ git add '*.txt'
    
##### Remove Files of Stage, resetting the Stage

You can unstage files by using the git reset command

	$ git diff --staged
    
##### Remove file to tree directori

    $ git rm <file.extension>    
    $ git rm '*.txt'     
    
** importan! ** this command remove file to the working tree

##### Committing

To store our staged changes we run the commit command with a message describing what we've changed. 

    $ git commit -m "Commit example file to can push" 
    
##### Checking for changes or status

Good job! Git is now tracking our octocat.txt file. Let's run git status again to see where we stand.

    $ git status 
    
##### History

So we've made a few commits. Now let's browse them to see what we changed.

Fortunately for us, there's git log. Think of Git's log as a journal that remembers all the changes we've committed so far, in the order we committed them.

    $ git log   


##### Push the changes to remote repository

The push command tells Git where to put our commits when we're ready, and boy we're ready.

The name of our remote is origin and the default local branch name is master. The -u tells Git to remember the parameters, so that next time we can simply run git push and Git will know what to do.

    $ git push -u origin <branch>
    
##### Update remote repository changes

We can check for changes on our Git repository and pull down any new changes.
The -u tells Git to remember the parameters, so that next time we can simply run git pull and Git will know what to do.

    $ git pull -u origin <branch>  
    
### Branch
    
##### Switching branch

When developers are working on a feature or bug they'll often create a copy (aka. branch) of their code they can make separate commits to. Then when they're done they can merge this branch back into their main master branch.

	$ git branch <branche>
	
##### Create and switch to new branch

You can create and switch to new branche

	$ git checkout -b <branche>
	
##### List branch

You can list the branch in your repository with.

	$ git branch 
	$ git branch -av	
		
##### Merge Branch

When you have to merge your changes from the **<branch-B>** into the **<branch-A>**.

1. Go to **<branch-A>**
	
       $ git checkout <branche-A>
	
2. Merge **<branche-B>** in my current branch

	   $ git git merge --no-ff <branche-B>

##### Delete branch

You can list the branch in your repository with.

	$ git branch -d <branche>
 
### Revert        

##### Undo the state of file to last commit state

Files can be changed back to how they were at the last commit by using the command: git checkout -- <target>

	$ git checkout -- <target>
	$ git checkout -- name.ext    
    
##### What is diferent to the last commit?

Take a look at what is different from our last commit by using the git diff command.
In this case we want the diff of our most recent commit, which we can refer to using the HEAD pointer.
    
    $ git diff HEAD
    
##### Staged Differences (cont'd)

Good, now go ahead and run git diff with the --staged option to see the changes you just staged. 

    $ git diff --staged    

    
## Git flow

### New feature

[What happend if I need to do a new feature in the code?](flow/feature.md)

## Git Reference

### Documentation
[http://rogerdudler.github.io/git-guide/](http://rogerdudler.github.io/git-guide/)

### Tutorials
[http://gitimmersion.com/](http://gitimmersion.com/)


	
	
