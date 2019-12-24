# Switch manifest for LineageOS pie

### Issues
* Random graphics glitches without hwc patch.

### Patching
* Apply bt.patch in hardware/interfaces.
* Apply kmod.patch in vendor/lineage.
* Apply Pro Controller patches to system/bt.
* Apply dolby, shieldtech, hekate and wlan patches to vendor/nvidia.
* Apply both PRs [here](https://github.com/DanielOgorchock/joycond/pulls) to hardware/nintendo/joycond.
* Repopick the nvidia-enhancements-p topic off of lineage gerrit.
* Apply frameworks_base-rsmouse.patch to frameworks/base
* Apply frameworks_native-hwc.patch to frameworks/native
* Copy NvShieldTech-hack.apk from patches to vendor/nvidia/common/shieldtech/app/NvShieldTech.apk (Forces on RSMouse)

### Notes
* vendorsetup.sh isn't used so just run lunch with lineage_icosa-userdebug.
