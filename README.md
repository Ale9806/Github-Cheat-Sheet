# Git-Cheat-Sheet
### Git phases:
<ol>
  <li> <b>Working Tree:</b> Area where you perform all the modifications (contains Track and untrack files)</li>
  <li> <b>Staging area :</b> Contains all of the information about what files and changes are goingt to be commited next </li>
  <li> <b>Git directory:</b> History of all track files and changes </li>
</ol>
<ul>
  <li>Tracked files are files from are working tree that were passed to the Staging areas</li>
  <li>Untracked files are files that remain at our working tree</li>
</ul>

### CONFIGURATION COMMANDS : 

| Command | Description |
| --- | --- |
| `git --help` | Display all available commands|
| `git config --global user.name "Name"`   | Set Name|
| `git config --global user.email "Email"`   |Set Email|
| `git config -l   ` | Check current configuration|
| `git remote -v `   | Check  current orign|
| `git remote show origin`   | Check more information of orign|

### BASIC COMMANDS:
| Command | Description |
| --- | --- |
| `git init ` | Create .git directory (Initialize Repository)|
| `git status `   |  Check status of repository|
| `git add`   |Add file from working tree to staging area|
| `git rm ` | Remove file from staging area (Remember to commit afterwards) |
|`git rm -cached [name of file]`| Untrack files from previous commit |
| `git mv `   | Move ore rename file|
| `.gitignore `   | Add files to be ingored|
| `git commit `   | Commit changes|
| `git commit -a -m`   | git add + git commit at the same time|
 * `git commit -a -m`  only works with tracked files
 
 ### REVIEW COMMANDS: 
 | Command | Description |
| --- | --- |
| `git diff` |Prints difference between older an newer version of a staged file|
| `git log `   |Show log of commits|
| `git show hashvlaue`   |Show code in the commit|
| `git blame file   ` | Show who made changes |

### UNDO COMMANDS: 

 | Command | Description |
| --- | --- |
| `git checkout ` |Undo changes (new file has to be unstage)|
| `git reset`   |Unstage changes (-p to select what to unstage)|
| `git commit -ammend`   |Undo a commit ( AVOID AMMENDING COMMITS THAT HAVE ALREADY MADE PUBLIC)|
| `git revert HEAD ` | Creates a new commit with the past version, this is done to matain history|
| `git revert hasvalue ` | Revert to any commit, not only the past version|
 
 ### BRANCH COMMANDS:
 
Branch: A pointer to a particular commit


 | Command | Description |
| --- | --- |
| `git branch --list  ` |List branches in repository|
| `gir branch [name]    `   |Create a new branch|
| `git checkout -b name ` | Create and switch to new branch|
| `git branch -d [name] `   |Delete a branch|
| `git checkout [name]` | Switch to branch|
| `git push --set-upstream origin  [name] ` |  Push to branch|
|`git merge branch `|Merge Head branch with selected branch|

### ADVANCE GIT
##### FORKING
A way of creating a copy of the given repository so that it belongs to our user.
To do a pull request (correct master code) you need to fork the repo and create a new branch.
You can only create 1 pull request per branch, though 1 pull request may have multiple commits 
##### CONTINUOUS INTEGRATION (CI/CD)
Continuos integration enables us to check our code is up and running everytime we create a commit
In ordet to apply CI with github you can use many 3rd parties solutions such as:
<ol>
  <li>Travis</li>
  <li>Jankins </li>
</ol>

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jen-reeve/Mineral-Stability/master?urlpath=rstudio)
