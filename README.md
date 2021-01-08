# OpenCore-ROG-Strix-Z390-I

OpenCore config for ROG Strix Z390-I.

This config has been fully tested with OpenCore 0.6.4 on the following build:

* Intel Core i7-8086K
* G.SKILL 3200C16 16 GB * 2
* Samsung 970 EVO 512 GB
* ~AMD RX 6800 XT~ (disabled)
* Broadcom BCM943602CS

## How To Use

Pour these files into your OpenCore installation and add your own SMBIOS settings. See Appendix for required kexts.

## Note

### USB

Due to limitations to USB ports. Only these USB ports are enabled:

* Back
  * 1 USB 3.1 Gen 2
* Front
  * USB-A
  * USB-C
* Onboard
  * USB 2.0 (for AIO in my case)
* Other
  * 20703A1 Bluetooth Controller (on BCM943602CS, replacing M.2 NIC)
  * AURA Controller

![Back USB Port](https://user-images.githubusercontent.com/6648210/104071772-ce759c00-5244-11eb-8775-3e70366394fb.png)

> I modded my Phanteks Enthoo Evolv Shift (PH-ES217E) for front panel with USB-A, USB-C, audio ports. See [my post](https://elethom.me/en/2020/case-mod-phanteks-217e) for more info.

### GPU

This config works with my build by disabling unsupported discrete GPU. If you use a discrete GPU, change it accordingly.

## Appendix

### ACPI

* Fix EC & USB Power
* CPU Power Management
* NVRAM Support
* Fix System Clocks
* Disable Discrete GPU

### Kexts

* AppleALC
* IntelMausi
* Lilu
* NVMeFix
* USBMap
* VirtualSMC
* WhateverGreen

### Device Properties

* iGPU: `0x3e9b0000`
* Audio Layout: `1`

## Contact

This project is designed and developed by [Elethom Hunter](http://github.com/Elethom). You can reach me via:

* Email: elethomhunter@gmail.com
* Telegram: [@elethom](http://telegram.me/elethom)
