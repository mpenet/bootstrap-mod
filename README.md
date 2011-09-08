bootstrap-mod
=============


Modular version of [https://github.com/twitter/bootstrap](twitter/bootstrap)
with minor differences

The goal is to add a clear separation between the different parts of
[https://github.com/twitter/bootstrap](bootstrap), allowing you to
select only the stuff you need and have fine grained control over the
generated files.

You can for instance only require the grid + reset + typo.

How to use
-----------

Files starting with _ are meant to be included in other files

_global add a context to the final files such as colors, sizes, utility
functions.
It can be included anywhere and wont generate any css alone.

When generating a build for your use you need to be aware of the
include chain in case you made modifications in _global included files.

To be sure you are up to date you need to compile the _* files first,
_global right after that, then your final less file.

Differences from Bootstrap
--------------------------

* .clearfix form row, is called "form-row" now


Build
-----

To build use you favorite minifier/packing util or simply cat on the
resulting css files. Dont use less to concat the less files together
since global is included more than once it would cause less mixins
duplicates.

Todo
----

* Basic build