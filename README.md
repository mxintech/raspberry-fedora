Install fedora in a Raspberry
===============

I follow the tutorial from the fedora magazine. You can check the links below.
I used a mac, consider it


### Reference Links
- [Mac commands to make SDcard](https://www.raspberrypi.org/documentation/installation/installing-images/mac.md)
- [Fedora magazine tutorial](https://fedoramagazine.org/install-fedora-on-a-raspberry-pi/)



## My steps

### Get and copy Fedora 32 arch64 to the SDcard

I downloaded the raw fedora image from the Fedora magazine tutorial

```bash
# Extract the compressed file
unxz ./Fedora-Minimal-32-1.6.aarch64.raw.xz

# List local disk (MAC only)
diskutil list

# Unmount the Disk related with your SDcard
# IMPORTANT: Validate is the correct device 
diskutil unmountDisk /dev/disk2

## Copy all the image to the SDcard
sudo dd bs=1m if=./Fedora-Minimal-32-1.6.aarch64.raw of=/dev/disk2

```

### Go to the raspberry
1. Insert the SDcard to the raspberry and boot the system
2. **Important step** Follow the instructions to configure for the FIRST time.
- You need to create an administrator user (this is made thanks to [Anaconda project](https://fedoraproject.org/wiki/Anaconda))
3. Login into the system with this user.

>Step 2 is very important have a keyboard ready. I made a mess with on this step and I had to erase the SDcard and start again


### Learn more
- [Interesting projects](https://www.raspberrypi.org/documentation/)



