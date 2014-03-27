measure-times
=============

This is a very simple tool that runs a command and measures the time
it takes to run. It allows to define samples (i.e. patterns) to grep
and generate timestamps for in the standard output of the command.

**NOTE:** There is currently no `setup.py` script to install this
little tool into your system.

Usage examples
--------------

List all files in `/usr/bin` and show timestamps for when anything
related to `gcc` or `vim` was logged:

    ./measure-times -s gcc -s vim -- ls -1 /usr/bin

The end of the output will something like:

    Summary:

    2014-03-27 15:44:58.592745: start
    2014-03-27 15:44:58.611523: ('vim',): evim
    2014-03-27 15:44:58.613958: ('gcc',): gcc
    2014-03-27 15:44:58.614019: ('gcc',): gcc-ar
    2014-03-27 15:44:58.614083: ('gcc',): gcc-nm
    2014-03-27 15:44:58.614144: ('gcc',): gcc-ranlib
    2014-03-27 15:44:58.622218: ('vim',): gvim
    2014-03-27 15:44:58.622276: ('vim',): gvimdiff
    2014-03-27 15:44:58.622313: ('vim',): gvimtutor
    2014-03-27 15:44:58.650523: ('vim',): rvim
    2014-03-27 15:44:58.660019: ('vim',): vim
    2014-03-27 15:44:58.660064: ('vim',): vimdiff
    2014-03-27 15:44:58.660099: ('vim',): vimdot
    2014-03-27 15:44:58.660133: ('vim',): vimtutor
    2014-03-27 15:44:58.660166: ('vim',): vimx
    2014-03-27 15:44:58.662087: ('gcc',): x86_64-redhat-linux-gcc
    2014-03-27 15:44:58.665203: stop

License
-------

measure-times is copyright (C) 2014 Jannis Pohlmann <jannis@xfce.org>.
It is licensed under GNU GPLv2.
