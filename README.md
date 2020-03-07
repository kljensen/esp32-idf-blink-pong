# Blink pong

Making two esp32 boards play blinking LED pong.

## Instructions

First, install the ESP-IDF sdk following [this guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/)

I'm using the [MELIFE ESP32 boards](https://www.amazon.com/MELIFE-Development-Dual-Mode-Microcontroller-Integrated/dp/B07Q576VWZ)
which you can buy in a two-pack on Amazon. The male pins are sodered on, which is uncool.

The built-in LED to GPIO2.

On my mac, the devices show up as `/dev/cu.SLAB_USBtoUART`. Yours may show up as something different.

Flash
```
idf.py -p /dev/cu.SLAB_USBtoUART flash
```
