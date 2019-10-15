NetBeans Local Respository Builder
==================================

A simple bit of tooling that lets you populate your local repository
with NetBeans modules from a netbeans build.

Usage
-----

```
./build-all /path/to/netbeans/source/dir RELEASEnnn
```

to populate your local Maven repository from the NetBeans source dir
(this will run the necessary Ant targets to have a complete install).


Hints
-----

 1. If you just did a git pull, do yourself a favor and run `ant clean`
in the netbeans source dir first; that is not done by default since
you may be patching modules and just wanting an update including your
patches.

 2. Resist the temptation to use `-SNAPSHOT` in your version.  98% of
Maven hatred and loathing is caused by the ill-advised
download-the-whole-internet magic `-SNAPSHOT` causes Maven to perform.
It is ~~almost~~ always a mistake to use it.
