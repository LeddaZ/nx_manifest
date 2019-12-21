# Switch manifest for LineageOS pie

### Issues
* LP0 is broken
* Performace significantly decreases without USB plugged in.
* Random graphics glitches - Disable hw overlays in dev options.

### Patching
* Apply bt.patch in hardware/interfaces.
* Apply kmod.patch in vendor/lineage.
* Apply Pro Controller patches to system/bt.
* Apply hekate and wlan patches to vendor/nvidia.
* Apply both PRs [here](https://github.com/DanielOgorchock/joycond/pulls) to hardware/nintendo/joycond.
* Repopick the nvidia-enhancements-p topic off of lineage gerrit.

### Notes
* vendorsetup.sh isn't used so just run lunch with lineage_foster_tab-userdebug.
