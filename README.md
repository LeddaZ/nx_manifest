# Switch manifest for LineageOS Pie

### Issues
* Random graphics glitches with glcomposer

### Patching
Basic:
* Repopick the nvidia-enhancements-p topic off of lineage gerrit.
* Repopick the joycon-p topic off of lineage gerrit.
* Repopick the icosa-bt topic off of lineage gerrit.

For RSMouse:
* Apply frameworks_base-rsmouse.patch to frameworks/base
* Copy NvShieldTech-hack.apk from patches to vendor/nvidia/shield/shieldtech/app/NvShieldTech.apk (Forces on RSMouse)

### Notes
* Use foster_tab if you want Nvidia games
