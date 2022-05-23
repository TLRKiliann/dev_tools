


                                 ██████╗ ██╗████████╗     ██╗ ██████╗███╗   ███╗██████╗ ██╗ 
                                ██╔════╝ ██║╚══██╔══╝    ██╔╝██╔════╝████╗ ████║██╔══██╗╚██╗
                                ██║  ███╗██║   ██║       ██║ ██║     ██╔████╔██║██║  ██║ ██║
                                ██║   ██║██║   ██║       ██║ ██║     ██║╚██╔╝██║██║  ██║ ██║
                                ╚██████╔╝██║   ██║       ╚██╗╚██████╗██║ ╚═╝ ██║██████╔╝██╔╝
                                 ╚═════╝ ╚═╝   ╚═╝        ╚═╝ ╚═════╝╚═╝     ╚═╝╚═════╝ ╚═╝ 

---

# Install Git

`└─ $ ▶ mkdir folder_name`

`└─ $ ▶ cd folder_name`

**First time**

`└─ $ ▶ sudo apt install git-all`

`└─ $ ▶ git clone "https.."` (from ssh or https)

`└─ $ ▶ git init`

`└─ $ ▶ git config --global user.name "pseudo"`

`└─ $ ▶ git config --global user.email "e-mail"`


# Configuration

**Git & Virtualenv**

**First time**

`└─ $ ▶ sudo apt install git-all`

`└─ $ ▶ git init`

`└─ $ ▶ git clone https://address repository`

`└─ $ ▶ git config --global user.name "pseudo"`

`└─ $ ▶ git config --global user.email "e-mail"`

To verif name

`└─ $ ▶ git config user.name`

To verify email

`└─ $ ▶ git config user.email`

**Switch to virtualenv**

`└─ $ ▶ virtualenv --version`

`└─ $ ▶ virtualenv folder_name` 

`└─ $ ▶ source folder_name/bin/activate`

`└─ $ ▶ cd folder_name/`


**Renaming the Local master Branch to main**

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

`└─ $ ▶ nano .gitignore`

Use `/lib/` to hidden your directory, you can use `.log` for files ending with .log.

---

**Alias**

1. You need the git config alias command. Execute the following in a Git repository

`└─ $ ▶ git config alias.ci commit`

2. For global alias

`└─ $ ▶ git config --global alias.ci commit`

3. To enter new configuration

`└─ $ ▶ git config --global alias.co checkout`

After it, you can use :

`└─ $ git co name_of_branch`

4. Create the alias dog for showing the log graph

`└─ $ git config --global alias.dog "log --all --decorate --oneline --graph"`

After it, you can use :

`└─ $ git dog`

5. To show all about your branch with git config

`└─ $ ▶ git config --list --show-origin`

```
file:/home/your_username/.gitconfig   user.name=TLRKiliann
file:/home/your_username/.gitconfig   user.email=philogenie@protonmail.com
file:/home/your_username/.gitconfig   alias.ci=commit
file:/home/your_username/.gitconfig   alias.co=checkout
file:/home/your_username/.gitconfig   alias.dog=log --all --decorate --oneline --graph
file:.git/config        core.repositoryformatversion=0
file:.git/config        core.filemode=true
file:.git/config        core.bare=false
file:.git/config        core.logallrefupdates=true
file:.git/config        remote.origin.url=git@github.com:TLRKiliann/git-cmd.git
file:.git/config        remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
file:.git/config        branch.main.remote=origin
file:.git/config        branch.main.merge=refs/heads/main
file:.git/config        alias.ci=commit
```

6. To see the settings entered

`└─ $ ▶ cat /home/your_username/.gitconfig`

```
[user]
	name = TLRKiliann
	email = philogenie@protonmail.com
[alias]
	ci = commit
	co = checkout
	dog = log --all --decorate --oneline --graph
```

---

# Basic

`└─ $ ▶ git --help`

`└─ $ ▶ git diff`

`└─ $ ▶ git diff file_name.(py,txt,etc)`

`└─ $ ▶ git status` 

`└─ $ ▶ git add name of file`

`└─ $ ▶ git add --all (or -A or .)`

`└─ $ ▶ git commit -m "msg to commit"`

`└─ $ ▶ git push -u origin name_of_branch sender`

---

# Branch

`└─ $ ▶ git branch`

Display all branch

`└─ $ ▶ git branch --all`

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

```
 - [deleted]         newname
```

**Merge a branch**

`└─ $ ▶ git merge branch_name`

**If there is conflict**

`└─ $ ▶git merge --abort`

## How to abort a conflicting merge in Git:

**If you want to throw a merge away and start over, you can run the following command :**

`└─ $ ▶ git merge --abort`


## How to remove a remote branch in Git:

**If you no longer need a remote branch you can remove it using the command below :**

`└─ $ ▶ git push --delete origin branch_name_here`

---

# Log

**Suppose we want to see the changes made to the “main.py” file in our code. We could do so using the following command**

`└─ $ ▶ git log -- main.py`

**To get hash of latest commit**

`└─ $ ▶ git rev-parse HEAD`

`└─ $ ▶ git log <hash_number>`

**The three most recent commit**

`└─ $ ▶ git log -n 3`

`└─ $ ▶ git log --oneline`

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
 
**Shows the patch for each commit as well as their full diff.**

`└─ $ ▶ git log -p` (you can use <git add -p> to add patch)

**Searches for commits by a specified author. The \<pattern\> argument can be a string or a regex.**
           
`└─ $ ▶ git log --author="<pattern>" `
           
**Searches for commits with a commit message. The \<pattern\> argument can be a string or a regex.**

`└─ $ ▶ git log --grep="<pattern>" `

**Displays only commits that occur between \<since\> and \<until\> arguments. Both can be either a commit ID, a branch name, HEAD, or any other kind of revision reference.**

`└─ $ ▶ git log <since>..<until>`

`└─ $ ▶ git log --before="yesterday"`

`└─ $ ▶ git log --after="2022-19-5"`

**What’s happening: git reflog is an amazing resource for recovering project history. You can recover almost anything—anything you’ve committed—via the reflog**

`└─ $ ▶ git reflog`

	
	
	
	
	
	
**Combined**

`└─ $ ▶ git log --oneline master..some-feature`

`└─ $ ▶ git log --after="2022-19-5" --before="2019-3-19"`

`└─ $ ▶ diff --name-only --diff-filter=U`

---

# Merge

**Display branch merged**

`└─ $ ▶ git branch --merged`

**To view branches that contain jobs that have not yet been merged, you can use the git branch --no-merged command**

`└─ $ ▶ git branch --no-merged`

---

# Rebase

## Very clear & good graphic concepts

https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Rebaser-Rebasing

## !!! Never rebase commits that have already been pushed to a public repository !!!

**But don't panic there always possible to undo with :**

`└─ $ ▶ git merge --abort`

or with

`└─ $ ▶ git rebase --abort`

# Rebase with branch

## Warning with merge & rebase, possible conflicts

**From <another> branch with patch to update main branch**

`└─ $ ▶ git rebase main`
*(then git checkout main & git merge <another>)*

**With 3 branch**

`└─ $ ▶ git rebase --onto master serveur client`

**To modify a commit**

`└─ $ ▶ git rebase --interactive 'bbc643cd^'`

---

# Stash

---

# Amend

1. Changing the Last Commit: 

`└─ $ ▶ git commit --amend`

2. Edit hello.py and main.py

`└─ $ ▶ git add hello.py`

`└─ $ ▶ git commit`

3. Realize you forgot to add the changes from main.py 

`└─ $ ▶ git add main.py`

`└─ $ ▶ git commit --amend --no-edit`

`└─ $ ▶ git push --set-upstream origin main`

---

# Push

Pour avertir les autres de cette branch main, vous devez la pousser sur le serveur distant Cela rend la branche renommée disponible sur le serveur distant.

`└─ $ ▶ git push --set-upstream origin main`


Après toutes ces tâches, et s’être assuré que la branche main se comporte comme la branche master, vous pouvez supprimer la branche master :

`└─ $ ▶ git push origin --delete master`

---

# Best combinaisons

**After modifying or editing a file**

`└─ $ ▶ git diff` (with optional filename.etc)

---

**To see all merged or no merged branch**

`└─ $ ▶ git commit branch --merged`

`└─ $ ▶ git commit branch --no-merged`

# SSH

`└─ $ ▶ ssh-keygen -t rsa -b 4096 -C "emailgithub@github.com"`
	
Then add a name if you wish. \
Enter a passphrase at the end (more secure)

`└─ $ ▶ eval $(ssh-agent -s)`

The output of ssh-agent -s is some environment variable assignments, something like SSH_AUTH_SOCK=blahblah; export SSH_AUTH_SOCK etc. When you run eval $(ssh-agent -s), the shell executes that as code, and those variables get set in that shell. The variables there contain the information ssh-add needs to contact the agent, and they get inherited down from the shell to the ssh-add process.
	
`└─ $ ▶ ssh-add (optional name of the key)`

1. Copy the public key (rsa.pub) in GitHub repository (settings > Deploy key)
2. Check the box `Allow write access`.
3. And press `add key`
4. Return to your repository & click button (btn) `code` & copy ssh
5. In you local machine enter

`└─ $ ▶ git clone <ssh copied from btn code>`

