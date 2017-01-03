# ddclient-dh
ddclient patch to support dinahosting domains

# DEPRECATED
Use ddnsupdater2

Or use https://github.com/alexandregz/ddns_synology_dinahosting (more manual method but it works fine)

# Usage
Apply patch file as usual.

# with DDNS updater (Synology package)
Execute ddclient with help option to update .dat file (Qtip package [DDNS updater](https://www.cphub.net/?id=40&pid=304) uses this file to show providers). Then, config ddclient from Synology Desktop.

```shell
root@voyager:/volume1/@appstore/ddnsupdater# cd /volume1/@appstore/ddnsupdater/ && wget https://raw.githubusercontent.com/alexandregz/ddclient-dh/master/dinahosting_synology.patch
[...]
root@voyager:/volume1/@appstore/ddnsupdater# patch < dinahosting_synology.patch
patching file ddclient
root@voyager:/volume1/@appstore/ddnsupdater# ./ddclient --help > tmp/ddnshelp.dat
root@voyager:/volume1/@appstore/ddnsupdater#
```

# Dinahosting config to DDNS updater

![Dinahosting configuration](https://raw.github.com/alexandregz/ddclient-dh/master/config.png)


# Requirements

**Domain zone type A** must be created before to use patch files

~~_dinahosting_synology.patch_ can create new zones automatically~~ this feature needs debug -problems with update


# Files

dinahosting.patch Patch file to [ddclient](https://github.com/wimpunk/ddclient) v3.8.2

dinahosting_osx.patch Patch file to ddclient installed with [Homebrew](https://github.com/homebrew/homebrew) v3.8.2 (distinct from Github repo)

dinahosting_synology.patch Patch file to [DDNS updater](https://www.cphub.net/?id=40&pid=304) package v.1.27-002
