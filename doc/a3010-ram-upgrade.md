# A3010 4 MiB RAM Upgrade

A 4 MiB RAM upgrade for the Acorn A3010.

<a href="/doc/a3010-ram-upgrade.md"><img src="/jpeg/a3010-ram-upgrade-front.jpeg" width="480"></a>

- [Schematic](/pdf/a3010-ram-upgrade-schematic.pdf)
- [Layout](/pdf/a3010-ram-upgrade-layout.pdf)
- [Gerber](https://github.com/dpicken/acorn-hw/raw/master/gerber/a3010-ram-upgrade.zip)
- [BOM](/pdf/a3010-ram-upgrade-bom.pdf)

# Assembly notes

Tin the RAM IC pins and PCB pads, then solder the ICs to the PCB with hot-air:

<a href="/doc/a3010-ram-upgrade.md"><img src="/jpeg/a3010-ram-upgrade-assembly-1.jpeg" width="480"></a>

If using individual machined pins:

  - cover the motherboard's IC6 and IC11 connectors with kapton tape
  - lay the RAM upgrade board on top
  - insert a pin through the center of each hole
  - solder all pins
  - remove the board and tape

The result should be:

<a href="/doc/a3010-ram-upgrade.md"><img src="/jpeg/a3010-ram-upgrade-assembly-2.jpeg" width="480"></a>

# Installation

Install the RAM upgrade board, ensuring its IC6 and IC11 footprints align with the motherboard's IC6 and IC11 connectors.

Configure the A3010's RAM links:

  - LK20: connect pins 2 and 3
  - LK21: connect pins 1 and 2
  - LK22: no connections

<a href="/doc/a3010-ram-upgrade.md"><img src="/jpeg/a3010-ram-upgrade-installation.jpeg" width="480"></a>

