# MacOS Big Sur and Catalina (10.15 - 11.7.6) successfully achieved on an Intel i5-9600k and Z390X

![schreibtisch](https://github.com/DevGhali/Hackintosh-Z390X-i59600k-OpenCore-EFI/assets/113459534/65796d37-ac41-4208-a925-a21d77fe5d4a)


## Specs ⚙️

| **Component**   | **Model**                       |
| --------------- |---------------------------------|
| CPU             | Intel i5-9600K (6) @ 3.70GHz    |
| Motherboard     | GIGABYTE Z390 GAMING X rev1.0   |
| RAM             | 16GB (2x 8GB) CORSAIR @ 3200MHz (3400MHz WITH XMP)|
| Audio Chipset   | Realtek® ALC892                 |
| GPU             | IGPU - Intel UHD Graphics 630 2048 MB  |
| OS Disk (SATA SSD) | SANDISK SSD PLUS 240GB                  |

* OpenCore: 0.6.3
* macOS: Big Sur 11.7.6 and Catalina 10.15 both worked well

## Important stuff to bear in mind 🧠

* in order to achieve Big Sur you need to install Catalina first then upgrade from the os itself, for some reason installing Big Sur directly didnt work for me
* it is configured to use the iGPU only, if you have a graphics card that you would like to use please make the required changes, the "GPU_DISABLE" SSDT should be removed
* SMBIOS isnt fully configured, things such as the serial number and UUID need to be changed

## BIOS Settings 🛠 - Required for inatallation and to run the OS 

| **Setting**     | **Enabled/Disabled**                       |
| --------------- |---------------------------------|
| Internal Graphics            | Enabled     |
| Vtd     | Disabled   |
| Above 4G encoding             | Enabled |
| XCHI handoff  | Enabled                 |
| SATA Configuration             | ACHI  |
| CSM | Disabled                  |
| Secure boot | Disabled                  |
| Windows 8/10 featured | Other OS                 |
| CGF lock | Disabled                  |


## Guide 🗡
<img width="250" height="250" align="right" src="https://dortania.github.io/OpenCore-Install-Guide/dortania-logo-clear.png"/>
<h3> This is the most important part which requires patience and dedication upon not succeding you can always search the internet, ask on reddit or easily HMU and i would be more than happy to help! 😊</h3>
<h3> If you have the same specs you can skip the part of making the EFI folder and just use mine as well as the BIOS configuration BUT if it doesnt work for some reason you'd need to build your own EFI afterall </h3>
<h3> If my EFI worked for you congrats! 🥳 you'd only need to Generate SMBIOS and sort the serial number stuff</h3>

-  [Dortania's OpenCore installation Guide](https://dortania.github.io/OpenCore-Install-Guide/)

-  [SMBIOS Guide](https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html)

## Whats working and whats not ✅ ❌

<h3>Working</h3>

* USB Ports 2.0 and 3.0
* Audio all ports working + over HDMI
* Ethernet
* Shutdown & Restart
* Wifi and Bluetooth haven't tested yet beacause i need an adapter from mini pcie to pcie but im pretty sure an intel AC3160 would work, tested from previous hackintosh builds (kexts are included in the EFI)
* icloud, imessage and facetime worked after configuing the SMBIOS and adding a valid serial number
* Downloading apps from AppStore and Apple-id work just fine 

<h3>Not Working</h3>

* Sleep works but on wake the screen stays black to get screen output the hdmi needs to be taken out and put back in

<h1>Happy Hackintoshing! 🤩 </h1>
