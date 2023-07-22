# Simple Terminal

`st` is a simple terminal implementation for X.

## Upstream

The upstream development for `st` can be found [here](https://git.suckless.org/st).

# Patches

- [alpha](https://st.suckless.org/patches/alpha_focus_highlight/)
- [clipboard](https://st.suckless.org/patches/clipboard/)
- [ligatures](https://st.suckless.org/patches/ligatures/)
- [pipe](https://st.suckless.org/patches/externalpipe/)
- [scrollback](https://st.suckless.org/patches/scrollback/)
- [xresources](https://st.suckless.org/patches/xresources/)

# Arch Linux Install

Download the`PKGBUILD` from this repository and run the following command:

```
makepkg -cf
```

This will create a file that ends in `.pkg.tar.zst`. Then run:

```
sudo pacman -U *.pkg.tar.zst
```

# Regular Install

Download the source code from this repository:

```
git clone https://github.com/hooregi/st.git
cd st
sudo make clean install
```
