# OpenCore hackintosh EFI for Lenovo IdeaPad 5 15IIL05

This EFI supports running macOS Big Sur throught Tahoe using the OpenCore bootloader. It is still in development, so expect bugs and various other issues to appear here and there. I only tested it on my 87K laptop, and it may not work properly on variants of this model with older or newer CPUs for example.
Thus I would greatly appreciate your contributions & bug reports in order to improve and optimize it.

*If you like my work, consider starring this repo and taking a look at my other projets ❤️*

## Specifications/Specs 
![About This Mac](assets/About_This_Mac.png)

|Component|Details|
|---|---|
|**CPU**|**Intel(R) Core(TM) i5-1035G1 CPU @ 1.00GHz**|
|**RAM**|**8G DDR4 3200MHz**|
|**iGPU**|**Intel(R) UHD G1 Graphics 4095MB VRAM**|
|**SSD**|**UMIS RPJTJ512MEE1OWX 512GB NVMe PCIe**|
|**WIFI**|**Intel Wi‑Fi 6 AX201 160MHz + Bluetooth 5**|
|**Audio**|**Realtek ALC257**|
|**Ports**|**2xUSB3.0, 1xUSB3.0 Type-C, HDMI, SD card reader, Headphone Jack, and DC charging port**|
|**Fingerprint**|**ELAN fingerprint sensor**|
|**Webcam**|**Integrated 720p HD webcam**|
|**OpenCore**|**2.4.1**|

## Things not working
+ HDMI does not work at all. this is a commun problem on Ice Lake iGPUs that cannot be corrected.
+ the ELAN fingerprint sensor (these cannot work on a hackintosh because of Apple security policies)
+ hibernation is buggy and should be disabled (can cause high CPU usage after wake because of BT driver problems)
 
## Things Working
+ the UHD G1 iGPU works perfectly with Metal 3 hardware acceleration support & the full 4GB of VRAM working.
+ Sound works via AppleALC.kext with layout_id=11
+ trackpad & keyboard work throught different Voodoo kexts.
+ all ports (except HDMI) works thank's to USBTMap.kext mapping.
+ Wifi works throught Airport & heliport, and Blutooth works correclty.
+ everything else works (Webcam, SSD...)

## How to install


