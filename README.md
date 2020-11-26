# Asus-GL753VD-Hackintosh
Clover config and files for installing Hackintosh on ASUS GL753VD notebook (tested on ASUS FX753VD-GC256T (aka GL753VD))

Based on https://github.com/MohammadtaghiFarkhondekar/macOS-For-Asus-ROG-GL553VD

# Works:
* Boot
* Graphics acceleration (Intel HD Graphics 630)
* Battery
* All USB 2.0/3.0 Ports
* DVD RW Drive
* Wi-Fi (see Notes)
* Bluetooth
* Wired connection (Ethernet)
* Keyboard
* Hyper-Threading (Intel Core i7-7700HQ)
* Card Reader
* Web Camera
* Sound (see Notes)
* 3,5mm jack (see Notes)
* Storages (only SATA)
* Shutdown/Reset (without BIOS resetting)

# Not works:
* Touchpad (it may works after installing VoodooI2CELAN.kext)
* Discrete video (NVIDIA GeForce GTX 1050)
* Keyboard lighting setting (I tried to compile my own firmware files according to https://github.com/hieplpvip/AsusSMC/wiki/Installation-Instruction, but I got an "AE_ALREADY_EXIST" error)
* Sleep (will never works on integrated video, at least according to ctich's message: https://4pda.ru/forum/index.php?s=&showtopic=84979&view=findpost&p=95445635)
* Storages in external boxes, connected through USB
* Many other Fn keys

# Not tested:
* HDMI connecting
* miniDisplayPort connecting
* USB-C connecting
* SMBIOS-dependent apps (iMessage, App Store, etc.)

# Notes:
* You can surf the Internet and watch videos on WLAN connection, but uploading/downloading files and streaming will be pain in the ass.
* Sound from 3,5mm jack sounds too distorted, headphones are better connect through an external sound card.
* Internal speakers will not works if you restarted in macOS from Windows; also sound from it sounds too flat (possibly because of nonworking auxiliary ICESound audio card).
* Sometimes graphic artifacts may appear, but it also occur on preinstalled Windows 10 Home SL (after reinstalling Windows I didn't see any graphic artifacts).
* Airplane Mode indicator will always turned on regardless of current Airplane Mode state on real system (seems like ACPI bug).

Tested on macOS 10.15.7 Catalina. I do not guarantee that my config will works on macOS 11.0 Big Sur, at least at this moment of time.
