# macOS 12, Monterey on the B365M Mortar

![about](https://user-images.githubusercontent.com/73723350/160302049-f2fcfe32-2416-4443-98c5-26be6752f483.png)
![neofetch](https://user-images.githubusercontent.com/73723350/160302051-3b3fcd7b-af1c-45d2-ba55-1a2b0bb4dde0.png)

## notes
- use `HfsPlus.efi` instead of `OpenHfsPlus.efi`
- create your own USB map with USBToolBox in Windows
- `-v` can be removed after installation
- OpenCanopy GUI isn't provided
- everything is set as per the Configuration.pdf (0.7.9) by Acidanthera for CFL-based sysstems
- `config-iGPU.plist` only works with the integrated Intel UHD 630
- make your own SMBus SSDT (SBUS-MCHC) after install
- OpenCore version is **0.7.9**
- no Wi-Fi & Bluetooth Kexts included such as OpenIntelWireless
- the provided EFI is able to boot **macOS 11** or **12**

## hw used in this build

CPU: Intel Core i5-8400

MoBo: MSI-MAG B365M Mortar

GPU: Intel UHD 630 Graphics

RAM: G.Skill DDR4 16 Aegis 3000MHz running @ 2666 MHz

Wi-Fi/BT: fenvi T919

HDD: SanDisk SSD PLUS 120GB

## what is working

everything.

## what isn't working

-.

## BIOS settings & ver

udate to [7C67v143](https://download.msi.com/bos_exe/mb/7C67v143.zip)

lad the default settings

... and change the following:

- **Serial(COM) Port0** - Disabled
- **Parallel(LPT) Port** - Disabled
- **XHCI Hand-off** - Enabled
- **Initiate Graphic Adapter** - IGD *(only if you're using the iGPU, otherwise change it to PEG)
- **Integrated Graphics Share Memory** - 64MB *(also iGPU-only)*
- **Windows 10 WHQL Support** - UEFI
- **Intel VT-D Tech** - Enabled

**Repository will be improved very soon.**
