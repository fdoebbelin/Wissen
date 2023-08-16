## What's in this directory?

These are files containing the installer and other software for the Debian GNU/Linux operating system. The files in this directory are specifically for the `amd64` architecture.

## How do I use these files?

The files here are complete ISO images, ready to use.

Once you have downloaded all the ISO images you want, you will typically need to write them to installation media.

## What size and type of media will I need?

The images described here are sized to be written to writeable DVD media at a minimum, but may be written to larger media if needed.

For extra convenience, **these images may also be written directly to a USB stick**. So long as your computer will boot directly from that USB stick, it should start the Debian installer that way. The first DVD in this set is also deliberately limited in size so it should fit on a standard-sized 4GB USB stick.

## There are lots of files here! Do I need all of them?

In most cases it is not necessary to download and use **all** of these images to be able to install Debian on your computer. Debian comes with a massive set of software packages, hence why it takes so many disks for a complete set. Most typical users only need a small subset of those software packages.

Initially, you will only need to download and use the **first** image of a set (labelled as `debian-something-1` to be able to start the Debian installer and set up Debian on your computer. If there are more images available here (labelled `debian-something-2`, `debian-something-3`, etc.), they contain the extra packages that can be installed on a Debian system (as mentioned previously). They will **not** be bootable and are entirely optional. If you have a fast Internet connection, you're most likely better off installing any desired extra packages directly from the Debian mirrors on the Internet instead of by using these extra images.

## How can I verify my download is correct and exactly what has been created by Debian?

There are files here (SHA512SUMS, etc.) which contain checksums of the images. These checksum files are also signed - see the matching .sign files. Once you've downloaded an image, you can check:

- that its checksum matches that expected from the checksum file; and
- that the checksum file has not been tampered with.

For more information about how to do these steps, read the [verification guide](https://www.debian.org/CD/verify).

## Only the first few images are available! Where are the rest?

We don't store/serve the full set of ISO images for all architectures, to reduce the amount of space taken up on the mirrors. You can [use the jigdo tool](https://www.debian.org/CD/faq/#why-jigdo) to recreate the missing ISO images instead.

## Non-free Firmware

This is an **official** Debian image build and so only includes Free Software.

For convenience for some users, there is an alternative **unofficial** netinst CD build which includes [non-free firmware](https://wiki.debian.org/Firmware) for extra support for some awkward hardware. Look under [/cdimage/unofficial/non-free/cd-including-firmware/](https://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/) if you need that CD image instead.

## Other questions?

See the Debian CD [FAQ](https://www.debian.org/CD/faq/) for lots more information about Debian CDs and installation.

The images here were put together by the [Debian CD team](https://wiki.debian.org/Teams/DebianCd) , using debian-cd and other software.

| ![\[ICO\]](_resources/blank_f5af97b39630428188114a99af6aed4e.png) | [Name](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/?C=N;O=D) | [Last modified](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/?C=M;O=A) | [Size](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/?C=S;O=A) |
| --- | --- | --- | --- |
| * * * |     |     |     |
| [![\[PARENTDIR\]](_resources/go-previous_8af5008e089c46cb864f3ffef7273a47.png)](https://cdimage.debian.org/debian-cd/current/amd64/) | [Parent Directory](https://cdimage.debian.org/debian-cd/current/amd64/) |     | -   |
| [![\[SUM\]](_resources/text-x-generic-template_3ed1f92fb54a4edaa13c3dc5c0.png)](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA256SUMS) | [SHA256SUMS](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA256SUMS) | 2022-07-09 18:22 | 1.8K |
| [![\[CRT\]](_resources/application-certificate_03618dcf497940238fcbc10612.png)](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA256SUMS.sign) | [SHA256SUMS.sign](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA256SUMS.sign) | 2022-07-09 18:34 | 833 |
| [![\[SUM\]](_resources/text-x-generic-template_3ed1f92fb54a4edaa13c3dc5c0.png)](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA512SUMS) | [SHA512SUMS](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA512SUMS) | 2022-07-09 18:22 | 3.0K |
| [![\[CRT\]](_resources/application-certificate_03618dcf497940238fcbc10612.png)](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA512SUMS.sign) | [SHA512SUMS.sign](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/SHA512SUMS.sign) | 2022-07-09 18:34 | 833 |
| [![\[ISO\]](_resources/media-optical_e4a1cc40e26646fe8d1d766d055ed3e1.png)](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/debian-11.4.0-amd64-DVD-1.iso) | [debian-11.4.0-amd64-DVD-1.iso](https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/debian-11.4.0-amd64-DVD-1.iso) | 2022-07-09 13:57 | 3.6G |
| * * * |     |     |     |

Apache/2.4.54 (Unix) Server at cdimage.debian.org Port 443