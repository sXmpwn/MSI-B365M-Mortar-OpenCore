# macOS 12, Monterey on the B365M Mortar
![About](https://user-images.githubusercontent.com/73723350/160298482-352045e2-09d6-4b0d-9504-7722e58323c0.png)
![MoBo](https://user-images.githubusercontent.com/73723350/160301389-3796d74d-dcc5-4d3c-98c8-20e72d44c5f4.png)


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

RAM: G.Skill DDR4 Aegis 3000 MHz running @ 2666 MHz

Wi-Fi/BT: fenvi T919

HDD: SanDisk SSD PLUS 120GB

## what is working

everything.

## what isn't working:

-.

## BIOS settings & ver

Update to **E7C67IMS.143**

Load the default settings

... and change the following:

- **Serial(COM) Port0** - Disabled
- **Parallel(LPT) Port** - Disabled
- **XHCI Hand-off** - Enabled
- **Initiate Graphic Adapter** - IGD *(only if you're using the iGPU, otherwise change it to PEG)
- **Integrated Graphics Share Memory** - 64MB *(also iGPU-only)*
- **Windows 10 WHQL Support** - UEFI
- **Intel VT-D Tech** - Enabled

**Repository will be improved very soon.**
