

             ▄▀▀█▄   ▄▀▀▄ ▀▄  ▄▀▀█▄   ▄▀▄▄▄▄   ▄▀▀▀▀▄   ▄▀▀▄ ▀▄  ▄▀▀█▄▄   ▄▀▀█▄  
            ▐ ▄▀ ▀▄ █  █ █ █ ▐ ▄▀ ▀▄ █ █    ▌ █      █ █  █ █ █ █ ▄▀   █ ▐ ▄▀ ▀▄  
              █▄▄▄█ ▐  █  ▀█   █▄▄▄█ ▐ █      █      █ ▐  █  ▀█ ▐ █    █   █▄▄▄█ 
             ▄▀   █   █   █   ▄▀   █   █      ▀▄    ▄▀   █   █    █    █  ▄▀   █ 
            █   ▄▀  ▄▀   █   █   ▄▀   ▄▀▄▄▄▄▀   ▀▀▀▀   ▄▀   █    ▄▀▄▄▄▄▀ █   ▄▀  
            ▐   ▐   █    ▐   ▐   ▐   █     ▐           █    ▐   █     ▐  ▐   ▐   
          
---

# Install Anaconda

--------

- Downloading \
https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh

---

Decompile Folder

`└─ $ ▶ bash ~/Downloads/Anaconda3-2022.05-Linux-x86_64.sh`

---

Version

`└─ $ ▶ conda --versions`

---

Change $path

`└─ $ ▶ export PATH=~/anaconda3/bin:$PATH`

---

Create virtualenv

`└─ $ ▶ conda create --name env79 python=3.9`

---

if ERROR

`└─ $ ▶ source ~/.bashrc`

(base) \
`└─ $ ▶ conda activate env79`

(env79) \
`└─ $ ▶ On y est !!!`

---

Install pytorch

`└─ $ ▶ conda install -c pytorch pytorch`

---

LIST
----

To see all env

`└─ $ ▶ conda info --envs`

or

(base) \
`└─ $ ▶ conda env list`

```
# conda environments:
#
base                  *  /home/esteban/anaconda3
env79                    /home/esteban/anaconda3/envs/env79
```

---

To see all packages :

(env79) \
`└─ $ ▶ conda list`

you can see versions of : 

> python (3.9)
> pip (21.2.4)
> cudatoolkit

---

DEACTIVATE

`└─ $ ▶ conda deactivate`

(base) \
`└─ $ ▶ You are in second virtualenv.`

```
(base) restart automatically in every time you open a terminal
To set the auto_activate_base parameter to false, type :
```

`└─ $ ▶ conda config --set auto_activate_base false`

ACTIVATE

`└─ $ ▶ conda activate env79`

QUIT (base)

`└─ $ ▶ conda deactivate`

REMOVE package

`└─ $ ▶ conda remove <name_of_package>`

UPDATE

`└─ $ ▶ conda update --all`

---

INSTALL
-------

For install libraries with pip command
copy the link : https://pypi.org/project/sty/
and in your terminal

`└─ $ ▶ pip install sty`


If you want to install flask for example:
In browser: flask conda install

`└─ $ ▶ conda install -c anaconda flask`

---

JUPYTER
-------

(env79)
Install Jupyter

`└─ $ ▶ conda install -c anaconda jupyter`

Open Jupyter notebook (browser)

`└─ $ ▶ jupyter notebook`

> Use Control-C to stop this server and shut down all kernels 

---

> You browser display your user directory
> Choose to go to Documents in GUI
> and click new button and choice python3 (a new tab is opened)
> don't forget to save and take a look where youre file created is.

---

GitHub
> Create a new repository and upload your "file_name.pynb" from GitHub.

or

https://anaconda.org/anaconda/git

To install this package with conda run:

`└─ $ ▶ conda install -c anaconda git`

---
