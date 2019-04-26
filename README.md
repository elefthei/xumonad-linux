# xumonad-linux
A minimal xubuntu and xmonad based linux distro and live CD based on xubuntu 18.04 LTS.

![screenshot](https://raw.githubusercontent.com/elefthei/xumonad-linux/master/assets/screenshot.png)

`sha256: 24b8d3938635e6057498446a5c928e8aaa4185d42d7525394158eafe635cdc7e  xumonad-dist.iso`

# Introduction
XUMonad is based on Xubuntu, Xfce and XMonad. Xubuntu is the base OS, xfce4 is the panel and utilities, xmonad is the window
manager and nautilus is the file manager. The latest ISO is based on xubuntu 18.04 bionic LTS. I write Haskell, Scala and Coq
so these are available in xumonad,

## Logging-in the live CD
The username is `xumonad` with no password.

## Usage
Standard xmonad hotkeys apply, although the meta-key is used instead of Alt. `Meta-p` opens the `rofi` program launcher,
a lightweight replacement for `dmenu`. XUmonad comes with the `xfce4-panel` as a status bar, although it is customary
to use `xmobar` I found the xfce panel easier to use, able to listen to xmonad through `ewmh` and customizable through point-and-click.

## Download

Download xumonad [ISO](https://www.dropbox.com/s/zmugql8pq3itsix/xumonad-dist.iso).

# Packages
XUMonad comes with xubuntu, minus some software like libreoffice and minesweeper. It comes with:
- XMonad/rofi/xfce4
- Haskell/GHC/Stack/Cabal
- Emacs with a good .emacs
- VIM/Vundle with a good .vimrc
- opam/Ocaml/Coq
- IntelliJ Community edition
  + scala
  + haskell

## How to create your own ISO
XUMonad is packaged with the Pinguy-builder from PinguyOS.

First, setup an xubuntu system from the official Xubuntu live CD with xmonad the way you like it.
Then, copy `~/.xmonad` and everything else in the user's home into `/etc/skel`.
The `start-xmonad.sh` script is in `/usr/local/bin` invoked at boot from `/usr/share/xsession/xmonad.desktop`.
Finally, call `PinguyBuilder-gtk` as superuser and use the Gtk UI to create a `dist` iso file in `/home/PinguyBuilder`.

## How to Burn ISO
Burn ISO to DVD or USB stick with `unetbootin`.

# License

XUMonad comes wtih non-free software.
MIT License. I have no obligation towards users.

*Lef Ioannidis, elefthei (at) mit.edu*
