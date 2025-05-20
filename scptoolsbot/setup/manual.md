---
icon: java
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

# Manual

You can always head to the [latest release](https://github.com/Vxrpenter/SCPToolsBot/releases) and download the `.jar` that contains the bot. Just make sure you have java 22 or higher installed and you are good to go.

{% tabs %}
{% tab title="Linux" %}
## Linux

Sometimes console is spammed with warnings on startup, you can remove these by adding this option before -jar `--enable-native-access=ALL-UNNAMED`

```sh
sudo java -jar <file.jar>
```
{% endtab %}

{% tab title="Windows" %}
## Windows

{% hint style="warning" %}
This install is not recommended and not encouraged. All errors during installation are **YOUR** responsibility
{% endhint %}

```powershell
java -jar <file.jar>
```
{% endtab %}

{% tab title="MacOS" %}
## MacOS

{% hint style="warning" %}
This install is not recommended and not encouraged. All errors during installation are **YOUR** responsibility
{% endhint %}

```sh
sudo java -jar <file.jar>
```
{% endtab %}
{% endtabs %}
