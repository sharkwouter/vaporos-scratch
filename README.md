# VaporOS

SteamOS is an operating system which can turn a computer into a game console. VaporOS improves on this by not only focussing on games, but also offer multimedia and emulation support along with some other extras to make the system more enjoyable to use.

## Features

VaporOS contains all the features found in SteamOS plus the following additions:

- **Retroarch**, an emulator  frontend with support for PSP, PS1, N64, SNES, NES, GBA and more
- **Kodi**, an entertainment center which can play videos and music
- **VaporOS-FTPServer**, a file server which allows you to easily transfer files
- **VaporOS Flatpak Manager**, a front-end for flatpak. It allows for easy software installation
- **Improved desktop experience** with a text editor, archive manager, media player (**VLC**) and **Gnome Tweak Tool** added
- **Bash completion** for command line users
- **TRIM support** for SSDs

## Download

Download the latest Vaporos release [here](https://github.com/sharkwouter/vaporos/releases).

## Installation

VaporOS can be installed from a DVD or from a USB stick. To be able to do so, the latest VaporOS ISO (vaporos-XXX.iso) has to be downloaded like mentioned above. Burning the ISO to a DVD can be done with any DVD burning program like Imgburn. Instructions on how to use a USB stick will be listed below. A USB stick of at least 2 GB will be required for this.

After having made the installation media (DVD or USB stick), installing from it is pretty straight forward. Put the installation media in the computer and press F8, F9, F11 or F12 during boot to open the boot menu and pick it. Which of these buttons works depends on the hardware and might take some trial and error. After that pick the option "Automated installation" (**this will erase your disk!**) and wait for the installation to finish. The system will reboot multiple times during installation. Once finished select the reboot option and press enter. You are now ready to use VaporOS.

### Installing from USB (Windows)

Download the tool [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/) and use it to copy the VaporOS ISO to your USB stick. **This erases all data on the USB stick!!**

### Installing from USB (Mac)

Open the application ``terminal``. Now run the ``diskutil list`` command see a list of drives in the system. Plug in the USB stick and run ``diskutil list`` again and use the difference in the output to find which device is your USB stick, this should be something like /dev/diskX or /dev/rdiskX.

To write the ISO to the USB stick, use the following command:
```
sudo dd if=/path/to/installation/media.iso of=/dev/diskX
```
**This erases all data on the target device! Do replace the path and the X in the device location, but be careful not to pick the wrong device!**

### Installing from USB (Linux)

Open a terminal and run the ``lsblk`` command see a list of drives in the system. Plug in the USB stick and run ``lsblk`` again and use the difference in the output to find which device is your USB stick, this should be something like /dev/diskX or /dev/rdiskX.

To write the ISO to the USB stick, use the following command:
```
sudo dd if=/path/to/installation/media.iso of=/dev/sdX
```
**This erases all data on the target device! Do replace the path and the X in the device location, but be careful not to pick the wrong device!**

## Using VaporOS

After installation there are a couple of steps to take to allow the use of VaporOS' features. These are listed here.

### Adding the VaporOS Applications to Steam

After logging in the Retroarch, Kodi and VaporOS-FTPServer have to be added to Steam before then can be used. To do this go to setting and under System pick "Add Library Shortcut". Pick the application you'd like to add. Repeat until all of them are in your Steam library.

### Transfering Files from Another Computer

To do this simply start the VaporOS-FTPServer program from Steam and enter the address shown in the file browser or and FTP client. This will allow you to transfer files to and from your Steam machine.

## Known Issues

- Retroarch and Kodi don't work with every type of controller, the Steam controller does work
- On BIOS systems the installer will ask where to install the bootloader, filling in /dev/sda should work on most systems. This is a SteamOS bug.
- Exiting VaporOS-FTPServer doesn't work with every type of controller at the moment. Binding Esc to the controller or pressing Esc on the keyboard quits it
- Applications installed with Flatpak don't have sound

## Support

If you need any help or would like to help out with this project, feel free to [join us on Discord](https://discord.gg/qynSaKY).

## Development

Instructions on how to build VaporOS yourself can be found [here](https://github.com/sharkwouter/vaporos/wiki/Build-Instructions). You can also find more information on how this works [here](https://github.com/sharkwouter/vaporos/wiki/Developer-Information).

## Special Thanks

- ProfessorKaos64 for packaging Retroarch.
- The Deb Multimedia team for packaging ffmpeg and Kodi.
- Nate Wardawg for the name.
- Jorgën Såagrid for allowing the continued use of the name VaporOS.
- Valve for creating SteamOS.
