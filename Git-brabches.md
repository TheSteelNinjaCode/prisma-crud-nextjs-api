to get help with branches
`git help branch`

git always have one branch by default, called master branch

see the existing branches
`git branch`

create new branch
`git branch <branch-name>`

to get the location of the HEAD pointer
`cat .git/HEAD`

to list the directory of the .git folder
`ls .git/HEAD`

to switch to a branch
`git checkout <branch-name>`

to create a new branch and switch to it
`git checkout -b <branch-name>`

to delete a branch
`git branch -d <branch-name>`

to delete a branch forcefully
`git branch -D <branch-name>`

to merge a branch to the current branch
`git merge <branch-name>`

to merge a branch to the current branch with a message
`git merge <branch-name> -m "message"`

to merge a branch to the current branch with a message and without fast-forward
`git merge <branch-name> -m "message" --no-ff`

to merge a branch to the current branch with a message and without fast-forward and without commit
`git merge <branch-name> -m "message" --no-ff --no-commit`

to merge a branch to the current branch with a message and without fast-forward and without commit and without auto-merging
`git merge <branch-name> -m "message" --no-ff --no-commit --no-ff`

if you make changes then you want to change branches without committing the changes git will ask to commit or stash the changes

Switching with uncommitted changes

1. Cannot switch if changes in working directory conflict
2. Can switch if changes in working directory could be apply without conflict
3. Can switch if file are not been track
4. Commit the changes to the current branch before switching
5. If you don't want the changes remove them with -> `git checkout -- <file-name>`
6. Or stash (is like a pocket) them with -> `git stash`

Rename a branch
Note: Be careful renaming and sharing branches with others because it can cause conflicts and confusion is better to name before sharing
`git branch -m <old-branch-name> <new-branch-name>`

Delete Branch
Note: you cant be in the branch you want to delete, switch to another branch first then delete the branch
`git branch -d <branch-name>`

if you want to force delete a branch even if not marge
`git branch -D <branch-name>`

To know if branched is merged or not
`git branch --merged`

To know witch branches are not marge
`git branch --no-merged`

<!-- Reset Branches -->

There is 3 types of Reset:

1. Soft Reset
2. Mixed Reset
3. Hard Reset

The Soft reset:

1. move the head pointer
2. keep the changes in the staging area
3. keep the changes in the working directory
   `git reset --soft <commit-id>`

The Mixed reset:

1. move the head pointer
2. remove the changes from the staging area to match the repository
3. keep the changes in the working directory
   `git reset --mixed <commit-id>`

The Hard reset:

1. Move the Head pointer
2. Remove the changes from the staging area to match the repository
3. Remove the changes from the working directory to match the repository
   `git reset --hard <commit-id>`
