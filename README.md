# Installing pgAdmin4 for postgresql environment in Ubuntu Desktop
### Requirements
* python3.5
* virtualenv
* .whl file (postgres)
* sublime (for text editor)

# Install virtualenv run in terminal
    sudo apt-get install virtualenv python3-pip libpq-dev python3-dev
    cd
    virtualenv -p python3 pgadmin4 (pgadmin4 or whatever you want)
    cd pgadmin4
    source bin/activate
  
### download latest version of pgadmin visit [PGADMIN LATEST](https://www.pgadmin.org/download/pgadmin-4-python-wheel/)
### paste to virtualenv folder
    pip install ./<filename.whl>
    
## Configuration
    
    subl lib/python3.x/site-packages/pgadmin4/config_local.py
#### Write:
    import os
    DATA_DIR = os.path.realpath(os.path.expanduser(u'~/.pgadmin/'))
    LOG_FILE = os.path.join(DATA_DIR, 'pgadmin4.log')
    SQLITE_PATH = os.path.join(DATA_DIR, 'pgadmin4.db')
    SESSION_DB_PATH = os.path.join(DATA_DIR, 'sessions')
    STORAGE_DIR = os.path.join(DATA_DIR, 'storage')
    SERVER_MODE = False
  
#### RUN:
    python lib/python3.x/site-packages/pgadmin4/pgAdmin4.py

#### ACCESS:
    http://localhost:5050
    
    if you have access error try to install requirements.txt
    pip install -r requirements.txt
 
#### MAKE A SHORTCUT:
    touch ~/pgadmin4/pgadmin4
    chmod +x ~/pgadmin4/pgadmin4
    subl ~/pgadmin4/pgadmin4
    
#### Write:
    #!/bin/bash
    cd ~/pgadmin4
    source bin/activate
    python lib/python3.x/site-packages/pgadmin4/pgAdmin4.py
    
#### Now you can just run it with a simpler command:
    ~/pgadmin4/pgadmin4
    
    Other option to make it more simplier
    alias pgadmin4=~/pgadmin4/pgadmin4
    then try to run just pgadmin4
    
#### Creating /bash_aliases for permanent alias
    touch ~/.bash_aliases
    vim or subl ~/.bash_aliases
    add lines
    alias guipgadmin or whatever shortcut you want for terminal
    alias pgadmin4=~/pgadmin4/pgadmin4
    
    
