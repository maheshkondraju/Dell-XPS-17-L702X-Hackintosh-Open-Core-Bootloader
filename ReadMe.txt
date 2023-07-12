There are couple of differences between USB EFI and SSD EFI. 

1. USB EFI SMBIOS is set to MacBookPro14,1 where as SSD EFI is set to MacBookPro8,3. This change is required, otherwise installation leads to an error "this update cannot be installed on this computer" where we cant select SSD Drive to install the OS, even after enabling boot arg -no_compat_check.

2. Advise Features quirk under Generic PlatformInfo is required during installation to fix the error "A Required Firmware Update Could Not Be Installed".

Open Core 0.9.3

Hello Everyone,

This release of Open Core 0.9.3 for Dell XPS 17 L702x is perfect, test and let me know if encountered any errors or problems.

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

Geekbench Single Core Score is 605 & Multi Score is 2063 for Core i7 2630QM processor.
