# Git - quick reference

## Selected commands

| git command | description | more info |
| ------------| ----------- | --------- |
|checkout -b <new_branch\> |Create new branch AND check it out|git help|
|checkout -b <new_branch\> <remote\>/<branch\>|Create new branch AND set remote tracking AND check it out|git help|
|checkout -- <file\>|Discard unstaged changes to file|git help|
|branch -f <branch\> <commit\>|Move branch head to commit|git help|
|reset <older_commit\>|Move branch head backwards in time to older commit|[atlassian.com](https://www.atlassian.com/git/tutorials/undoing-changes/git-reset)|
|revert <bad_commit\>|Invert changes introduced by commit and append new commit with resulting inverse content|git help|
|merge <branch\>|Merge branch into current branch|[atlassian.com](https://www.atlassian.com/git/tutorials/using-branches/git-merge)|
|cherry-pick <commit1\> <commit2\>|Pick commits and append to HEAD|git help|
|rebase <new_base> [<branch\>]|Change base of branch from one commit to another|[atlassian.com](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)|
|push <remote\> <source\>:<destination\>|Precisely define what and where to push using refspec|git help|
|push <remote\> :<remote_branch\>|Delete branch on remote using refspec with empty source|git help|
|tag <tag_name\> <commit\>|Add tag to commit|git help|
|describe <commit\>|Find most recent tag that is reachable from commit|git help|
|reflog|Track when Git refs were updated in local repository|[atlassian.com](https://www.atlassian.com/git/tutorials/rewriting-history/git-reflog)|
|stash| Save local modifications away and revert working directory to match HEAD commit|[atlassian.com](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)|
|blame -L n,m <file\>|Show what revision and author last modified lines n to m of file|[atlassian.com](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-blame)|
|config|Get or set Git configuration values|[atlassian.com](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config)|


## Useful links
### Command refs
1. [atlassian.com](https://www.atlassian.com/git)
2. [ndpsoftware.com](https://ndpsoftware.com/git-cheatsheet.html)
3. [git-scm](https://git-scm.com/docs)
4. [learn x in y minutes](https://learnxinyminutes.com/docs/git/)
5. [How to read command synopsis](https://github.com/git/git/blob/master/Documentation/CodingGuidelines) (section *Writing documentation*)

### Tools
1. [Meld](https://meldmerge.org/) + [how to set it up](https://stackoverflow.com/questions/34119866/setting-up-and-using-meld-as-your-git-difftool-and-mergetool)

### Tutorials
1. [Learn Git Branching](https://learngitbranching.js.org/)
2. [Git Immersion](https://gitimmersion.com/lab_01.html)

### How git works
1. [Git for ages 4 and up - video](https://www.youtube.com/watch?v=1ffBJ4sVUb4)
2. [Pro Git - book](https://www.git-scm.com/book/en/v2)
