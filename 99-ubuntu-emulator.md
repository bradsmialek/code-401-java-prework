# Ubuntu JDK Emulator error

## Issue

When attempting to create an emulator using the [android developer guide](https://developer.android.com/studio/run/managing-avds), students may see a warning when they first build the emulator:

```
Grant current user access to /dev/kvm
```

They may proceed and create the emulator but when they try to run the app in the emulator it will fail, giving the error: 

```
/dev/kvm device: permission denied
Grant current user access to /dev/kvm
```
## Resolution

Paste these lines into the terminal to fix the issue.

```
sudo adduser $USER /dev/kvm;
sudo chown $USER /dev/kvm;
newgrp kvm;
```
Then restart your machine and android studio, it should work.

## Sources
If you have further issues, check out these sources

[https://stackoverflow.com/questions/37300811/android-studio-dev-kvm-device-permission-denied](https://stackoverflow.com/questions/37300811/android-studio-dev-kvm-device-permission-denied)
[https://askubuntu.com/questions/985142/ubuntu-14-android-studio-3-xrdp-dev-kvm-permission-denied](https://askubuntu.com/questions/985142/ubuntu-14-android-studio-3-xrdp-dev-kvm-permission-denied)

