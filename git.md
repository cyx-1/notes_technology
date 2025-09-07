# Git

## Setting up your Git identity 
- The following commands sets the correct name to be shown properly in your future commits: 
```
git config –global user.name "Your Name" 
git config –global user.email "your.email@example.com"
```

## Setting up local repository given a GitHub repo, and .gitignore 
- The following command would replicate a GitHub repository into your local Git repository. The name of the GitHub project becomes the name of the new folder containing the project content: ```git clone <repository>```
- Keep in mind that git is great for text artifacts, not great for frequently changing binary artifacts. 
- You could use the .gitignore file to exclude folders and files of certain convention from going into git repository

## Review who did what when in a repository 

## Retrieve latest changes from remote repository 
- The command to use here is: git fetch It makes your local repository aware of all the changes that took place on the remote git repository, while not impacting the changes that you have been making in working area and staging area

## Checking on status of modified files 
- git status Tell you which change you have made that have not been committed yet

## Updating local branch to catch up to the latest 
- The command to use here is: ```git pull``` It makes your local branch catch up to the latest changes in the corresponding remote branch

## Publish changes for codebase cloned from GitHub 
- After setting up a new repository via Clone, the following steps would put your changes into the remote git repository on GitHub: 1) put new or modified files into the staging area 2) commit changes in staging area into a branch on local repository 3) push the changes in local branch into the remote branch. 

## Publish changes from a new project folder not cloned from GitHub
- Sometimes you want to create a folder, work on the project content and then connect it to a remote project on GitHub. The steps to follow here is similar to the previous section with two minor difference: 1) the folder gets set up with git init, and 2) a remote repository name(origin) need to be added to the local git project: ```git remote add origin <repository url>```

## Working with branches 
- Each branches in Git is a pointer to a commit. When committing new changes to a branch, the branch pointer updates to the latest commit. Local branch typically follows a remote branch of the same name. See illustration below on how to list branches, switch to a different branch, create a new branch, and delete branch

## Perform diff in Git
- Although Git comes with a diff tool by default, it is better to use a visual compare tool to spot the differences more easily. 
- Recommendation here is to use Beyond Compare to work with Git

## Merge changes within Git 
- A Git merge combines changes from one branch into another, producing either a fast-forward merge (target moves its pointer forward without new commit) or a 3-way merge (Git creates a merge commit with two parents). Use the –no-ff option to create a 3-way merge even if fast-forward is possible. Use this command to initiate the merge: ```git merge <branch name>/commit hash``` if the merge requires conflict resolution, use this command to abort: ```git merge –abort```

## Reverting changes to correct a mistake
- Correcting mistakes in Git comes in multiple forms. Here are some examples: 1) revert changes made in working directory with content from local repository 2) move the changed file back into working directory because the move to staging area was premature 3) revert a recent commit in the local repository 4) revert a recent commit to the remote repository 5) consolidate multiple local commits into one and then push into remote repository Note: example 4 and 5 are rewriting history that may be already exposed to other team members. So use these technique only if truly required, and share a signal to inform this drastic action. Note: solutions for example 3 could also be useful to point the working directory to any commit

## Conduct code review via GitHub pull request 
- The PR process follows these steps: 1) implementor pushes code into branch 2) implementor create pull request for code review by specifying source and target branches 3) reviewer(s) provide comments on the PR and indicates whether a PR is ready to merge or needs more work 4) implementor updates the source branch with changes to address review comments and repeat step 3 until reaching green signal to merge 5) PR changes get merged into the target branch.

## Use Git alias to simplify usage 
- Many Git commands are too verbose to type, use these alias instead to abbreviate and consolidate commands. For example, the following command would fetch the latest from remote and also display the commit tree: git f As another example, the following command stages all changes (new, modified, deleted files) in the repository, commits the staged changes with a commit message, pushes the new commit(s) to the remote repository, and then shows a graphical commit history: git cmp "commit msg"

## Use file system to create a **remote git repository**
- https://thehorrors.org.uk/snippets/git-local-filesystem-remotes/
- In the directory to create the remote git repo
  - git init --bare myrepo.git
- In the directory where local git repo should reside (add quotes as needed)
  - git clone /path/to/repos/myrepo.git

## Use interactive rebase to consolidate multiple commits
- rebase -i HEAD~2
- pick the first commit, squash second commit and then wq!
- consolidate the commit msgs
- git push -f
- in case if another person has already fetched commits prior to consolidation, use git rh to go back to a common commit and the git p 


[worktree](https://grok.com/share/bGVnYWN5_16be80be-007e-4516-9dc6-b55e7d58798e) 

Back to [index](index.md)