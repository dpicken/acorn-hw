# USB Mouse

A USB mouse -> quadrature mouse adapter, based on [WeeMouse](https://github.com/IJeffray/WeeMouse) and [Atari-Quadrature-USB-Mouse-Adapter](https://github.com/jjmz/Atari-Quadrature-USB-Mouse-Adapter).

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse.jpeg" width="480"></a>

- [Schematic](/pdf/usb-mouse-schematic.pdf)
- [Layout](/pdf/usb-mouse-layout.pdf)
- [Gerber](https://github.com/dpicken/acorn-hw/raw/master/gerber/usb-mouse.zip)
- [BOM](/pdf/usb-mouse-bom.pdf)

# Assembly notes

Solder capacitors, IC and USB socket:

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse-rear.jpeg" width="480"></a>

Tin cables, then solder to the board:

| Signal  | PCB | Acorn Mouse |
|---------|-----|-------------|
| 5V      |  1  |   6         |
| GND     |  2  |   4         |
| X2      |  3  |   1         |
| X1      |  4  |   5         |
| Y1      |  5  |   9         |
| Y2      |  6  |   7         |
| ButtonM |  7  |   3         |
| ButtonR |  8  |   8         |
| ButtonL |  9  |   2         |

Acorn mouse socket:

      /-----------\
     /             \
    | 9   8      7  |
    | 6   5   4   3 |
     \    2   1    /
      \-----------/

Use a zip tie and hot glue to provide strain relief:

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse-zip-tie.jpeg" width="480"></a>

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse-hot-glue.jpeg" width="480"></a>

To flash firmware, short JP1 whilst connecting USB to a Linux host, then:

    git clone https://github.com/ch32-rs/wchisp.git
    git clone https://github.com/IJeffray/WeeMouse.git
    cd wchisp
    cargo build --release
    sudo ./target/release/wchisp flash ../WeeMouse/Generated/firmware.bin

Heat shrink:

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse-heat-shrink.jpeg" width="480"></a>

Plug and play:

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse-plug.jpeg" width="480"></a>

<a href="/doc/usb-mouse.md"><img src="/jpeg/usb-mouse-play.jpeg" width="480"></a>

