Module search paths
-------------------

When importing a module, Python searches for it in the following order:

* the current directory
* if the module is not found, Python searches in the directories listed in the ``PYTHONPATH`` environment variable
* if the module is still not found, Python checks the default installation path (e.g. ``/usr/local/lib/python3.12/`` on Unix)

Module search paths are stored in the ``sys.path`` variable:

.. code:: python

    In [1]: import sys

    In [2]: sys.path
    Out[2]:
    ['',
     '/usr/local/bin',
     '/usr/local/lib/python312.zip',
     '/usr/local/lib/python3.12',
     '/usr/local/lib/python3.12/lib-dynload',
     '/home/user/venv/pyneng-py3-12/lib/python3.12/site-packages']
