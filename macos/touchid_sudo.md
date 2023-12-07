# Persistent TouchID for sudo

I always need to set this up after updating macOS, but this solution seems to prevent this setting from being reset on update. 

Edit/Create the following file:
```
/etc/pam.d/sudo_local
```

Include the following in `/etc/pam.d/sudo_local`
```
auth sufficient pam_tid.so
```

Confirm that `/etc/pam.d/sudo` includes: `auth include sudo_local`

*source:* [alansiu](https://www.alansiu.net/2023/11/08/using-touch-id-for-sudo-on-macos-even-after-installing-an-os-update/)
