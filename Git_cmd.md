


           ██████╗ ██╗████████╗     ██╗ ██████╗███╗   ███╗██████╗ ██╗ 
          ██╔════╝ ██║╚══██╔══╝    ██╔╝██╔════╝████╗ ████║██╔══██╗╚██╗
          ██║  ███╗██║   ██║       ██║ ██║     ██╔████╔██║██║  ██║ ██║
          ██║   ██║██║   ██║       ██║ ██║     ██║╚██╔╝██║██║  ██║ ██║
          ╚██████╔╝██║   ██║       ╚██╗╚██████╗██║ ╚═╝ ██║██████╔╝██╔╝
           ╚═════╝ ╚═╝   ╚═╝        ╚═╝ ╚═════╝╚═╝     ╚═╝╚═════╝ ╚═╝ 



```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```

```diff
Install Git
```

`└─ $ ▶ mkdir folder_name`

`└─ $ ▶ cd folder_name`


## Git & Virtualenv

`└─ $ ▶ sudo apt install git-all`

`└─ $ ▶ git init`

`└─ $ ▶ git clone https://...`

`└─ $ ▶ git config --global user.name "pseudo"`

`└─ $ ▶ git config --global user.email "e-mail"`


## Switch to virtualenv

`└─ $ ▶ virtualenv --version`

`└─ $ ▶ virtualenv folder_name` 

`└─ $ ▶ source folder_name/bin/activate`

`└─ $ ▶ cd folder_name/`


## Renaming the Local master Branch to main

`└─ $ ▶ git branch -m master main`

`└─ $ ▶ git branch`

`└─ $ ▶ git status`

**To verify**

`└─ $ ▶ git push -u origin main`

Return

``` 
...
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```


### Basic

`└─ $ ▶ git --help`

`└─ $ ▶ git status` 

`└─ $ ▶ git add name of file`

`└─ $ ▶ git add --all (or -A or .)`

`└─ $ ▶ git commit -m "msg to commit"`

`└─ $ ▶ git push -u origin name_of_branch sender`


### Branch

`└─ $ ▶ git branch`

**Create a branch**

`└─ $ ▶ git branch new_name`

or

**Create & switch at same time to new branch**

`└─ $ ▶ git checkout -b new_name`

**Switch branch**

`└─ $ ▶ git checkout new_name`


**Delete branch**

`└─ $ ▶ git branch -d branch_name`

**How to remove a remote branch in Git**
*If you no longer need a remote branch you can remove it using the command below:*

`└─ $ ▶ git push --delete origin branch_name_here`

Return

 - [deleted]         newname


**Merge a branch**

`└─ $ ▶ git merge branch_name`


### How to abort a conflicting merge in Git:

**If you want to throw a merge away and start over, you can run the following command :**

`└─ $ ▶ git merge --abort`


### How to remove a remote branch in Git:

**If you no longer need a remote branch you can remove it using the command below :**

`└─ $ ▶ git push --delete origin branch_name_here`


### Log

`└─ $ ▶ git log <hash_number>`

**The three most recent commit**

`└─ $ ▶ git log -n 3`

`└─ $ ▶ git log --graph --oneline`

`└─ $ ▶ git log --graph --oneline --all`

Return

```
* 18d997e (HEAD -> seconduser, origin/seconduser) file modified
* 92f83a8 (origin/master, origin/HEAD, main) delete files
*   75c5eff some changes
|\  
| * 2d0a56d deleted files
| * c882ad4 changes
| * dbbb2d9 changes added
* | cc76b1c file5 changes
* |   a37a660 Merge branch 'master' of https://github.com/Main_name/git-cmd
|\ \  
| * \   844834c Merge pull request #1 from Main_name/newname
| |\ \  
* | \ \   146d1b1 Merge branch 'newname'
|\ \ \ \  
| | |_|/  
| |/| |   
| * | | 1d5d884 new file5
| | |/  
| |/|   
| * | 0302b8e to verify
* | | fe0240f file4.txt changes
* | | e8dc3ca new file added
| |/  
```

**Includes changed files and the number of added or deleted lines from them besides the git log information.**

`└─ $ ▶ git log --stat`

Return

```
commit ab30fa84b50394da345567802925b01b8f4eabcc0
Author: Name <name@mail.com>
Date:   Sat May 21 11:38:52 2022 +0200

    some cmd added

 Git_cmd.md | 35 +++++++++++++++++++++--------------
 1 file changed, 21 insertions(+), 14 deletions(-)
 ```


**What’s happening: git reflog is an amazing resource for recovering project history. You can recover almost anything—anything you’ve committed—via the reflog.**

`└─ $ ▶ git reflog`

---

rebase & stash
