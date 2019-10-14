# HP Probook 440 G4 Hackintosh
This is the guide to install macOS on the HP Probook 440 G4.
## My Laptop Configuration:
- CPU: i5-7200U
- RAM: 16GB
- GPU: Nvidia 930MX / Intel HD 620
- WIFI: Broadcom BCM94352Z DW1560
- Drives: 128GB M.2 SSD & 1TB HDD (Windows), 120GB (External SSD for hackintosh)
- FHD Display
## What works:
- Wifi
- Bluetooth
- Intel HD 620 Graphics Acceleration
- Brightness
- Sleep
- Audio via AppleALC
- Keyboard with Volume Controls and Brightness controls
- Power Management with percentage
- Trackpad
## What doesn't work:
- Nvidia GPU (not supported)
- Fingerprint sensor
- Camera (I changed SMBIOS from 14,1 to 15,4 camera doesn't work, but audio started to work properly)
## Let's Get Started
### Prepare:
- HP Probook 440 G4
- macOS Mojave downloaded from the App Store
- atleast 8GB USB stick
- USB Wifi adapter or LAN cable
### Bios:
- open F10
- boot menu F9
- disabled Secure Boot
- disabled VT-d
- enabled VTx
### USB installer:
- connect USB stick to device running macOS (Mac or Hackintosh)
- open Disk Utility - format USB as Mac OS Extended (Journaled) and rename it to USB
- download [MacOS Mojave from the Apple App Store](https://apps.apple.com/us/app/macos-mojave/id1398502828?mt=12)
- after download open terminal and paste:
```
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/USB
```
- it should take up to 30 minutes
- when its done download [Clover Bootloader](https://sourceforge.net/projects/cloverefiboot/)
- mount EFI partition in [Clover Configurator](https://www.tonymacx86.com/resources/clover-configurator.429/)
- then download [my EFI Folder](./EFI.zip)
- replace my [EFI](./EFI.zip) with original EFI on EFI partition
### Installation
- turn on laptop and start pressing F9 key (it opens boot menu)
- select your USB stick and wait for it to boot
- select Install macOS... (use arrows and enter)
- after boot select Disk Utility
- in left corner click on "view" and select "Show All Devices"
- select your drive for hackintosh
- format it as "APFS", scheme "GUID Partition Map"
- close Disk Utility and go to Install MacOS, select your drive and continue..
- when your laptop restarts be sure it boots to your USB stick
- continue the installation
- after instalation completed, configure hackintosh setting for your need
### Post Instalation
- download [Clover Bootloader](https://sourceforge.net/projects/cloverefiboot/) and install it for UEFI booting only
- [go here and folow instruction](https://www.tonymacx86.com/threads/guide-hp-probook-elitebook-zbook-using-clover-uefi-hotpatch.261719/) (if it will show to enter the password over and over, then try to add before the command - sudo)
- after completing previous point download my EFI folder
- go to [Clover Configurator](https://www.tonymacx86.com/resources/clover-configurator.429/) and mount EFI partition on current boot disk
- replace EFI with my [EFI](./EFI.zip)
- reboot your laptop 

Now everything should be working

Enjoy your new hackintosh
