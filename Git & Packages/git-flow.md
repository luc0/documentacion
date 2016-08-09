# SETTING UP GIT-FLOW

```git flow init```
- It's better to use the default naming scheme. 

# RELEASE

```git flow release start 1.1.5```
- Switched to a new branch 'release/1.1.5'

```git flow release finish 1.1.5```
- pulls from the remote repository
- release content is merged back into both "master" and "develop"
- commit tagged with release name (ex. 1.1.5)
- release branch is deleted, and we're back on "develop"

# HOTFIX

```git flow hotfix start missing-link```
- creates branch "hotfix/missing-link", the branch is based off of "master"

```git flow hotfix finish missing-link```
- release content is merged back into both "master" and "develop"
- hotfix is tagged for easy reference
- branch is deleted, and check out "develop"



REF:
https://www.git-tower.com/learn/git/ebook/en/command-line/advanced-topics/git-flow