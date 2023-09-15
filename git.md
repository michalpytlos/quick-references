# Git - quick reference

## Contents
- [Commands](#commands)
- [Config](#config)
- [Useful links](#useful-links)

## Commands
| Command | description | usage |
| ------------| ----------- | --------- |
|[blame](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-blame)|Show what revision and author last modified each line of file|`git blame FILE`|
||Show what revision and author last modified lines n to m of file|`git blame -L n,m FILE`|
|[branch](https://www.atlassian.com/git/tutorials/using-branches)|List, create or delete branches||
||Move branch head to commit|`git branch -f BRANCH COMMIT`|
||List branches whose tips are reachable from commit|`git branch --merged [COMMIT]`|
|checkout|Switch branches or restore working tree files||
||Get FILE from BRANCH|`git checkout BRANCH -- FILE`|
||Discard unstaged changes to file|`git checkout -- FILE`|
||Create new branch AND check it out|`git checkout -b NEW_BRANCH`|
|cherry-pick|Pick commits and append to HEAD|`git cherry-pick COMMIT [COMMIT...]`|
|[commit](https://www.atlassian.com/git/tutorials/saving-changes/git-commit)|Commit staged changes||
||Modify the last commit without changing the message|`--amend --no-edit`|
||Modify the last commit and declare that the authorship of the commit now belongs to the comitter|`--amend --reset-author`|
|describe|Find most recent tag that is reachable from commit|`git describe [COMMIT...]`|
|[diff](https://www.atlassian.com/git/tutorials/saving-changes/git-diff)|Run diff on commits, branches, files and more||
||Show which files changed between commits (in diffstat form)|`git diff --stat COMMIT_1 COMMIT_2`|
|[log](https://www.atlassian.com/git/tutorials/git-log#filtering-the-commit-history)|Show commit logs||
||List files modified in last NUM days|`git log --since="NUM day ago" --pretty="" --name-only \| sort -u`|
|[merge](https://www.atlassian.com/git/tutorials/using-branches/git-merge)|Merge branch into current branch|`git merge BRANCH`|
|[mergetool](https://git-scm.com/docs/git-mergetool)|Run merge conflict resolution tools to resolve merge conflicts|
|[push](https://www.atlassian.com/git/tutorials/syncing/git-push)|Upload local repo content to remote repo||
||Precisely define what and where to push using refspec|`git push REMOTE SOURCE:DESTINATION`|
||Delete REF from remote. REF can be a branch or a tag.|`git push REMOTE -d REF`|
||Delete TAG from remote. Use this version if there is a branch with the same name.|`git push REMOTE -d refs/tags/TAG`|
|[rebase](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)|Change base of branch from one commit to another|`git rebase NEW_BASE [BRANCH]`|
|[reflog](https://git-scm.com/docs/git-reflog)|Manage information recorded in reference logs||
|[reset](https://www.atlassian.com/git/tutorials/undoing-changes/git-reset)|Move branch head backwards in time to older commit|`git reset OLDER_COMMIT`|
|[restore](https://www.git-tower.com/learn/git/commands/git-restore)|Unstage or discard uncommitted local changes||
|revert|Invert changes introduced by commit and append new commit with resulting inverse content|`git revert BAD_COMMIT`|
|[show](https://www.atlassian.com/git/tutorials/git-show)|View expanded details on git objects||
||List files affected by commit together with their status|`git show --pretty="" --name-status COMMIT`|
|[stash](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)| Save local modifications away and revert working directory to match HEAD commit||
||Show changes recorded in stash entry in patch form|`git stash show -p STASH_REF`|
|tag|Add tag to commit|`git tag TAG_NAME COMMIT`|

## Config
| Command | description | usage |
| ------------| ----------- | --------- |
|[config](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)|Get or set Git configuration values||
||Show all variables in config file |`--list`|q
||Set variable in config file |`git config VARIABLE "VALUE"`|
||Disable paging for `git branch`|`config --global pager.branch false`|

## Useful links
### Command refs
1. [atlassian.com](https://www.atlassian.com/git)
2. [ndpsoftware.com](https://ndpsoftware.com/git-cheatsheet.html)
3. [git-scm](https://git-scm.com/docs)
4. [learn x in y minutes](https://learnxinyminutes.com/docs/git/)
5. [How to read command synopsis](https://github.com/git/git/blob/master/Documentation/CodingGuidelines) (section *Writing documentation*)
6. [How to undo (almost) anything with Git](https://github.blog/2015-06-08-how-to-undo-almost-anything-with-git/)

### Tools
1. [Meld](https://meldmerge.org/) + [how to set it up](https://stackoverflow.com/questions/34119866/setting-up-and-using-meld-as-your-git-difftool-and-mergetool)

### Tutorials
1. [Learn Git Branching](https://learngitbranching.js.org/)
2. [Git Immersion](https://gitimmersion.com/lab_01.html)

### How git works
1. [Git refs and the reflog](https://www.atlassian.com/git/tutorials/refs-and-the-reflog)
1. [Git for ages 4 and up - video](https://www.youtube.com/watch?v=1ffBJ4sVUb4)
2. [Pro Git - book](https://www.git-scm.com/book/en/v2)
