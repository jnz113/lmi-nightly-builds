# Nightly Xiaomi-lmi PostmarketOS Builds

This repository contains workflows and configurations to automatically build PostmarketOS edge images for Xiaomi-lmi supported by mainline kernel fork. These images are intended for testing purposes only and should make testing more accessible to people without the capabilities to compile the kernel from source.

## Image Information

The CI builds images once on Day 1 and Day 15 at midnight UTC. When completed, it will upload artifacts for each device that was built. These artifacts contain `boot.img` and an xz-compressed rootfs. Artifacts are kept for 14 days (i.e. until the next rebuild).

The default user is called `user`, the password is `147147`, just like on official PostmarketOS stable images.

## Downloading

Head to the [Actions tab](https://github.com/jnz113/lmi-nightly-builds/actions), select the most recent successful run and download the artifact for your device. Extract the Zip, de-compress the rootfs and you're ready to flash!

## Tips

For xiaomi-lmi, when migrating from the stock Android system, remember to wipe the dtbo partition.

Flash the rootfs image to the super partition, and the boot image to the boot partition.