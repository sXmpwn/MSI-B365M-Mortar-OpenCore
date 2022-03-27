# Hackintosh-MSI-B365M-Mortar
![About](https://user-images.githubusercontent.com/73723350/160297595-05fc8983-3993-4574-978a-a212bafc1721.png)

Notes:
- use HfsPlus instead of OpenHfsPlus
- create your own USB map with USBToolBox in Windows
- -v can be removed after installation
- GUI isn't provided
- config-iGPU.plist only works with the integrated Intel UHD 630
- OpenCore version is 0.7.9
- no Wi-Fi & Bluetooth Kexts included such as OpenIntelWireless
- the EFI is able to boot macOS 11 or 12

My hardware used in this build:

CPU: Intel Core i5-8400

MoBo: MSI-MAG B365M Mortar

GPU: Intel UHD 630 Graphics

RAM: G.Skill DDR4 Aegis 3000 MHz running @ 2666 MHz

Wi-Fi/BT: fenvi T919

HDD: SanDisk SSD PLUS 120GB

What is working:

everything.

What isn't working:

-.

BIOS Version and settings

Update to E7C67IMS.143

Load the default settings

... and change the following:

- Serial(COM) Port0 --> Disabled
- 
- Parallel(LPT) Port --> Disabled
- 
- XHCI Hand-off --> Enabled
- 
- Initiate Graphic Adapter --> IGD (only if you're using the iGPU, otherwise change it to PEG)
- 
- Integrated Graphics Share Memory --> 64MB (also iGPU-only)
- 
- Windows 10 WHQL Support --> UEFI
- 
- Intel VT-D Tech --> Enabled

Repository will be improved very soon.
