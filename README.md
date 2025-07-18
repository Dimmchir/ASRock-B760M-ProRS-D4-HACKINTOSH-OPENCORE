# ASRock-B760M-ProRS-D4-HACKINTOSH-OPENCORE
Hackintosh settings for ASRock-B760M-Pro RS/D4 Sequoia v.15.5 OpenCore 1.0.5
_________________________________
| Specifications | Detail                                                  |
| ------------------- | ------------------------------------------- |
| Motherboard | ASRock B760M Pro RS/D4 |
| Processor | 12th Gen Intel(R) Core Alder Lake i5-12400F |
| Discrete Graphics | AMD Radeon RX 6600 |
| Integrated Graphics | No |
| Sound chip | Realtek ALC897 (layout-id:12 (0C000000)) |
_________________________________

# What works : 
```
- Sound
- Boot-chime
- Sleep and wake
- Ethernet/Bluetooth
- Custom USB port mapping with USBToolBox
```
_________________________________
<img width="1399" height="1439" alt="Screenshot 2025-07-18 at 11 39 20" src="https://github.com/user-attachments/assets/a398945d-b470-4340-b01e-a508fd185f1f" />

# Warning!
Smbios serial numbers have been removed from Config.plist:
![PlatformInfo](https://github.com/user-attachments/assets/8737621c-39cc-4430-8997-d657643834f8)

You need to make your own Smbios. It is convenient to do this using the [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
_________________________________
When updating Mac OS, you must change the config.plist in the Misc/Security/SecureBootModel section to temporarily set the value to Disabled, otherwise there will be an endless reboot.

![Disabled](https://github.com/user-attachments/assets/8c9835c9-a4f5-444b-9333-03335fbacb4f)

After updating, you can return the value to Default in the Misc/Security/SecureBootModel section.
_________________________________
To edit config.plist it is better to use [ProperTree](https://github.com/corpnewt/ProperTree)
