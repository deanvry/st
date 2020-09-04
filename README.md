# st - simple terminal
st is a simple terminal emulator for X which sucks less.

## Requirements
In order to build st you need the Xlib header files.

## Patches
All patch was saved on the `patches` directory. Installed patch:
- st-scrollback, st-scrollback-mouse, st-scrollback-mouse-altscreen
 
## Key Bindings
- scrollback: use `alt + up/down`, `shift + pageup/down`, or `mouse scroll` instead.
- font resize (zoom)
  - up: `ctrl + plus` or `ctrl + shift + equal`
  - down: `ctrl + minus`
  - reset: `ctrl + equal`

## Installation
Edit `config.mk` to match your local setup (st is installed into
the `/usr/local` namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    git clone https://github.com/deanvry/st
    cd st
    sudo make clean install

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Uninstall
If you want to uninstall st, run the command below on the repo root folder.

    sudo make uninstall

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
