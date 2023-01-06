There are couple of differences between USB EFI and SSD EFI. 

1. USB EFI SMBIOS is set to MacBookPro14,1 where as SSD EFI is set to MacBookPro8,3. This change is required, otherwise installation leads to an error "this update cannot be installed on this computer" where we cant select SSD Drive to install the OS, even after enabling boot arg -no_compat_check.

2. Advise Features quirk under Generic PlatformInfo is required during installation to fix the error "A Required Firmware Update Could Not Be Installed".
