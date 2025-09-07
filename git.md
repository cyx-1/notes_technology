# Git

## Use file system to create a **remote git repository**
- https://thehorrors.org.uk/snippets/git-local-filesystem-remotes/
- In the directory to create the remote git repo
  - git init --bare myrepo.git
- In the directory where local git repo should reside (add quotes as needed)
  - git clone /path/to/repos/myrepo.git

## use interactive rebase to consolidate multiple commits
- rebase -i HEAD~2
- pick the first commit, squash second commit and then wq!
- consolidate the commit msgs
- git push -f
- in case if another person has already fetched commits prior to consolidation, use git rh to go back to a common commit and the git p 


[worktree](https://grok.com/share/bGVnYWN5_16be80be-007e-4516-9dc6-b55e7d58798e) 

Back to [index](index.md)