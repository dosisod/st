# st

This is my custom build of `st`.

## Patches

* [alpha](https://st.suckless.org/patches/alpha/)
* [scrollback](https://st.suckless.org/patches/scrollback/)
* [hidecursor](https://st.suckless.org/patches/hidecursor/)
* [boxdraw](http://st.suckless.org/patches/boxdraw/)
* [anysize](https://st.suckless.org/patches/anysize/)
* [undercurl](https://st.suckless.org/patches/undercurl/)
* [font2](https://st.suckless.org/patches/font2/)
* [bgra-glyphs](https://gitlab.freedesktop.org/mawww/libxft.git) patch for libXft

## Building

Since this requires having a patched version of libXft, some initial setup is
required. When first installing:

```
$ git clone --recurse-submodules https://github.com/dosisod/st
$ cd st/libxft
$ git checkout bgra-glyphs
$ sh autogen.sh && ./configure && make
$ cd ../freetype
$ sh autogen.sh && ./configure && make
$ cd ..
```

Tested on Ubuntu 18.04.


Below is a copy of the original README.

```
st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
```
