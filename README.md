# xumonad-linux
A minimal xubuntu and xmonad based linux distro and live CD

# Introduction
XUMonad is based on Xubuntu, Xfce and XMonad. A base xubuntu installation is used, with xfce4 as the panel, xmonad as the window
manager and nautilus as the file manager. The latest ISO based on xubuntu 18.04 bionic LTS is here:
https://www.dropbox.com/s/zmugql8pq3itsix/xumonad-dist.iso

## Packages
XUMonad comes with XFCE4, xubuntu without some of the included software like libreoffice and minesweeper. It is built
for functional programming and writting proofs in Coq. It comes with:
- XMonad
- Haskell/GHC/Stack/Cabal
- Emacs/Proof-general with a good .emacs
- opam/Ocaml/Coq
- IntelliJ Community edition
  + scala
  + haskell
- VIM/Vundle with a good .vimrc

## Logging-in the live CD
The username is `xumonad` with no password.

# Create ISO
XUMonad is packaged with the Pinguy-builder found here, maintained by `u/PinGUY`.
https://sourceforge.net/projects/pinguy-os/files/ISO_Builder/

First, setup an xubuntu system from the official Xubuntu live CD with xmonad the way you like it.
Then, copy ~/.xmonad and everything else in the user's home into `/etc/skel`.
The `start-xmonad.sh` script is in `/usr/local/bin` invoked at boot from `/usr/share/xsession/xmonad.desktop`.
Finally, call `PinguyBuilder-gtk` as superuser and use the Gtk UI to create a `dist` iso file in `/home/PinguyBuilder`.

## Burn ISO
Burn ISO to DVD or USB stick with `unetbootin`.

# Lincense

MIT License, I have no obligation towards users.

# Author
Lef Ioannidis <elefthei (at) mit.edu>
