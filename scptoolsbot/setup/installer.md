---
icon: square-terminal
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Installer

There's an installation script that is updated with every release. Just head to the latest release and download the `installer.sh`. After downloading the installer, give it the right permissions and execute it.

## Quick Install

You can quickly run the most current version of the script directly from master:

```sh
sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/installer.sh)"
```

## Run from Release

When you download the script from the latest release you should give it the right execution permission and then run it:

```sh
chmod +x installer.sh

sudo ./installer.sh
```

