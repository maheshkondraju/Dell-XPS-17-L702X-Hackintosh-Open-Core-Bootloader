Open Core 1.0.0 for Dell XPS 17 L702x.

Changelog:

There are couple of differences between USB EFI and SSD EFI. 

1. USB EFI SMBIOS is set to MacBookPro14,1 where as SSD EFI is set to MacBookPro8,3. This change is required, otherwise installation leads to an error "this update cannot be installed on this computer" where we cant select SSD Drive to install the OS, even after enabling boot arg -no_compat_check.

2. Advise Features quirk under Generic PlatformInfo is required during installation to fix the error "A Required Firmware Update Could Not Be Installed".

This release of Open Core 1.0.0 for Dell XPS 17 L702x is perfect, test and let me know if encountered any errors or problems.

Lots of hardwork has gone in to this release.

Includes FakeSMC along with ACPIMonitor.kext & IntelCPUMonitor.kext instead of VirtualSMC for better sensor support, especially for monitoring CPU speed stepping C states & Turbo P states.

Includes DSDT.aml for better CPU heat Management, temps of the cpu cores idle around 48 c.

Includes Patched ASPP-Override.kext, AppleIntelCPUPowerManagement.kext & AppleIntelCPUPowerManagementClient.kext for SandyBridge Processors for Turbo P states management.

Includes Patched CPUFriend.kext & CPUFriendDataProvider.kext for SandyBridge Processors for CPU speed stepping C states & Turbo P states management.

Audio has been recognized and working properly.

Intel WiFi works.

Fn + Brightness Keys works for increasing & Decreasing brightness.

Realtek Gigabit Ethernet Controller is working.

GenericUSBXHCI.kext has been included for Renesas USB 3.0.

CryptexFixup.kext has been included to support booting of Ventura.

VoodooPS2Controller.kext has been included to work with Synaptics Trackpad.

Config is completely re-written using Open Core Configurator.

All hardware details has been added under DeviceProperties.

Intel HD 3000 Graphical Artifacts are gone by enabling Open Legacy Patcher "enable blur feature".

![0XQB4kX](https://github.com/maheshkondraju/Dell-XPS-17-L702X-Hackintosh-Open-Core-Bootloader/assets/36487164/ebe6b37e-3e93-4887-9e19-967adfe6d73f)
![SzSQ2aD](https://github.com/maheshkondraju/Dell-XPS-17-L702X-Hackintosh-Open-Core-Bootloader/assets/36487164/d5ab2262-d6f6-42ea-9e84-31a152417ef5)
![vXSGz3V](https://github.com/maheshkondraju/Dell-XPS-17-L702X-Hackintosh-Open-Core-Bootloader/assets/36487164/8952af8e-9ba5-453f-bf8f-bd4f465837eb)
