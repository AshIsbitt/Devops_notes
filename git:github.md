# Git and Github

This is a refresher of git and github commands

See [this video](https://www.youtube.com/watch?v=SWYqp7iY_Tc)

What is Git? - Version Control System for tracking changes in a directory created by Linus Torvolds. Note that knowledge of Bash is recommended.

- Snapshots of the directory with a Commit
- Easy to revert back

### Commands
- `git init` - creates the git repository with a .git folder
- `git add` will stage the files/folders specified to prepare for commiting.
- `git status` will show how many files have been changed, as well as everything "Added"
- `git rm` removes something from the staging area. `git rm --cached`
- `git commit` will commit your changes to the repo. Note that you need to include a commit message with this command. `git commit -m "commit message"`
- `git push` will push the local repo to a remote, IE github
- `git pull` is the reverse, pulling the latest changes from the remote repo to your local machine
- `git clone` will clone a github repo to your local machine
- `git --version` will show the version of Git you're using.

Installing is simple, and can be pulled through homebrew or from the main website.

`git config` will allow you to set up your username and email for github within your local git install. You can also set up SSH keys between git and github to circumvent this.

.gitignore is a page that has a list of other files not to push to the repo. `touch .gitignore` is the best way to create it in a terminal.

- `git branch name` is used to create a branch, which stems out from the master. You need to switch to the branch with `git checkout name`. 

Once the work a branch was split off for is compliete, `git merge name` will merge it back to master. You will need to include a commit message.

- `git remote` will show you the remote repos linked to your repo.

