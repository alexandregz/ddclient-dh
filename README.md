# ddclient-dh
ddclient patch to support dinahosting domains

# Usage
Apply patch file as usual.

# with DDNS updater (Synology package)
Execute ddclient with help option to update .dat file (Qtip package [DDNS updater](https://www.cphub.net/?id=40&pid=304) uses this file to show providers). Then, config ddclient from Synology Desktop.

```shell
root@voyager:/volume1/@appstore/ddnsupdater# patch < dinahosting_synology.patch
patching file ddclient
root@voyager:/volume1/@appstore/ddnsupdater# ./ddclient --help > tmp/ddnshelp.dat
root@voyager:/volume1/@appstore/ddnsupdater#
```

# Dinahosting config to DDNS updater

![Dinahosting configuration](https://raw.github.com/alexandregz/ddclient-dh/master/config.png)


# Requirements

**Domain zone type A** must be created before to use


# Files

dinahosting.patch Patch file to [ddclient](https://github.com/wimpunk/ddclient) v3.8.2

dinahosting_osx.patch Patch file to ddclient installed with [Homebrew](https://github.com/homebrew/homebrew) v3.8.2 (distinct from Github repo)

dinahosting_synology.patch Patch file to [DDNS updater](https://www.cphub.net/?id=40&pid=304) package v.1.27-002