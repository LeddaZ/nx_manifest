# Switch manifest for LineageOS pie

### Issues
* Random graphics glitches - Disable hw overlays in dev options.

### Patching
* Apply bt.patch in hardware/interfaces.
* Apply kmod.patch in vendor/lineage.
* Apply Pro Controller patches to system/bt.
* Apply dolby, shieldtech, hekate and wlan patches to vendor/nvidia.
* Apply both PRs [here](https://github.com/DanielOgorchock/joycond/pulls) to hardware/nintendo/joycond.
* Repopick the nvidia-enhancements-p topic off of lineage gerrit.
* Apply hack-input.patch to frameworks/native
* Copy NvShieldTech-hack.apk from patches to vendor/nvidia/common/shieldtech/app/NvShieldTech.apk (Forces on RSMouse)

### Notes
* vendorsetup.sh isn't used so just run lunch with lineage_foster_tab-userdebug.
