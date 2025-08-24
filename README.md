# My personal QMK configuration

This repository contains the sources for the firmware of the keyboards that I use.
Currently, this repository contains sources for:

- [Keychron Q3](https://www.keychron.com/products/keychron-q3-qmk-custom-mechanical-keyboard?variant=39773518692441)

## Prerequisites

You'll need the QMK firmware tooling on your machine. You can get this via various installation methods.

1. Arch Linux: `pacman -S qmk`
1. Windows WSL: `pip install --user qmk`
1. MacOS: `pip install --user qmk`

## Getting started

1. Run the normal `qmk setup` procedure if you haven't already done so -- see [QMK Docs](https://docs.qmk.fm/#/newbs) for details.
1. Clone this repository to your local machine
1. Enable userspace in QMK config using `qmk config user.overlay_dir="$(realpath qmk_configuration)"`
1. Configure the keyboard `qmk config user.keyboard=keychron/q3/ansi`
1. Configure the keymap `qmk config user.keymap=wmeints`
1. Run `qmk compile` to compile the keyboard firmware
1. Flash the keyboard with `qmk flash`. 

**Note:** The flash procedure requires the keyboard to be in bootloader mode. You can achieve this by holding the Esc key and reconnecting the USB cable.
After flashing, the keyboard automatically returns to normal operational mode.

