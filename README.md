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
* [sixel](https://github.com/bakkeby/st-flexipatch)
* ["maxcol"](https://github.com/nimaipatel/st/blob/master/patches/7672445bab01cb4e861651dc540566ac22e25812.diff)

## Building

On Arch Linux, install the [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/)
and [freetype2](https://archlinux.org/packages/extra/x86_64/freetype2/)
packages, then run `make && sudo make install`.

For instructions for building on Ubuntu 18.04, click
[here](https://github.com/dosisod/st/tree/ubuntu1804#building).

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
