# CVE-2020-0443

This is a proof of concept app that exploits [CVE-2020-0443](https://www.cve.org/CVERecord?id=CVE-2020-0443) to brick any Android device. After running the app and rebooting, the device will keep repeating the boot animation.  
[A patch](https://android.googlesource.com/platform/frameworks/base/+/d3a2b5832f6ca9da74cda814ec76aec679b3389a) for this vulnerability was released in the [November 2020 Android security bulletin](https://source.android.com/security/bulletin/2020-11-01#framework).  
Devices bricked due to this vulnerability can be fixed either through factory reset, or if you have access to ADB during the boot-loop:
```
adb shell settings put system system_locales en_US
```
Install and/or run this app at your own risk. I'm not responsible for data loss or damaged devices.  
Note that this project is provided for educational purposes only; please don't use it for malicious activities.
