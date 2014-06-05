Digital edition of the Well-tempered Clavier
============================================

This repository is a digital edition of the the Well-tempered Clavier
by J.S. Bach (Books I & II), encoded in the Humdrum file format.
Tools for processing the encodings in this format on the command-line
can be found online at https://github.com/humdrum-tools


These digital scores can also be found as a submodule in the 
[humdrum-data](https://github.com/humdrum-tools/humdrum-data) repository.


Data processing tools and other resources
=========================================

These digital scores may also be found on the kernScores website:
*    http://kernscores.stanford.edu/browse?l=wtc

with mirrors at:
*    http://kern.humdrum.org/browse?l=wtc
*    http://kern.ccarh.org/browse?l=wtc

which includes dynamic conversions to other data formats.  

The [Humdrum Extras](http://extras.humdrum.org) command-line programs 
can download these files from kernScores.  A quick method of downloading:
```bash
    mkdir -p bach-js/wtc
    cd bach-js/wtc
    humsplit h://wtc
```
To get online access to a single movement, for example to transpose the first 
prelude into D-flat major:
```bash
   transpose -k d- h://wtc/wtc1p01
```

To interface to the Humdrum Toolkit commands, use the humcat command to download to standard input (the -s option is needed when downloading multiple files):
```bash
   humcat -s h://wtc | census -k
```


Makefile
========

The makefile provided in the base directory includes example data
processing commands.  Type ```make``` when in the same directory as the
makefile to list commands that can be run with the makefile.

If the command ```which make``` reports that the make command cannot
be found, then you must install it.  In linux, this command might
install it:
```bash
   sudo apt-get install build-essential
   # or
   sudo yum install build-essential
```

In OS X Mavericks or later, install the Xcode command-line tools:
```bash
   xcode-select --install
```

In Cygwin on MS Windows, re-run the cygwin install program and make sure
that the development tools are included in the installation packages.



