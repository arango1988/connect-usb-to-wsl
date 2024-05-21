# How to connect a USB device to WSL

## Description
This repository is for personal use, helping me remember how to connect and test a USB device with WSL. It provides step-by-step guides, configurations, and troubleshooting tips to integrate USB functionality within WSL. Ideal for developers and tech enthusiasts using USB devices in their Linux workflows on Windows

## Steps
Follow steps at: https://learn.microsoft.com/en-us/windows/wsl/connect-usb

Using CMD run: `usbipd list`

This will list all USB devices connected. You should see something like:
```
Connected:
Copy code
BUSID  VID:PID    DEVICE                                                        STATE
1-2    0403:6001  USB Serial Converter                                          Attached
4-1    13d3:56c9  HP TrueVision HD Camera                                       Not shared
4-3    0bda:b00a  Realtek Bluetooth 4.2 Adapter                                 Not shared
```

Take the busid of the USB device you need to work on and attach it to WSL (-w = wsl):
`usbipd attach -w --busid 1-2`
