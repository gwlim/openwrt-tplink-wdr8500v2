# OpenWrt support for TP-LINK WDR8500v2

This repository contains patches and binaries for adding OpenWrt support on TP-LINK WDR8500v2

  - Full hardware support
  - Requires external SPI Programmer to replace original uboot with Breed bootloader
 
Original uboot needs to be replaced due to RSA Protection

  - Overwrite the first 102K of the SPI flash with the breed bootloader included in this repository
  - git clone official openwrt repository
  - copy all the patches into the openwrt repository
  - apply the patches and do make menuconfig
  - choose TP-LINK WDR8500v2 then make

```sh
$ git apply *.patch
$ make menuconfig
$ make
```
