
# DIO | Summary Git and GitHub

A place to store a brief overview of Git and GitHub from the course "Code Version Control with Git and GitHub" - [Digital Innovation One](https://www.dio.me/).

## 📚 Documentation
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Documentation](https://docs.github.com/)

## 💻 Class Summary

### Directory commands
- Access a local directory
```
cd dir_name
```
- Exit the current directory
```
cd ..
```
### Git init
A command to create a git repository in a local directory.
```
git init
```
### Git clone
A command for downloading existing source code from a remote repository
```
git clone <https://name-of-the-repository-link>
```
### Git branch
A command for creating, listing and deleting branches.
- Creating a new branch
```
git branch <branch-name>
```
- Viewing branches
```
git branch
or
git branch --list
```
- Deleting a branch
```
git branch -d <branch_name>
```
### Git status
A command to get all the necessary information about the current branch.
```
git status
```
### Git add
A command for createing, modifying or deleting a file, these changes will happen in local.  Use the git add command to include the changes of a file(s) into the next commit. 
```
git add <file>
or
git add -A (add all files)
```
Important: The git add command doesn't change the repository and the changes are not saved until we use git commit.
### Git commit
A command for saving the changes locally. 
```
git commit -m "commit message"
```
### Git push
A command for sending the changes to the remote repository, after commiting the changes.
```
git push <remote> <branch-name>
``` 
For newly created branches
```
git push -u origin <branch-name>
```
### Git pull
A command for getting updates from the remote repository. (git fetch + git merge)
```
git pull <remote>
```
### Git revert
A commandfor undoing the changes that were made. The commit history remains untouched. 
- First, get the hash code in the commit history
```
git log --oneline
```
- Use the command specifying the hash code
```
git revert <hash-code>
```
- Press shift+q to exit the screen.
### Git merge
A command for integrating the feature branch with all of its commits back to the dev/master branch.
- Access the specific branch that will be merged with the feature branch.
```
git checkout master
```
- Upate the local master branch
```
git fetch
```
- Merge the feature branch into master/dev
```
git merge <branch-name>
```
### Git checkout
A command for switching from one branch to another.
```
git checkout <name-of-the-branch>
```
A command for creating and switching a branch at the same time
```
git checkout -b <name-of-the-branch>
```
Important:
- The changes in the current branch must be committed or stashed before switching.
- The branch should exist in the local.
### Git restore
A command for discarding changes in working directory.
```
git restore <file>
```
### .gitignore
- A command for writing into the .gitignore file.
```
echo <directory-name>/ > .gitignore
```
- A command for appending into the .gitignore file.
```
echo <directory-name>/ >> .gitignore
```
- A command for removing the directory from the .gitignore file.
```
echo > .gitignore
```
### Removing Git repository
A command for removing initialized Git repository in local
```
rm -rf .git
```
### Modifying commit message
A command for modifying the message from the last commit.
```
git commit --amend -m "message"
```
### Restoring commit
A command for restoring a previous version of commits.
- Soft: Files are rolled back to staged. Ready to be commited.
```
git reset --soft <hash-code>
```
- Mixed (default): Files are rolled back to untracked/unstaged. Necessary to use git add to include in  what will be commited.
```
git reset --mixed <hash-code>
or
git reset
```
- Hard: Fles are removed completely.
```
git reset --hard <hash-code>
```
### Removing a file
A command for removing a file.
```
git reset <file>
```
### Unstaging a file
A command for unstaging a file.
```
git restore --staged <file>
```
### Adding a remote repository
A command for adding a remote repository in Git.
```
git remote add <name> <URL>
```
