# HenryBoot
An All-In-One bootable USB drive that works on any architecture and contains many useful tools.

## Installation / Quickstart

### Prequisites
 - [7-zip](https://www.7-zip.org/)
 - A USB drive or SD/MicroSD card with a minimum of 8GB on it (for the lightest of installation weights). 32-128GB drives are *HIGHLY* recommended for a better experience.

### Let's get started!
 - Download the repo and extract it somewhere. 
 - Download Ventoy (can be found [here](https://www.ventoy.net/en/index.html)) and run it.
 - It will present you with a screen that looks like this:

![image](https://user-images.githubusercontent.com/62612165/142452824-4c453883-ac03-426d-83d5-48453d37e0d3.png)

 - Select your target USB drive, then click install.
 - Next, copy all the files in the github repo except for `LICENSE` and `README.md` to your USB drive once you finish formatting the drive.
 - For the next step, go [here](https://cdimage.ubuntu.com/lubuntu/releases/21.10/release/lubuntu-21.10-desktop-amd64.iso) and wait for the image to download.
 - Once downloaded, move the image to your USB drive and rename it EXACTLY to `Lubuntu-21.10-Preloaded.iso`.

 - Open the `persistence` folder. The only current supported persistence image is Lubuntu, which is why you just downloaded it. 
 - Next, download [this](https://github.com/ventoy/backend/releases/download/v5.0/images.zip) file and unzip it somewhere. This part requires [7-zip](https://www.7-zip.org/) to be installed. 
 - Go into the folder of images you just downloaded and find `persistence_xfs_4GB_casper-rw.dat` and copy it to the `persistence` folder on your USB drive. 
 - Almost done! 
 - Now, rename that fine EXACTLY to `lubuntu_4GB.dat`. Done! 
Now, go into your BIOS and boot from the drive! You should be presented with a screen like this:
![image](https://user-images.githubusercontent.com/62612165/142459343-f5210965-6b69-4c1a-ad0e-d1ef8f16c139.png)
If you don't see a screen looking similar to that, you've done something wrong.
 
#### To add more operating systems, see below.

## Tested Images

If an image is in **bold**, it supports persistence using the `persistence_xfs_4GB_casper-rw.dat` image.
Please note: for proper menu aliases for untested images, you need to add your image to the json file in the root of the `/ventoy` folder in this format:
```json
    ...
    "menu_alias": [
        ...
        {
            "image": "/myimage.iso",
            "alias": "My Image's Alias"
        },
        ...
    ]
    ...
```
OR
Rename the file you download from the download links below to the name specified in the list.

The following is a list of tested images.

 - [elementaryos-6.0-stable.20211103.iso](https://nyc3.dl.elementary.io/download/MTYzNzE1MDI2Mw==/elementaryos-6.0-stable.20211103.iso)
 - [endeavouros-2021.08.27-x86_64.iso](https://objects.githubusercontent.com/github-production-release-asset-2e65be/195270052/e7608cb1-35b6-44e3-a838-a6f20bc6103c?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20211117%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20211117T013916Z&X-Amz-Expires=300&X-Amz-Signature=2ff05eb276db7dc9c5fd11adcdf324eee05320aa9806564cf6aa457b816a481b&X-Amz-SignedHeaders=host&actor_id=62612165&key_id=0&repo_id=195270052&response-content-disposition=attachment%3B%20filename%3Dendeavouros-2021.08.27-x86_64.iso&response-content-type=application%2Foctet-stream)
 - [kubuntu-21.10-desktop-amd64.iso](https://cdimage.ubuntu.com/kubuntu/releases/21.10/release/kubuntu-21.10-desktop-amd64.iso)
 - [Lakka-Generic.x86_64-3.6.img](https://le-builds.lakka.tv/Generic.x86_64/Lakka-Generic.x86_64-3.6.img.gz) (Requires [7-zip](https://www.7-zip.org/) for extraction of archive once downloaded)
 - **Lubuntu-21.10-Preloaded.iso** (Just follow the quickstart guide for this one)
 - [MXlinux-21_x64.iso](https://cfhcable.dl.sourceforge.net/project/mx-linux/Final/Xfce/MX-21_x64.iso)
 - [Parrot-home-4.11.3_amd64.iso](https://edge1.parrot.run/parrot/iso/4.11.3/Parrot-home-4.11.3_amd64.iso)
 - [WindowsRecovery.iso](https://hbcd.mirrors.hoobly.com/HBCD_PE_x64.iso)
 - [xubuntu-21.10-desktop-amd64.iso](https://mirror.us.leaseweb.net/ubuntu-cdimage/xubuntu/releases/21.10/release/xubuntu-21.10-desktop-amd64.iso)
 - [Zorin-OS-16-Core.iso](https://mirror.umd.edu/zorin/16/Zorin-OS-16-Core-64-bit-r4.iso)

Want to submit a successfully tested image? Make an issue and use the `tested image` template.
