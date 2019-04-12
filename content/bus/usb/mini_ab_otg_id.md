title: 'Host and device identification in USB mini OTG'
categories:
  - Bus
    - USB
tags: ['USB', 'OTG', 'ID', 'Host', 'device', 'GND']
description: 'Introduces USB mini AB pinout and explains how the extra ID pin decides Host or Device role'
draft: true
+++

## Ports
## Conventional ports
Generally USB has two types of ports:
- Type A
- Type B

Type A ports are found on USB host units. Type B ports are found on USB device units.
This prevents the user from connecting two USB hosts together (which is electrically
  not safe).

### OTG ports
OTG enabled units have special type of USB port with the designation AB.
- USB mini AB
- USB micro AB

These AB ports are mechanically designed to accept both Type A and Type B plugs/units
into the OTG enabled units.

There is one problem in connecting two USB OTG units together. Both can act as hosts
when connected and this is not electrically safe. So, initially when two USB OTG units are
connected through USB OTG cable there must be a mechanism to ask one unit to start as
USB host and the other as USB device. The roles can later be changed using HNP protocol.

## Identification
USB OTG plugs have an extra pin called ID. This pin is used to detect if the connected
USB OTG unit would like to act as host or device by default.

If the ID pin in the USB OTG cable reads GND, that unit shall act as USB host.
If the ID pin in the USB OTG cable is floating, that unit shall act as USB device.

Plug on one side of the USB OTG cable has the ID pin grounded and the other plug
has the ID pin floating.
