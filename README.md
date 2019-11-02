# Switch manifest for LineageOS pie

### Issues
* Wifi and bt fw isn't copied to vendor, need to integrate fw symlinking in wifi loader script.
* Random graphics glitches
* Omx is broken (fixed upstreamish)


### Stuff
* remove NvCPLSvc from vendor/nvdia/common/nvcpl makefile, it causes logspam at the moment.
* bt.patch needs to be applied in hardware/interfaces, kmod.patch goes in vendor/lineage and the others go to system/bt
* vendorsetup.sh isn't used so just run lunch with lineage_foster_tab-userdebug
