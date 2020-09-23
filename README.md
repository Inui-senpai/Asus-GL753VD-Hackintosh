# Asus-GL753VD-Hackintosh
Clover config and files for installing Hackintosh on ASUS GL753VD notebook (tested on ASUS FX753VD-GC256T (aka GL753VD))

Based on https://github.com/MohammadtaghiFarkhondekar/macOS-For-Asus-ROG-GL553VD

# Works:
* Boot
* Graphics acceleration (Intel HD Graphics 630)
* Battery
* All USB 2.0/3.0 Ports
* DVD RW Drive
* Wi-Fi
* Bluetooth
* Wired connection (Ethernet)
* Keyboard
* Hyper-Threading (Intel Core i7-7700HQ)
* Card Reader
* Web Camera
* Sound (not works if restarted from Windows)
* 3,5mm jack (see Notes)
* Storages (SSD 128 GB+SSD 120 GB+HDD 1 TB)
* Shutdown/Reset (without BIOS resetting)

# Not works:
* Touchpad
* Discrete video (NVIDIA GeForce GTX 1050)
* Keyboard lighting setting (I tried to compile my own firmware files according to https://github.com/hieplpvip/AsusSMC/wiki/Installation-Instruction, but I got an "AE_ALREADY_EXIST" error)
* Sleep (will never works on integrated video, at least according to ctich's message: https://4pda.ru/forum/index.php?s=&showtopic=84979&view=findpost&p=95445635)
* External storages (in external boxes)

# Not tested:
* HDMI connecting
* miniDisplayPort connecting
* USB-C connecting
* SMBIOS-dependent apps (iMessage, App Store, etc.)

# Notes:
* Sound from 3,5mm jack sounds too distorted, headphones are better connect through an external sound card.
* Sometimes graphic artifacts may appear, but it also happens on Windows 10 too.

Tested on macOS 10.15.6 Catalina. I do not guarantee that my config will works on macOS 11.0 Big Sur, at least at this moment of time.
