# Git Learning Log

## 1. Merge Conflict

I deliberately created a merge conflict by editing the same line of a file in two different branches.

Git showed conflict markers:

<<<<<<<
=======
>>>>>>>

I resolved the conflict by choosing the correct content, removing the conflict markers, then staging and committing the resolved file.

## 2. Three Git Commands I Found Confusing

### git status
I learned that `git status` shows the current state of my working directory, including modified, staged, and untracked files.

### git add
I learned that `git add` moves changes from the working directory to the staging area so they can be included in the next commit.

### git merge
I learned that `git merge` combines the changes from another branch into the branch I am currently on.

## 3. A Git Mistake I Made

One mistake I made was typing a Git command incorrectly, which caused Git to show an error.

I checked the error message, corrected the command, and ran it again successfully. This taught me to read Git's messages instead of panicking when something goes wrong.
i also accidently made a folder with wrong crdentials , afterwards i learned how to delete it and make a new one instead of starting from start.