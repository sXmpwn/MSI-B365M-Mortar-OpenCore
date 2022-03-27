# macOS 12, Monterey on the B365M Mortar

![about](https://user-images.githubusercontent.com/73723350/160302049-f2fcfe32-2416-4443-98c5-26be6752f483.png)
![neofetch](https://user-images.githubusercontent.com/73723350/160302051-3b3fcd7b-af1c-45d2-ba55-1a2b0bb4dde0.png)

**the provided EFI is only a sample for this build, it boots but I highly recommend to build your own EFI so you'll learn about things & how they work, head to the** [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## notes
- use `HfsPlus.efi` instead of `OpenHfsPlus.efi`
- create your own USB map with [USBToolBox](https://github.com/USBToolBox) in Windows
- `-v` (stands for Verbose) can be removed after installation
- OpenCanopy GUI isn't provided to keep it lightweight
- everything is set as per the [Configuration.pdf (0.7.9)](https://github.com/ad422/OSx86-MSI-B365M-Mortar/blob/main/Configuration.pdf) by Acidanthera for CFL-based sysstems
- `config-iGPU.plist` only works with the integrated Intel UHD 630
- [make your own](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus-methods/manual.html) SMBus SSDT (SBUS-MCHC) after install
- generate a `iMac19,1` SMBIOS using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
- OpenCore version is **0.7.9**
- no Wi-Fi & Bluetooth Kexts included such as [OpenIntelWireless](https://openintelwireless.github.io/)
- the provided EFI is able to boot **macOS 11** or **12**
- the propertry list must be named `config.plist`
- only use [ProperTree](https://github.com/corpnewt/ProperTree) to edit plist files, avoid configurators like OCAuxiliary, Clover & OC Configurator
- the SSDT's are prebuilts by Acidanthera, however I recommend to use [SSDTTime](https://github.com/corpnewt/SSDTTime) to generate them or the manual way (as the prebuilts are kinda bloated)

## hw used in this build

CPU: **Intel Core i5-8400**

MoBo: **MSI-MAG B365M Mortar**

GPU: **Intel UHD 630 Graphics**

RAM: **G.Skill DDR4 16 Aegis 3000MHz** running @ 2666 MHz

Wi-Fi/BT: **fenvi T919**

HDD: **SanDisk SSD PLUS 120GB**

## what is working

|Features|Status|Additional details|
|:-|:-|:-|
|Sound| :thumbsup: |with layout-id 1|
|USB Ports| :thumbsup: |mapped|
|Wi-Fi| :thumbsup: |via T919|
|Bluetooth| :thumbsup: |via T919|
|AirDrop/Handoff| :thumbsup: |both directions work|
|Universal Control| :thumbsup: |tested with iPad Pro 2016 & iPad 2018|
|Ethernet| :thumbsup: |-|
|Unlock with Apple Watch| :thumbsup: |with a AW Series 3|
|Graphics acceleration (iGPU)| :thumbsup: |connected to the single HDMI port|
|Sidecar| :thumbsup: |tested with iPad Pro 2016 & iPad 2018, wireless + lightning|
|Restart/Shutdown| :thumbsup: |-|
|Sleep| :thumbsup: |(iGPU-only) to also wake up the monitor you'll have to use the boot-arg `igfxonln=1` |
|CPU power management| :thumbsup: |X86PlatformPlugin is loaded in IOReg|
|iServices| :thumbsup: |requires generated Apple ROM|
|DRM| :thumbsup:| Apple TV doesn't work, Netflix plays on Chromium |

## what isn't working

nothing.

## BIOS settings & ver

update to [7C67v143](https://download.msi.com/bos_exe/mb/7C67v143.zip) (latest beta as of end-march)

load the default settings;

... and change the following:

- **Serial(COM) Port0** - Disabled
- **Parallel(LPT) Port** - Disabled
- **XHCI Hand-off** - Enabled
- **Initiate Graphic Adapter** - IGD *(only if you're using the iGPU, otherwise change it to PEG)
- **Integrated Graphics Share Memory** - 64MB *(also iGPU-only)*
- **Windows 10 WHQL Support** - UEFI
- **Intel VT-D Tech** - Enabled

## credits

- [Dortania](https://github.com/dortania) for the guide
- [CorpNewt](https://github.com/corpnewt) for (especially ProperTree) & too many things to mention each and our great conversations on the dc server
- [Acidanthera](https://github.com/acidanthera) for too many things to mention each
- [RehabMan](https://github.com/RehabMan) for too many things to mention each
- [OpenCore project](https://github.com/OpenCorePkg) for the bootloader
- [Dhinak G](https://github.com/dhinakg) for USBToolBox

greetings

⁓ sXmpwn
