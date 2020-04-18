# Switch manifest for LineageOS Pie

### Issues
* Random graphics glitches with glcomposer

### Patching
Basic:
* Repopick the nvidia-enhancements-p, nvidia-shieldtech-p,nvidia-nvgpu-p, nvidia-beyonder-p, joycon-p and icosa-bt topics off of lineage gerrit.
* Also `repopick 272671`.
* Apply all patches to their respective directories (from patches folder).

### Notes
* Beyonder and RSMouse both require ATV builds to fully work without hacks.
* For Beyonder (Shield TV remote app) you can run the command `settings put global mouse_mode 0` once in ADB to enable the trackpad.
* Use foster\_tab if you want Nvidia games.
