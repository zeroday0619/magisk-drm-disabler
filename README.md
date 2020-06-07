# Magisk DRM Disabler (MDD)  [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

If you're on GitHub and want to create a Pull/Merge Request, head to this project's [GitLab repo.](https://gitlab.com/Atrate/magisk-drm-disabler/)

## READ THIS FIRST

Some (quite a few) users have reported various breakages due to this module. It is not really possible to fix them, since it seems that DRM might be integrated to tightly into some ROMs. You have been warned.

## Description

A Magisk module designed to disable DRM (Digital Restrictions Management) completely on Android devices using Magisk, for reasons of security or ethics (see: [Opposing Digital Rights Mismanagement](https://www.gnu.org/philosophy/opposing-drm.en.html) and [Examples of proprietary DRM](https://www.gnu.org/proprietary/proprietary-drm.en.html)).

[XDA Support thread](https://forum.xda-developers.com/apps/magisk/module-magisk-drm-disabler-t4070117)


**List of replaced files in LIGHT mode:**
```
system
├── bin/
│   ├── drmserver*
│   ├── lgdrmserver*
│   └── mediadrmserver*
└── vendor/
    └── lib/
        └── liboemcrypto.so
```

**List of replaced directories in LIGHT mode:**
```
/system/app/LGDrm
/system/etc/drm
/data/drm
/data/mediadrm
/data/vendor/mediadrm
/data/data/.drm
/data/.dcmdrm
```

**List of replaced files in FULL mode:**
```
system
├── bin/
│   ├── drmserver*
│   ├── lgdrmserver*
│   └── mediadrmserver*
├── etc/
│   ├── init/
│   │   ├── drmserver.rc*
│   │   └── mediardmserver.rc*
│   ├── move_widevine_data.sh*
│   └── permissions/
│       ├── com.android.mediadrm.signer.xml
│       └── com.google.widevine.software.drm.xml
├── framework/
│   ├── com.android.mediadrm.signer.jar*
│   └── oat/
│       ├── arm/
│       │   ├── com.android.mediadrm.signer.odex
│       │   └── com.android.mediadrm.signer.vdex
│       └── arm64/
│           └── com.android.mediadrm.signer.odex
├── lib/
│   ├── libdrmframework_jni.so
│   └── libstagefright_hwextendedmediadrm.so
├── lib64/
│   └── libdrmframework_jni.so
└── vendor/
    ├── bin/
    │   └── hw/
    │       ├── android.hardware.drm@1.0-service*
    │       ├── android.hardware.drm@1.0-service.widevine*
    │       ├── android.hardware.drm@1.1-service.clearkey*
    │       ├── android.hardware.drm@1.1-service.widevine*
    │       ├── android.hardware.drm@1.2-service.clearkey*
    │       ├── android.hardware.drm@1.2-service.widevine*
    │       └── vendor.oneplus.hardware.drmkey@1.0-service*
    └── lib/
        └── liboemcrypto.so
```

**List of replaced directories in FULL mode:**
```
/system/app/LGDrm
/system/etc/drm
/system/lib/drm
/system/lib64/drm
/system/vendor/lib/mediacas
/system/vendor/lib64/mediacas
/system/vendor/lib/mediadrm
/system/vendor/lib64/mediadrm
/data/drm
/data/mediadrm
/data/vendor/mediadrm
/data/data/.drm
/data/.dcmdrm
```

## Installation
1. Install through Magisk Manager 

OR

1. Download the module from the releases
2. Flash the module through Magisk Manager or TWRP/OrangeFox

### Grab the newest release on [GitLab](https://gitlab.com/Atrate/magisk-drm-disabler/-/releases) or [GitHub](https://github.com/Magisk-Modules-Repo/magisk-drm-disabler/releases)

---

### THIS IS NOT A MODULE THAT WILL HELP YOU BYPASS DRM PROTECTION
Quite the contrary, it will make you unable to watch any DRM-restricted content.

### Disclaimer
I am not responsible for any damage done to your device by this module, so flash at your of discretion

### LOOKING FOR TESTERS!
If you're interested in helping the project by being a tester, please refer to [CONTRIBUTING.md](./CONTRIBUTING.md)

## Credits
topjohnwu for magisk

## [Changelog](./CHANGELOG)

## License
This project is licensed under the [GPL-3.0-or-later](https://www.gnu.org/licenses/gpl-3.0.html).

