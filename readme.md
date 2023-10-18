# Josh's Notes
## How to compile firmware
- `git clone [this repo]`
- `git fetch [this repo]`
- `git checkout bluetooth_playground`
- `make git-submodule`
- `qmk compile -kb keychron/k3_pro/ansi/rgb -km via`
  - or just `qmk compile` if you have set defaults

## How to upload firmware
- Install QmkToolbox
- Put keyboard in bootloader mode
  - For the K3 Pro take off the spacebar
  - Turn the K3 Pro off using the toggle
  - Hold the reset button under the spacebar and then turn it on
  - QmkToolbox should now recognise the keyboard
- Use QmkToolbox to upload the firmware which is located in the qmk_firmware folder
 
# Sensitive Defaults
## Settings a default keyboard
Often only have 1 keyboard
- `qmk list-keyboards | grep [k3_pro]`
- `qmk config user.keyboard=keychron/k3_pro/ansi/rgb`
- `qmk config user.keymap=[github username]` to create a new keymap default
- `qmk new-keymap` to create a new keymap default

To compile using the new keymap go
- `qmk compile -kb keychron/k3_pro/ansi/rgb -km [joshpiper/github username]`

# Quantum Mechanical Keyboard Firmware

[![Current Version](https://img.shields.io/github/tag/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/tags)
[![Discord](https://img.shields.io/discord/440868230475677696.svg)](https://discord.gg/Uq7gcHh)
[![Docs Status](https://img.shields.io/badge/docs-ready-orange.svg)](https://docs.qmk.fm)
[![GitHub contributors](https://img.shields.io/github/contributors/qmk/qmk_firmware.svg)](https://github.com/qmk/qmk_firmware/pulse/monthly)
[![GitHub forks](https://img.shields.io/github/forks/qmk/qmk_firmware.svg?style=social&label=Fork)](https://github.com/qmk/qmk_firmware/)

This is a keyboard firmware based on the [tmk\_keyboard firmware](https://github.com/tmk/tmk_keyboard) with some useful features for Atmel AVR and ARM controllers, and more specifically, the [OLKB product line](https://olkb.com), the [ErgoDox EZ](https://ergodox-ez.com) keyboard, and the [Clueboard product line](https://clueboard.co).

## Documentation

* [See the official documentation on docs.qmk.fm](https://docs.qmk.fm)

The docs are powered by [Docsify](https://docsify.js.org/) and hosted on [GitHub](/docs/). They are also viewable offline; see [Previewing the Documentation](https://docs.qmk.fm/#/contributing?id=previewing-the-documentation) for more details.

You can request changes by making a fork and opening a [pull request](https://github.com/qmk/qmk_firmware/pulls), or by clicking the "Edit this page" link at the bottom of any page.

## Supported Keyboards

* [Planck](/keyboards/planck/)
* [Preonic](/keyboards/preonic/)
* [ErgoDox EZ](/keyboards/ergodox_ez/)
* [Clueboard](/keyboards/clueboard/)
* [Cluepad](/keyboards/clueboard/17/)
* [Atreus](/keyboards/atreus/)

The project also includes community support for [lots of other keyboards](/keyboards/).

## Maintainers

QMK is developed and maintained by Jack Humbert of OLKB with contributions from the community, and of course, [Hasu](https://github.com/tmk). The OLKB product firmwares are maintained by [Jack Humbert](https://github.com/jackhumbert), the Ergodox EZ by [ZSA Technology Labs](https://github.com/zsa), the Clueboard by [Zach White](https://github.com/skullydazed), and the Atreus by [Phil Hagelberg](https://github.com/technomancy).

## Official Website

[qmk.fm](https://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.
