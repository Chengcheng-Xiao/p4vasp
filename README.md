p4vasp
==========================

Copyright notes:
The p4vasp is distributed under the General Public License version 2 (GPL2).

For more information and support visit www.p4vasp.at.

Binary distributions
==========================

Binary distribution contains a single executable file.
Place this file at a convenient location (e.g. Desktop)
and add it to the system PATH.
P4vasp is a portable application - it can be started from a usb drive.


Source-code distributions
==========================

Compilation Quickstart
--------------------------

For local installation run:
```
   $ ./install-local.sh
```

For global installation run:
```
   $ ./install.sh
```

Installation (local)
--------------------------

1) Make sure you have all the dependencies.
   In Ubuntu you can do it with a supplied script: `install/install-ubuntu-dependencies.sh`
2) If there are previous versions of p4vasp, uninstall them.
   You can do it with the `uninstall.sh` residing in the `P4VASP_HOME` directory.
3) Unpack the file:                
```
   $ tar -xvzf p4vasp-x.x.x.tgz
```
4) Change directory:               
```
   $ cd p4vasp-x.x.x
```

__OPTIONAL__: Apply patch for VASP [v5.4.4+]:
```
patch -p0 < 544_update.patch
```

5) Configure:                      
```
   $ make local
```
6) check and adjust the paths in `install/Configuration.mk`
7) Install:                        
```
   $ make install
```
8) Add path to p4v in the .bashrc  
```
   $ make bashrc
```


Installation (global)
--------------------------

1) Make sure you have all the dependencies.
   In Ubuntu you can do it with a supplied script: `install/install-ubuntu-dependencies.sh`
2) Uninstall the old version (as root):
                        This usually (depending on your installation) can be done with an uninstall script:
```                        
   $ sudo bash /usr/lib/p4vasp/uninstall.sh
```
3) Unpack the file:     
```
   $ tar -xvzf p4vasp-x.x.x.tgz
```
4) Change directory:    
```
   $ cd p4vasp-x.x.x
```

__OPTIONAL__: Apply patch for VASP [v5.4.4+]:
```
patch -p0 < 544_update.patch
```

5) Configure:           
```
   $ make config
```
6) install (as root):   
```
   $ make install
```
7) If something goes wrong
   - Run the diagnostic.py script, it may provide you with some hints.
   - Check FAQ
   - We can try to help you if you visit forum at www.p4vasp.at, please provide us with the output from diagnostic.py.



Installation (macOS)
--------------------------

Check out [installation instructions](README_MacOS.md).


Starting:
--------------------------

Start with: `p4v`

Look at the documentation in the `doc/intro/intro.html`
(or `/usr/lib/p4vasp/doc/intro.html`, when installed),
if you need some clues how to deal with the p4v GUI.

Some people prefer command-line tools and automatic scripts
to a graphical interface. For those, there are some simple
scripts in the utils directory (`/usr/lib/p4vasp/utils`).
They are also a good example for the p4vasp-API.


P4vasp package embeds the odpdom library, that is available also as a [separate
project](http://sourceforge.net/projects/odpdom) and a slightly modified version
of the [piddle library](piddle.sourceforge.net).
Both odpdom and piddle are available under the LGPL License (see
odpdom/COPYING).

This package as well may contain other packages (in ext directory) under various open-source licenses:
[fltk](www.fltk.org), [sqlite](www.sqlite.org) and [pysqlite](code.google.com/p/pysqlite).
These packages are provided for convenience only to make the installation easier.
