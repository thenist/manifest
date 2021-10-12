# Project Radiant #

### Sync ###

```bash

# Initialize local repository
repo init -u https://github.com/ProjectRadiant/manifest -b twelve

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

# Credits
* LineageOS for vendor and much more.
* ArrowOS who we track our hals from.
* ProtonAOSP for CTS and other patches.
* And everyone we have cherry picked from, Thank you so much! 

# Apply for Official # 
If you would like to apply for official, then feel free to take a look [here](https://github.com/ProjectRadiant/official_devices).