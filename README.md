# ASRock-B760M-ProRS-D4-HACKINTOSH-OPENCORE
Hackintosh settings for ASRock-B760M-Pro RS/D4 Sequoia v.15.5 OpenCore 1.0.5
_________________________________
| Specifications | Detail                                                  |
| ------------------- | ------------------------------------------- |
| Motherboard | ASRock B760M Pro RS/D4, BIOS v.10.03 |
| Processor | 12th Gen Intel(R) Core Alder Lake i5-12400F |
| Discrete Graphics | PowerColor AMD Radeon RX 6600 Fighter |
| Integrated Graphics | No |
| Sound chip | Realtek ALC897 (DeviceProperties/layout-id:12) |
_________________________________

# What works : 
```
- Sound
- Boot-chime
- Sleep and wake
- Ethernet
- Custom USB port mapping with USBToolBox
```
_________________________________

# Bugs : 
```
AMD (Navi 23) Graphics Cards had issue when booting using -v (verbose) boot-args,
you will face restart / black screen right after the verbose finished.
Sometimes it needs 2-3x times to boot into system.
Issue fixed by removing -v from boot-args
```
_________________________________
<img width="1420" height="1435" alt="Screen" src="https://github.com/user-attachments/assets/d0323225-9d53-4577-93b4-60035c180801" />


# Warning!
Smbios serial numbers have been removed from Config.plist:
<img width="1092" height="687" alt="Smbios serial numbers" src="https://github.com/user-attachments/assets/8db51eef-e8fa-41e5-8b23-7b4219d51e6a" />

You need to make your own Smbios. It is convenient to do this using the [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
_________________________________
When updating Mac OS, you must change the config.plist in the Misc/Security/SecureBootModel section to temporarily set the value to Disabled, otherwise there will be an endless reboot.

![Disabled](https://github.com/user-attachments/assets/8c9835c9-a4f5-444b-9333-03335fbacb4f)

After updating, you can return the value to Default in the Misc/Security/SecureBootModel section.
_________________________________
To edit config.plist it is better to use [ProperTree](https://github.com/corpnewt/ProperTree)
