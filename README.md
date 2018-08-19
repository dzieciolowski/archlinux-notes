# Arch Linux Notes

## Upgrade firmware on Crucial SSD

1. Download firmware from [http://www.crucial.com/usa/en/support-ssd](http://www.crucial.com/usa/en/support-ssd).

2. Unzip downloaded file.

3. Enhance ISO image by a Master Boot Record for booting via BIOS from USB stick (make sure you have [syslinux](https://www.archlinux.org/packages/core/x86_64/syslinux/) package installed):
`isohybrid MX500_M3CR022_Update.iso`

4. Copy ISO image to USB stick:
`sudo dd if=./MX500_M3CR022_Update.iso of=/dev/sdX oflag=sync bs=512k`

5. Boot from USB stick. The firmware will be updated automatically.
