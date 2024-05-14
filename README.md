# Cachyos-Handheld-Edition

Handheld Edition of CachyOS

This will include our own calamares, adjusted desktop and scripts for proper installation on handhelds.
We will provide only the online installation, so an internet connection will be mandatory.

Currently it is not planned to support more bootloaders, but if there is any interest we can simply add them as in our default ISOs, for now we will default to systemd-boot.
There will be support for 5 different filesystems:

- xfs
- ext4
- btrfs (default)
- zfs
- bcachefs

There will also be automatic snapshotting implemented, to make it easy for users to rollback if they run into issues.
Bcachefs could be generally a good idea for handhelds, but it is not fully ready yet and we don't suggest it for now.

## Features
- scx_lavd used as default scheduler - LAVD is a latency sensitive scheduler, which is intended to be used for handhelds and gaming
- Steam Deck like Steam Expierence
- Gamescope Session properly implemented 
- Kernel Patched to have support for Steam Deck OLED
- Steam Deck OLED Firmware included as default
- HDR correctly implemented via kerel patches
- All dependecies and packages bundled for a proper gaming expierence (cachyos-gaming-meta)
- Support for Winesync/Fastsync/NTSync (proton-cachyos provides a fastsync patched proton)
- BBRv3 used as default
- OpenRGB Patches included
- Screensharing for Discord (via xwaylandvideobridge)
- CachyOS Kernel
- CachyOS Repository (all packages compiled with avx2/avx512 including auto detection for cpu support)


## Planned
- Improve the experience further to provide a Steam Deck similar experience to SteamOS
- Provide the Steam Deck Themes
- Enhance Hardware Support


## Additonal Information

### How can I disable scx_lavd and use the BORE/EEVDF Scheduler?

This can be simply done with following:
```
sudo systemctl disable scx.service
sudo systemctl mask scx.service
```

## Credit to:
- ChimeraOS
- Ripplingsnake
- Manjaro (Phillip Müller for the base deckify package)
