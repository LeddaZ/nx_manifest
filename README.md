# Switch manifest for LineageOS Quorndog

### Environment Setup
The `snack` submodule is used to manage and automate repopicks and patches needed for a Switchroot Android development environment

To set up dev environment:
```bash
cd <folder>
repo init -u git://github.com/mer-hybris/android.git -b hybris-17.1
git clone https://gitlab.com/switchroot/android/manifest.git --recursive -b halium-17.1 .repo/local_manifests
.repo/local_manifests/snack/snack.sh -y
```

To build:
```bash
export USE_CCACHE=1 ALLOW_MISSING_DEPENDENCIES=true
make -j$(nproc --all) hybris-hal droidmedia
mka halium-boot
```

To flash:
```bash
./Heimdall/build/bin/heimdall flash --BOOT hybris-boot.img
```

### Products
* `icosa_sr`: Standard tablet Android with Nvidia enhancements, based on LineageOS
* `icosa_tv_sr`: Android TV with Nvidia enhancements, based on LineageOS

### Notes
* HWC is forced off for `icosa_sr`
* Nvidia games current do not work (use GLTools for Shield games)
