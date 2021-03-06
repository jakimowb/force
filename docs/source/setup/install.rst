.. _install:

Installation
============

FORCE is mostly written in C/C++: This, it needs to be compiled. Administrator rights are not necessarily required, unless you want to install to the system-wide search path (e.g. to make it available to muptiple users).

1. Create a directory, e.g.

  .. code-block:: bash

    mkdir -p ~/src/force
    cd ~/src/force

2. Pull from Github

  .. code-block:: bash

    git need to check, update later

3. Edit the Makefile with the text editor of your choice, e.g.

  .. code-block:: bash

    vi Makefile

  * `BINDIR` is the directory used for installing the software. 

    * By default, this is ``/usr/local/bin``. This is a system-wide search path. If you install to this directory, all users on this machine can use the code. You need admin rights to install to this directory. 

    * Alternatively, you can specify a private directory, e.g. ``/home/YOURNAME/bin``. In this case, the code is only available to you, but you do not need admin rights for the installation.

  * The next block specifies the location of libraries and headers. It might be possible that you need to make some changes here.

  * The rest of the Makefile should be OK. Only edit anything if you know what you are doing.

4. Compile the code

  .. code-block:: bash

    make -j

5. Install the code. If you are installing to a system directory, include ``sudo`` to install with admin rights. If you are installing to a private directory, remove the ``sudo``.

  .. code-block:: bash

    sudo make install

6. Test if it was installed correctly:

  .. code-block:: bash

    force

  If the program cannot be found, you will likely need to add this directory to your search path ``$PATH`` (see `here <https://opensource.com/article/17/6/set-path-linux>`_). This might happen if you have used a custom installation directory.


Installation with optional software
-----------------------------------

* Install with SPLITS.

  Follow these steps before step 3 in the installation instruction:

  a) Install SPLITS, see :ref:`depend-opt`

  b) In ``src/cross-level/const-cl.h``, uncomment the SPLITS preprocessor definition ``#define SPLITS``.
     
     .. code-block:: bash

       vi src/cross-level/const-cl.h
  
  c) Edit the Makefile
  
     .. code-block:: bash

       vi Makefile

     ``SPLITS`` names the directories, where SPLITS header files and library are installed.     
     This line needs to be uncommented, and probably adjusted to your needs.
     
     Example: 
     
     ``SPLITS=-I/usr/local/include/splits -L/usr/local/lib -Wl,-rpath=/usr/local/lib``
     
     Additionally, uncomment the ``LDSPLITS`` line.

  d) Proceed with the installation of FORCE
  
  