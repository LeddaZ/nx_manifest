# Supplemental Manifest for TWRP 11 (icosa_sr)

```bash
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-11
git clone https://gitlab.com/switchroot/android/manifest.git -b lineage-18.1-twrp .repo/local_manifests
repo sync
repopick -g https://review.lineageos.org 316988
lunch twrp_icosa_sr-userdebug
WITH_TWRP=true ALLOW_MISSING_DEPENDENCIES=true m recoveryimage
```
