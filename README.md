# st - simple terminal
st is a simple terminal implementation for X.

### Requirements
In order to build st you need the Xlib header files.

## Patches
All patch was saved on the `patches` directory. Installed patch:
- st-scrollback, st-scrollback-mouse, st-scrollback-mouse-altscreen
- st-nordtheme
- st-boxdraw
- st-anygeometry
- st-font2
- st-w3m

## Added Features
- scrollback support with keyboard and mouse,
- better w3m image support,
- better line render with boxdraw,
- better glyph render with font2,
- font resize on the fly,
- nord theme.
 
## Key Bindings
- scrollback: `alt + up/down`, `alt + pageup/down` for faster scolling, or use `mouse scroll` instead.
- font resize
  - increase: `ctrl + plus` or `ctrl + shift + equal`
  - decrease: `ctrl + minus`
  - reset to default: `ctrl + equal`
- clipboard
  - copy: `ctrl + shift + c`
  - paste: `ctrl + shift + p`

## Installation
Edit `config.mk` to match your local setup (st is installed into the `/usr/local` namespace by default). 
If you want to compile st for OpenBSD you have to remove `-lrt` from `config.mk`.

Afterwards enter the following command to build and install:

    git clone https://github.com/deanvry/st --depth=1
    cd st
    sudo make clean install

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Uninstall
First go to this repo root directory, then enter the following command below:

    sudo make uninstall

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
