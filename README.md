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

# UEFI Settings:
* Go to Advanced Mode (F7)
* In Advanced tab:
1. Internal Pointing Device - Enabled;
2. Wake On Lid Open - Enabled;
3. Intel Virtualization Technology - **Enabled**;
4. Intel AES-NI - Enabled;
5. VT-d - **Enabled**
* In USB Configuration section of Advanced tab:
1. Legacy USB Support - **Enabled** (it's necessary for booting from USB drive prepared via BootDiskUtility);
2. USB Mass Storage Driver Support - Enabled
* In Graphics Configuration section of Advanced tab:
1. DVMT Pre-Allocated: **64MB**
* In SATA Configuration section of Advanced tab:
1. SATA Mode Selection: **AHCI**
* In Boot tab:
1. CSM Support - **Disabled**;
2. Launch PXE OpROM policy - Disabled;
3. Boot Option Priorities - Leave it as is, you can boot from USB drive via Boot Menu (press Esc during splashscreen)
* In Security tab:
1. Go to Secure Boot section;
2. Secure Boot Mode - **Disabled** (both Clover and OpenCore uses unsigned bootx64.efi, not sure about the latter, though)
* In Save & Exit tab:
1. Select Save Changes and Exit and then confirm saving and rebooting in the modal window

# Notes:
* You can surf the Internet and watch videos on WLAN connection, but uploading/downloading files and streaming will be pain in the ass.
* Sound from 3,5mm jack sounds too distorted, headphones are better connect through an external sound card.
* Internal speakers will not works if you restarted in macOS from Windows; also sound from it sounds too flat (possibly because of nonworking auxiliary ICESound audio card).
* Sometimes graphic artifacts may appear, but it also occur on preinstalled Windows 10 Home SL (after reinstalling Windows I didn't see any graphic artifacts).
* Airplane Mode indicator will always turned on regardless of current Airplane Mode state on real system (seems like ACPI bug).
* After installing, macOS creates the hidden boot entry named "Mac OS X". If you're going to reinstall the macOS, remove this entry through x64-version of BootICE in advance, otherwise you won't be able to boot into Setup Utility.

Tested on macOS 10.15.7 Catalina. I do not guarantee that my config will works on macOS 11.0 Big Sur, at least at this moment of time.
