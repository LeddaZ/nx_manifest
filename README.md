# Switch manifest for LineageOS Pie

### Issues
* Random graphics glitches without hwc patch.

### Patching
Basic:
* Apply hardware_interfaces-bt.patch in hardware/interfaces.
* Apply vendor_lineage-kmod.patch in vendor/lineage.
* Apply frameworks_native-hwc.patch to frameworks/native
* Repopick the nvidia-enhancements-p topic off of lineage gerrit.
* Repopick the joycon-p topic off of lineage gerrit.

For RSMouse:
* Apply frameworks_base-rsmouse.patch to frameworks/base
* Apply 0001-HACK-use-platform-sig-for-shieldtech.patch to vendor/nvidia
* Copy NvShieldTech-hack.apk from patches to vendor/nvidia/shield/shieldtech/app/NvShieldTech.apk (Forces on RSMouse)

### Notes
* vendorsetup.sh isn't used so just run lunch with lineage_icosa-userdebug.
