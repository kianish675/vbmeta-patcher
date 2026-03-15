<p align="center">
  <img src="assets/bg.png" alt="vbmeta-patcher">
</p>
<p align="center">
  <b>vbmeta-patcher</b> is a work-in-progress tool for patching <code>vbmeta.img</code> on supported Samsung Galaxy devices using GitHub Actions.
</p>

## Warning

This project modifies verified boot metadata. OEM unlocking must be enabled before flashing.  
Flashing a patched <code>vbmeta.img</code> may result in boot failure, data loss, or a soft-bricked device.  
You are responsible for anything that happens to your device.

## How do I add support for my device?

To add support for a new device:

1. Fork the repo
2. Create a folder for your device codename inside `target/`
3. Place your stock `vbmeta.img` inside that folder
4. Add the codename to the workflow dispatch options
5. Run the workflow and verify the patched output
6. If you want to add official support, open a pull request

**Example:**
- `target/mydevice/vbmeta.img`

## Where and how do I get my stock `vbmeta.img`?

Your stock `vbmeta.img` usually comes from your device’s stock BL or AP firmware package.  
You can obtain it by downloading the stock firmware for your exact device model and region, then extracting the original `vbmeta.img` from the package.

One source for stock firmware is **samfw.com**.

Make sure you use the correct firmware for your exact device variant. Using the wrong `vbmeta.img` may cause flashing or boot issues.

To download the correct firmware, check your phone's **OMC sales code** in Settings.

**Example:**
- `A266BXXS4AYG9`

  <img src="assets/omc.jpg" width="32%"/>
  
## Credits

- [@cd-Crypton](https://github.com/cd-Crypton) for the inspiration for this project.