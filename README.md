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
  * [02,05,06] 1 USB 3.1 Gen 1 Type-C
  * [04] 1 USB 3.1 Gen 2 Type-A
* Front
  * [01, 02] 1 USB 3.1 Gen 2 Type-C (U31G2_C1 Type-E connector)
  * [10] 1 USB 3.1 Gen 1 Type-A (U31G1_910 20-1 pin connector)
* Onboard
  * [12] USB 2.0 (for AIO in my case)
* Other
  * [13] AURA Controller
  * [14] 20703A1 Bluetooth Controller (on BCM943602CS, replacing M.2 NIC)

![Back USB Port](https://user-images.githubusercontent.com/6648210/104654365-ec387a80-56f6-11eb-8cf8-f10bc64b1f44.png)

> Complaints regarding the choice of USB ports will be ignored because I don't give a fuck. Go change them yourself if you don't like it. Good day, sir.

> I modded my Phanteks Enthoo Evolv Shift (PH-ES217E) for front panel with USB-A, USB-C, audio ports. See [my post](https://elethom.me/en/2020/case-mod-phanteks-217e) for more info.

### GPU

This config works with my build by disabling unsupported discrete GPU. If you use a discrete GPU, change it accordingly.

> DRM does not work with iGPU. I plan to wait a few months for macOS to support RDNA 2.

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
