# Install Git

$ mkdir name_folder

$ cd name_folder


## Virtualenv

$ sudo apt install git-all

$ git init

$ git clone https://...

$ git config --global user.name "Votre nom ou pseudo"
$ git config --global user.email "Votre@email.com"

On passe le dossier à virtualenv.

$ virtualenv --version
$ virtualenv nomdudossier 
$ source nomdudossier/bin/activate
$ cd nomdudossier/

---

## Branch

$ git branch

$ git branch new_name

or

$ git checkout -b new_name

**Switch branch**

$ git checkout new_name

**Delete branch**

$ git branch -d branch_name

**To merge a branch**

$ git merge branch_name

##How to abort a conflicting merge in Git:

If you want to throw a merge away and start over, you can run the following command:

$ git merge --abort
