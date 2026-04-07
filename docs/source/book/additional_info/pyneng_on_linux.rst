.. raw:: latex

   \newpage

.. _additional_info_pyneng_linux:

Preparing Linux
===============

Installing Python 3.10 on Debian
---------------------------------

If you are installing on a clean OS, it is best to install these packages:

::

    sudo apt-get install build-essential checkinstall
    sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev
    sudo apt-get install libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev

Installing Python 3.10

::

    wget https://www.python.org/ftp/python/3.10.12/Python-3.10.12.tgz
    tar xvf Python-3.10.12.tgz
    cd Python-3.10.12
    ./configure --enable-optimizations --enable-loadable-sqlite-extensions
    sudo make altinstall

After that, you can create a `virtual environment <https://pyneng.readthedocs.io/en/latest/book/01_intro/virtualenv.html>`__.

Virtual environment
-------------------

Installing virtualenvwrapper with pip:

::

    python3.10 -m pip install virtualenvwrapper

After installation, in ``~/.bashrc`` file in current user's home folder, you need
to add several lines:

::

    export VIRTUALENVWRAPPER_PYTHON=/usr/local/bin/python3.10
    export WORKON_HOME=~/venv

    . /usr/local/bin/virtualenvwrapper.sh

Restart command interpreter:

::

    exec bash

Create a virtual environment using Python 3.10 (the same command will take you to a virtual environment):

::

    mkvirtualenv --python=/usr/local/bin/python3.10 pyneng-py3


List of modules that need to be installed to complete tasks
-----------------------------------------------------------

::

    pip install pytest pytest-clarity pyyaml tabulate jinja2 textfsm pexpect netmiko

You also need to install graphviz on the OS (example for debian):

::

    apt-get install graphviz

