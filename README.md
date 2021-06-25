# Switch manifest for LineageOS Quorndog

### Environment Setup
The `snack` submodule is used to manage and automate repopicks and patches needed for a Switchroot Android development environment

To set up dev environment:
```
cd <folder>
repo init -u https://github.com/LineageOS/android.git -b lineage-17.1
git clone https://gitlab.com/switchroot/android/manifest.git -b lineage-17.1-icosa_sr .repo/local_manifests
.repo/local_manifests/snack/snack.sh -y
```

### Products
* `icosa_sr`: Standard tablet Android with Nvidia enhancements, based on LineageOS
* `icosa_tv_sr`: Android TV with Nvidia enhancements, based on LineageOS

### Notes
* HWC is forced off for `icosa_sr`
* Nvidia games current do not work (use GLTools for Shield games)
