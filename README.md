dspdfviewer-pkgsrc
==================

NetBSD pkgsrc script for dspdfviewer

You can find dspdfviewer [here][1]

Installation
------------

Copy `print/dspdfviewer` folder to `/usr/pkgsrc` directory.

NOTE: If your pkgsrc directory is different from above, copy to the respective
place.

Usage
-----

Once you have copied the folder, install it as you would do for any package.

`$ cd /usr/pkgsrc/print/dispdfviewer`<br>
`$ make install clean`

For a list of dependencies for the build check [here][2]

NOTE: If you are using pkgsrc in a non NetBSD system, replace `make` with
`bmake` in the above example.

Credits
-------

* The Dual-Screen PDF Viewer was originally written by [Danny Edel][3]
* Thanks to `trouble` and `cherry` for a machine to do and help with the package
  development as well as testing and fixing of the package.
* Thanks to `wiz` for reviewing and suggesting fixes / changes to conform to
  standardized `Makefile`.

License
-------

BSD 2-clause. See LICENSE.

[1]: http://dspdfviewer.danny-edel.de/
[2]: http://dspdfviewer.danny-edel.de/installation/source/options.html
[3]: https://github.com/dannyedel
