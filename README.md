# pulseandroid
pulseaudio on a smartphone

## How to make it work

### Prerequisites
You will need:

* an Android phone running [Android 7.0.0 or higher](https://wiki.termux.com/wiki/FAQ#What_are_system_requirements)
* [Termux](https://termux.com/)
* [Termux:Boot](https://wiki.termux.com/wiki/Termux:Boot)

### Packages
1. After installing Termux, open it and enter:

   ```sh
   pkg update -y
   pkg add openssh termux-services pulseaudio
   rm $PREFIX/var/service/sshd/down
   ```
   
1. Copy the files in `home/` to `$HOME` and the `etc/` and `usr/` directories to `$PREFIX`.

1. If you wish to access the device using SSH, make note of the username (obtainable using `echo $USER`).

1. Start *Termux:Boot* once.

1. Restart the device.

   You may need to open Termux again to grant background-running privileges.

