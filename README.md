# Magisk - Move User Certificates

This module makes all installed user certificates part of the system certificate store, so that they will automatically be used when building the trust chain. This module makes it unnecessary to add the network_security_config property to an application's manifest.

### Installation

1. Install [Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)
2. Download zip from [latest release](https://github.com/Bloody-Badboy/Move-User-Certificates/releases/latest/) or build using `dist.sh`
3. Install in Magisk
4. Install client certificates through [normal flow](https://support.portswigger.net/customer/portal/articles/1841102-installing-burp-s-ca-certificate-in-an-android-device)
5. Restart your device. Certificate copying happens during boot.
6. The installed user certificates can now be found in the system store.

### Adding certificates

Install the certificate as a user certificate and restart the device.

### Removing certificates

Remove the certificate from the user store through the settings, and restart the device.

## Building

```shell
./dist.sh
```

How to release a new version:

1. Push a new tag with a name like `v*`.
2. A new release will be automatically created.
