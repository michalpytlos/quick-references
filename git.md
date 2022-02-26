# Git - quick reference

## Selected commands
| git command | description | more info |
| ------------| ----------- | --------- |
|blame <file\>|Show what revision and author last modified each line of file|[atlassian.com](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-blame)|
|branch|List, create or delete branches|[atlassian.com](https://www.atlassian.com/git/tutorials/using-branches)|
|checkout|Switch branches or restore working tree files|git help|
|cherry-pick <commit1\> <commit2\>|Pick commits and append to HEAD|git help|
|config|Get or set Git configuration values|[atlassian.com](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)|
|describe <commit\>|Find most recent tag that is reachable from commit|git help|
|log|Show commit logs|[atlassian.com](https://www.atlassian.com/git/tutorials/git-log#filtering-the-commit-history)|
|merge <branch\>|Merge branch into current branch|[atlassian.com](https://www.atlassian.com/git/tutorials/using-branches/git-merge)|
|mergetool|Run merge conflict resolution tools to resolve merge conflicts|[git-scm.com](https://git-scm.com/docs/git-mergetool)|
|rebase <new_base> [<branch\>]|Change base of branch from one commit to another|[atlassian.com](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)|
|reflog|Manage information recorded in reference logs|[git-scm.com](https://git-scm.com/docs/git-reflog)|
|reset <older_commit\>|Move branch head backwards in time to older commit|[atlassian.com](https://www.atlassian.com/git/tutorials/undoing-changes/git-reset)|
|restore|Unstage or discard uncommitted local changes|[git-scm](https://git-scm.com/docs/git#_reset_restore_and_revert), [git-tower](https://www.git-tower.com/learn/git/commands/git-restore)|
|revert <bad_commit\>|Invert changes introduced by commit and append new commit with resulting inverse content|git help|
|stash| Save local modifications away and revert working directory to match HEAD commit|[atlassian.com](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)|
|tag <tag_name\> <commit\>|Add tag to commit|git help|


## Useful command options
| git command | description |
| ------------| ----------- |
|blame -L n,m <file\>|Show what revision and author last modified lines n to m of file|
|branch -f <branch\> <commit\>|Move branch head to commit|
|branch --merged [<commit\>]|List branches whose tips are reachable from commit|
|checkout -- <file\>|Discard unstaged changes to file|
|checkout -b <new_branch\> |Create new branch AND check it out|
|commit --amend --reset-author --no-edit||
|diff --stat <commit1\> <commit2\>|Show which files changed between commits (in diffstat form)|
|push <remote\> <source\>:<destination\>|Precisely define what and where to push using refspec|
|push <remote\> :<remote_branch\>|Delete branch on remote using refspec with empty source|
|stash show -p <stash_ref\>|Show changes recorded in stash entry in patch form|


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
1. [Git refs](https://www.atlassian.com/git/tutorials/refs-and-the-reflog)
1. [Git for ages 4 and up - video](https://www.youtube.com/watch?v=1ffBJ4sVUb4)
2. [Pro Git - book](https://www.git-scm.com/book/en/v2)
