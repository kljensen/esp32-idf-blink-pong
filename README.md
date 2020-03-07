# Blink pong

Making two esp32 boards play blinking LED pong. This is basically
a combo of the ESP-IDF examples "espnow" and "blink".

## Instructions

First, install the ESP-IDF sdk following [this guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/)

I'm using the [MELIFE ESP32 boards](https://www.amazon.com/MELIFE-Development-Dual-Mode-Microcontroller-Integrated/dp/B07Q576VWZ)
which you can buy in a two-pack on Amazon. The male pins are sodered on, which is uncool.

The built-in LED to GPIO2.

On my mac, the devices show up as `/dev/cu.SLAB_USBtoUART`. Yours may show up as something different.

### Build

Choose a path for your esp-idf. Mine is
`/Users/kljensen/src/github.com/espressif/esp-idf`.
Then,

```
export IDF_PATH=$HOME/src/github.com/espressif/esp-idf
git clone -b v4.0 --recursive https://github.com/espressif/esp-idf.git $IDF_PATH
. $IDF_PATH/export.sh
```

Notice this will do fancy stuff like create a python
environment for your development. See
[the guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/)
for customizing or avoiding this behavior.

### Flash

Assuming you have done

```
export IDF_PATH=$HOME/src/github.com/espressif/esp-idf
. $IDF_PATH/export.sh
```

Then you'd do

```
idf.py -p /dev/cu.SLAB_USBtoUART flash
```

You can monitor the serial output with

```
idf.py -p /dev/cu.SLAB_USBtoUART monitor
```

Quit this program with `^[`: that is, `control` and `[`).
