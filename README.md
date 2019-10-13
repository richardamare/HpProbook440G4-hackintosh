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
### USB installer
