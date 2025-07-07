# Github-Basics
This file aims to rovide the basic info on how Github works, how to manage projects, commits, branches, and pull requests.

Before you even touch any of the git commands it is helpfull to understand how to navigate your devices terminal

### Git Clone
To even start with the basics the first command you will most probably use is `git clone <repo_url_here>`. It simply puts all of the files from the url given into the destination folder, if you are using a terminal you will want to make sure you are already in the folder you want the repository to end up in, if you are using an IDE such as Visual Studio Code, it may prompt you to select a destination folder.

### Git Checkout/Branch
To ensure you dont overwrite others work it is helpfull to make a new branch, this makes sure that the changes you make do not affect the main branch which should allways be maintained in a deployable state, `git branch <branch_name>` makes a new branch, but if you want to switch to an existing branch you can use `git checkout`. But if you would like to make a new branch and switch to it with one command you can use the `-b` flag with the command to do this, it should looks something like `git checkout -b <branch_name>`.

### Git Pull
This command will become second nature once you are compitent with the git commands, this command is commonly used after doing the inital `git clone` as its use case is to pull from the current repository and merges any changes that have been made, you should use `git pull` before starting any new work on a file. In our repositories, the `main` branch is protected, meaning if you wanted to update the `main` branch using `git pull <remote_name> <branch_name>` they would have to be authorised, this is to ensure that there are no bugs introduced or mistakes made.

### Git Status
`git status` is a great command to use, as it allows you to see where in the process you are, such as showing unstaged files, that you havent done `git add` to,  that have changes within them, you will also see staged files, these are ones that are ready for your next commit. It also will show you what branch you are on.

### Git Add
When wanting to upload work to the remote repository, and tell git to keep track of a file in its current state, you will use `git add <file_name>`. you can also do `git add .` to add all files in the current repository to the list.

### Git Commit
This command you will use mainly when you are wanting to apply changes that you have completed in a file on a given branch, `git commit` is usually followed by a `-m` flag, this simply allows you to write a small message describing what changes have been made, not using the `-m` flag should open up an editor allowing for more detailed descriptions of changes, which is helpfull when dealing with multiple files.

### Git Push
Before using this command you will want to make sure you you have used both `git add` and `git commit` with the relevant flags, as you want to make sure you have everything set before issuing a change, this will take into account the branch you have made and then upload the files to that branch, if you have made a local branch that does not exitst on the remote branch you would have to specifiy this when doing `git push -u <remote_name> <branch name>` as this allows for tracking, which can be benifical for other commands you use, in most cases the `<remote_name>` will be `origin`.