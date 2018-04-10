# Installing pgAdmin4 for postgresql environment in Ubuntu 16 Desktop
### Requirements
* python3.5
* virtualenv
* .whl file (postgres)
* sublime (for text editor)

# Install virtualenv run in terminal
    sudo apt-get install virtualenv python3-pip libpq-dev python3-dev
    cd
    virtualenv -p python3 pgadmin4
    cd pgadmin4
    source bin/activate
  
### download latest version of pgadmin visit [PGADMIN LATEST](https://www.pgadmin.org/download/pgadmin-4-python-wheel/)
### paste to virtualenv folder
    pip install ./<filename.whl>
    
## Configuration
    
    subl lib/python3.5/site-packages/pgadmin4/config_local.py
#### Write:
    import os
    DATA_DIR = os.path.realpath(os.path.expanduser(u'~/.pgadmin/'))
    LOG_FILE = os.path.join(DATA_DIR, 'pgadmin4.log')
    SQLITE_PATH = os.path.join(DATA_DIR, 'pgadmin4.db')
    SESSION_DB_PATH = os.path.join(DATA_DIR, 'sessions')
    STORAGE_DIR = os.path.join(DATA_DIR, 'storage')
    SERVER_MODE = False
  
