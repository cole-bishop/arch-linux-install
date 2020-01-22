# Arch Linux Install
A conservative arch linux installation featuring an encrypted `/` and `/boot`. The installation
 phases are divided into pre and post scripts to allow for pick and choose functionality. 
## pre-install-script
Intended to be performed upon a partitionless NVMe drive. The instructions feature: 
* Encrypted `/` 
* Encrypted `/boot` (separate partition)
* Encrypted `/swap`
* Encrypted `/tmp`
* Separate `/home` partition
* `/crypto_keyfile.bin`  so as to allow reduce login prompts to grub root decryption prompt and user login only.
* Installation of `networkmanager` for easy use of `nmtui`, for network connection after disconnecting
archiso media. 
## post-install-script
My custom installation. 
* Installs the `yay` pacman wrapper
* Installs the packages found in `pkglist.txt` using `yay`
* Enabling and registering of any packages that are to be used as systemd services.