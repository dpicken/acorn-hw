# A3010 SysClk Switcher

An overclocking solution for the Acorn A3010 (and A3020/A4000), inspired by [stardot](https://stardot.org.uk/forums/viewtopic.php?t=21639).  Fits in the X3 position of later issue A3010 motherboards.

<a href="/doc/a3010-sysclk-switcher.md"><img src="/jpeg/a3010-sysclk-switcher.jpeg" width="480"></a>

- [Schematic](/pdf/a3010-sysclk-switcher-schematic.pdf)
- [Layout](/pdf/a3010-sysclk-switcher-layout.pdf)
- [Gerber](https://github.com/dpicken/acorn-hw/raw/master/gerber/a3010-sysclk-switcher.zip)
- [BOM](/pdf/a3010-sysclk-switcher-bom.pdf)

A SPDT switch may be connected to the header and controls whether the overlock is enabled/disabled.  Its position is latched at power-up (i.e. toggling the switch after power-up is harmless).

- A 50 MHz oscillator will clock the ARM250 and RAM at 16 MHz (requires 60 ns RAM).
- A 60 MHz oscillator will clock the ARM250 and RAM at 20 MHz (requires 50 ns RAM).

# Assembly notes

Solder the front side first, starting with the oscillator (especially if using hot air).

# Installation

Fit a full can oscillator socket in X3, and, a 22 ohm resistor (or something close) in R76:

<a href="/doc/a3010-sysclk-switcher.md"><img src="/jpeg/a3010-sysclk-switcher-installation-1.jpeg" width="480"></a>

Install the module, with switch header toward the test connector:

<a href="/doc/a3010-sysclk-switcher.md"><img src="/jpeg/a3010-sysclk-switcher-installation-2.jpeg" width="480"></a>
