# pcb-faves-kicad

KiCad is awesome. It's really high quality software, and I've been learning a lot about the back end side of hardware design. Front end circuit design is looking at optimized logic, design, etc. Back end is full of things like noise prevention and signal integrity.

I come up with some circuits to design every now and then for fun. This repo is just a collection of the PCBs I've designed. I'll add a text file to describe each pcb later on.

I should add that I haven't printed anything yet since I don't have access to PCB printers right now. So I'm just using typical values for clearance and trace width and stuff, not pushing anything. I keep things at 2 or 4 layers.

# Designs summary

Descriptions of each design in this repo for reference.

1. [usb-demux](#usb-demux)

More coming soon!

## usb-demux

[Schematic](usbdemux-sch.pdf)

[PCB](usbdemux-pcb.pdf)

When I work with microcontrollers and FPGAs, I encounter several issues. First, I have only one USB-C port on my laptop capable of delivering sufficient power, so I need to use a USB-C to USB-A converter before connecting any USB-A cable or pen drive. Second, to flash a device, I can only connect that specific device to my laptop, without any multiport hubs. So if I want to use two devices, I have to keep connecting and disconnecting.

This device is a 4 layer PCB that plugs directly into my laptop without a converter and allows me to use switches to control which of 4 USB ports my laptop is connected to. This way, all my devices are physically wired, but only one is communicating with my laptop at a time. The device has 1 USB-C and 3 USB-A receptacles and uses USB 2.0 communication due to greater applicability.

There are also 2 additional features in this PCB. The first is a set of header pins providing 5V and GND. This allows me to power a breadboard if I'm building any circuitry to interact with my microcontrollers or FPGAs. To prevent my laptop battery from draining or overheating, I added a 9V battery supply with a switching regulator to provide 5V to all the devices in place of my laptop.
