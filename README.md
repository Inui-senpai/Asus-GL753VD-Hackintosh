# Asus-GL753VD-Hackintosh
Clover config and files for installing Hackintosh on ASUS GL753VD notebook (tested on ASUS FX753VD-GC256T (aka GL753VD))

Based on https://github.com/MohammadtaghiFarkhondekar/macOS-For-Asus-ROG-GL553VD

# Works:
* Boot
* Graphics acceleration (Intel HD Graphics 630)
* Battery
* USB 2.0/3.0 Ports (except one USB 3.0 port on the right side)
* DVD RW Drive
* Touchpad (may not work after first startup)
* Bluetooth
* Wired connection (Ethernet)
* Keyboard
* Hyper-Threading (Intel Core i7-7700HQ)
* Card Reader
* Sound (not works if restarted from Windows)
* Storages (SSD 128 GB+HDD 1 TB)
* Shutdown/Reset (without BIOS resetting)

# Not works:
* Wi-Fi (but it's a matter of time)
* Discrete video (NVIDIA GeForce GTX 1050)
* Keyboard lighting setting (I tried to compile my own firmware files according to https://github.com/hieplpvip/AsusSMC/wiki/Installation-Instruction, but I got an "AE_ALREADY_EXIST" error)
* Sleep (will never works on integrated video)

# Not tested:
* HDMI connecting
* miniDisplayPort connecting
* USB-C connecting
* 3,5mm jack connecting

Tested on macOS 10.14.5 Mojave (but this may also works on newer versions of macOS)
