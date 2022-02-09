# Project Radiant #

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/dylanneve1/manifest -b twelve

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags -v
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch radiant_$device-$type

# Build the code
$ mka bacon -j$
```

# IMPORTANT
You SHOULD as a responsible builder adapt your trees if your device settings look broken on homepage! if the layout is out of place, you have 2 options:
1. Move the DeviceSettings to System menu. Example: https://github.com/ShapeShiftOS-Devices/device_motorola_sanders/commit/d54176ba3813d03b11297683499512fd439408c3
2. Overlay IA for your Settings: Your tree must have an overlay folder (or an rro one) if its simply overlay then make a file overlay/packages/apps/Settings/res/values/strings.xml and in this file:

```xml
<?xml version="1.0" encoding="utf-8"?>

     <string name="ds_ia">org.lineageos.settings.device</string> <!-- replace with your IA key -->

</resources>
```

# Credits
* LineageOS for vendor and much more.
* ArrowOS who we track our hals from.
* ProtonAOSP for CTS and other patches.
* And everyone we have cherry picked from, Thank you so much! 

# Apply for Official # 
If you would like to apply for official, then feel free to take a look [here](https://github.com/ProjectRadiant/official_devices).
