# Switch manifest for LineageOS Pie

### Issues
* Random graphics glitches with glcomposer

### Patching
Basic:
* Repopick the nvidia-enhancements-p topic off of lineage gerrit.
* Repopick the joycon-p topic off of lineage gerrit.
* Repopick the icosa-bt topic off of lineage gerrit.
* Apply sw-keymaster.patch to vendor/nvidia using `git am`

For RSMouse:
* Apply frameworks_base-rsmouse.patch to frameworks/base
* Apply 0001-HACK-use-platform-sig-for-shieldtech.patch to vendor/nvidia
* Copy NvShieldTech-hack.apk from patches to vendor/nvidia/shield/shieldtech/app/NvShieldTech.apk (Forces on RSMouse)

### Notes
* vendorsetup.sh isn't used so just run lunch with lineage_icosa-userdebug.
* For icosa builds copy* device/nvidia/shield-common/permissions/privapp-permissions-nvidia-system.xml to /system/etc/permissions after flashing to avoid a bootloop.
* It's best to use foster-tab instead.
