---
icon: github
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

# Source

When you want the latest version that is available not even for release you can build from source. This means that you will need to clone the GitHub repository and compile it to a `.jar` file. You can find the build in the `/build/libs/` folder.

{% tabs %}
{% tab title="Linux" %}
## Linux

You can safely remove all repository files after copying your build.

```sh
git clone https://github.com/Vxrpenter/SCPToolsBot

cd SCPToolsBot

chmod +x gradlew
./gradlew shadowjar
```
{% endtab %}

{% tab title="Windows" %}
## Windows

{% hint style="warning" %}
This install is not recommended and not encouraged. All errors during installation are **YOUR** responsibility
{% endhint %}

```powershell
git clone https://github.com/Vxrpenter/SCPToolsBot

cd SCPToolsBot

./gradlew shadowjar
```
{% endtab %}

{% tab title="MacOS" %}
## MacOS

{% hint style="warning" %}
This install is not recommended and not encouraged. All errors during installation are **YOUR** responsibility
{% endhint %}

```sh
git clone https://github.com/Vxrpenter/SCPToolsBot

cd SCPToolsBot

chmod +x gradlew
./gradlew shadowjar
```
{% endtab %}
{% endtabs %}
