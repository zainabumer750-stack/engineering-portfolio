# Week 01 Practice Answers

## Part A — Terminal Basics

### 1. What command shows your current directory?

`pwd`

### 2. What command lists the contents of the current directory?

`ls`

### 3. What command moves you up one directory?

`cd ..`

### 4. Create a folder called `practice`, move into it, and create a file called `test.py`.

    mkdir practice
    cd practice
    touch test.py

### 5. What is the difference between `cd folder` and `cd /folder`?

`cd folder` moves into a folder relative to your current location.

`cd /folder` starts from the root directory and looks for the folder there.

### 6. How would you run a Python file called `main.py`?

`python main.py`

## Part B — Git Concepts

### 7. What problem does Git solve?

Git keeps track of changes made to files and projects. It allows developers to save different versions of their work and return to earlier versions when needed.

### 8. What are the three main areas in Git, and how does a file move between them?

The three main areas are the working directory, staging area, and repository. Changes move from the working directory to the staging area with `git add`, and from the staging area to the repository with `git commit`.

### 9. What is the difference between `git add` and `git commit`?

`git add` puts changes into the staging area. `git commit` saves the staged changes into the Git history.

### 10. What is the difference between `git fetch` and `git pull`?

`git fetch` downloads changes from a remote repository without applying them to the current branch. `git pull` downloads the changes and integrates them into the current branch.

### 11. What is a remote repository, and what is `origin`?

A remote repository is a copy of a Git repository stored somewhere else, such as GitHub. `origin` is the default name commonly used for the remote repository.

### 12. What does `git status` show?

`git status` shows the current branch and the state of files, such as modified, staged, untracked, or unchanged files.

### 13. What is the difference between Git and GitHub?

Git is a version control system used to track changes in a project. GitHub is an online platform used to host Git repositories and collaborate with others.

## Part C — Git Commands

### 14. Write the full sequence of commands to create a new project, initialize Git, create a file, commit it, connect it to a new GitHub repository, and push it.

    mkdir my-project
    cd my-project
    git init
    touch README.md
    git add README.md
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/USERNAME/my-project.git
    git push -u origin main

### 15. You accidentally staged a file and want to unstage it but keep your changes. What command do you use?

`git restore --staged filename`

### 16. What command shows your last 5 commits in compact form?

`git log -5 --oneline`

### 17. Create and switch to a new branch called `add-login` in one command.

`git switch -c add-login`

### 18. You finished your work on `add-login`. Write the commands to switch to `main` and merge the branch.

    git switch main
    git merge add-login

### 19. What is the difference between `git diff` and `git status`?

`git status` gives a summary of the current state of the working directory and staging area. `git diff` shows the actual line-by-line changes.

### 20. You try to push but Git says the remote branch has changes you do not have. What should you do?

First, get the latest changes from the remote repository using `git pull`. After resolving any conflicts if necessary, push the changes again using `git push`.

## Part D — Practical Git Situations

### 21. You accidentally committed a `.env` file containing a database password and pushed it to a public GitHub repository. What should you do and why is deleting it in a new commit not enough?

I should immediately change or revoke the exposed password because it should be treated as compromised. I should remove the `.env` file, add `.env` to `.gitignore`, and remove the secret from Git history because deleting it in a new commit does not remove the old commit containing the password.

### 22. What is a Git merge conflict and how do you resolve one?

A merge conflict happens when Git cannot automatically combine changes from different branches. I should open the conflicted file, choose the correct final content, remove the conflict markers, then stage and commit the resolved file.

    git add filename
    git commit -m "Resolve merge conflict"

### 23. Explain what each of these `.gitignore` lines does.

`__pycache__/` — Ignores Python cache folders.

`*.pyc` — Ignores Python compiled bytecode files.

`venv/` — Ignores Python virtual environment folders.

`.env` — Ignores environment files that may contain private information such as passwords or API keys.

`.vscode/` — Ignores VS Code-specific project settings.

### 24. What does `git push --force` do, and why can it be dangerous?

`git push --force` overwrites the remote branch history with the local branch history. It can remove commits that other people have pushed, so it can be dangerous on shared branches.

### 25. Write a `.gitignore` for a Python project that also ignores `node_modules`, `dist`, and SQLite database files.

    __pycache__/
    *.pyc
    venv/
    .env
    .vscode/
    node_modules/
    dist/
    *.db
    *.sqlite
    *.sqlite3

## Part E — Markdown

### 26. Write Markdown for an H2 heading, a 3-item bullet list, a bold word, a link, and a Python code block.

    ## My Heading

    - Item 1
    - Item 2
    - Item 3

    **Bold word**

    [Open GitHub](https://github.com/)

    ```python
    print("Hello, World!")
    ```

### 27. Create a Markdown table with columns `Command` and `Purpose`, and include two rows.

    | Command | Purpose |
    |---|---|
    | git status | Shows the current Git status |
    | git add | Stages changes for a commit |

## Part F — Reflection

### 28. What was the most confusing thing for you?

The most confusing thing was understanding the difference between the working directory, staging area, commits, and the remote repository. I also found Git remote errors confusing at first.

### 29. What is one thing you understand now that you did not understand on Monday?

I now understand that a Git branch is a separate line of work and that it can be merged into the main branch after completing the changes. I also understand that Git tracks changes locally while GitHub hosts the remote repository.

### 30. Which concept do you still not fully understand?

I still want to practice the staging area and the different ways Git moves changes between the working directory, staging area, commits, and the remote repository.