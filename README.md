# Debian Build for Biqu/BTT CB1 (AllWinner H616)

This project is just a manual triggered build pipeline for the latest official packages and OS system image. You can find the assets under releases here.

[https://github.com/freakydude/cb1-os-build/releases/tag/prerelease-latest](https://github.com/freakydude/cb1-os-build/releases/tag/prerelease-latest)

You can install and replace your whole system image `H616_2.3.3_debian_bullseye_server_linux5.16.17.img`
or as an alternative just install the newest packages e.g.
`linux-dtb-current-sun50iw9_2.3.3_arm64.deb`
`linux-image-current-sun50iw9_2.3.3_arm64.deb`

## Example

There is an issue with ghost touching on the BigTreeTech TFT35 SPI. It is fixed by BTT but there are no updated packages.

You can connect and login with SSH to your running CB1

- Get latest dtb files: `wget https://github.com/freakydude/cb1-os-build/releases/download/prerelease-latest/linux-dtb-current-s
un50iw9_2.3.3_arm64.deb`
- Get latest linux kernel build: `wget https://github.com/freakydude/cb1-os-build/releases/download/prerelease-latest/linux-image-current
-sun50iw9_2.3.3_arm64.deb`
- Install both packages with apt: `sudo apt install ./linux-dtb-current-sun50iw9_2.3.3_arm64.deb ./linux-image-current-sun50iw9_2.3.3_arm6
4.deb`
- Reboot: `sudo systemctl reboot`

**Thanks @Duckferd to provide the basic idea.**

## Risks

Please note that the use of this open-source code is at your own discretion. The developer is not liable for any damages or consequences resulting from the use of this code. Therefore, use it with caution and at your own risk.

## Reference

- [Latest official build CB1 Debian Image](https://github.com/bigtreetech/CB1)
- [Official sourcecode of this build](https://github.com/bigtreetech/https://github.com/bigtreetech/CB1-Kernel)
- [BIQU TFT35 SPI](https://github.com/bigtreetech/TFT35-SPI/)
- [Allwinner usb boot](https://linux-sunxi.org/FEL/USBBoot)
- [Allwinner Online Development Forum](https://bbs.aw-ol.com/topic/2054/mq-quad-h616-%E4%B8%BB%E7%BA%BF%E5%86%85%E6%A0%B8%E7%BC%96%E8%AF%91%E8%B0%83%E8%AF%95%E8%AE%B0%E5%BD%95-u-boot-kernel-buildroot/17)
