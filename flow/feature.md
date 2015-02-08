#New Feature

* Develop new features for upcoming releases
* Typically exist **in local developers repos only**

## Commands

#### Open and switch to a new feature branch

Development of new features starting from the 'develop' branch.

    $ git checkout -b feature-the-name-to-my-feature develop

You should see that you are in new feature branch

    $ git branch -av

    // You should see something like this, '*' mark your current branch
    develop     87ee184 Initial commit
    * feature-the-name-to-my-feature 87ee184 Initial commit
    master      87ee184 Initial commit

#### Work in this branch

You should work now in your branch do the changes and commits that you need

    $ git add .
    $ git commit -m 'this is an example'

Frecuenly ( 2 o more times at day... ) you need pull the others developers changes in remote branche develope to our new feature branch

	$ git pull --rebase origin develop

#### Option 1: Merge the commits in feature branch to develop branche

Firts you need switch to banche when you need merge the commits feature branche, in this case, develop

    $ git checkout develop

Now, you merge the feature branch commits in develop

    $ git merge --no-ff feature-the-name-to-my-feature

#### Option 2: Rebase your feature branch commits to develope

if I want rebase the feature branch commits to develop branch, I need are in feature branch

    $ git checkout feature-the-name-to-my-feature

Now, I can rebase my feature commits to develope branch

    $ git rebase develop

#### Merge or rebase conflicts

- **importan!** in this situation, if you have conflicts, git need that you resolve this. You can run your mergetool to resolve conflicts

        $ git mergetool

-  If you have resolve conflicts you can continue the pull --rebase with

	    $ git rebase --continue

If you have some files with conflicts , a and b points, git repeats the process by each file

####  Push your develop branch with all the feature branch commits integrated

When the merge is finish you can push the changes to develop remote branch

First I pull for new changes in remote develop branche tha any developer can put in my local merge time

    $ git pull -u origin develop

And push

    $ git push -u origin develop

