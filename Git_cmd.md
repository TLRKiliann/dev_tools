# Install Git

`$ mkdir name_folder`

`$ cd name_folder`


## Virtualenv

$ sudo apt install git-all

$ git init

$ git clone https://...

$ git config --global user.name "pseudo"

$ git config --global user.email "e-mail"

**Switch to virtualenv**

$ virtualenv --version

$ virtualenv nomdudossier 

$ source nomdudossier/bin/activate

$ cd nomdudossier/

---

### Basic

$ git --help

$ git status

$ git add name of file

$ git add --all (or -A or .)

$ git commit -m "msg to commit"

$ git push -u origin name_of_branch sender

---

### Branch

$ git branch

**Create a branch**

$ git branch new_name

or

**Create & switch at same time to new branch**

$ git checkout -b new_name

**Switch branch**

$ git checkout new_name

**Delete branch**

$ git branch -d branch_name

**To merge a branch**

$ git merge branch_name

---

### How to abort a conflicting merge in Git:

**If you want to throw a merge away and start over, you can run the following command :**

$ git merge --abort

---

### How to remove a remote branch in Git:

**If you no longer need a remote branch you can remove it using the command below :**

$ git push --delete origin branch_name_here

---

### Log

$ git log <hash_number>

**The three most recent commit**

$ git log -n 3

$ git log --graph --oneline

$ git log --graph --oneline --all

---

rebase & stash




