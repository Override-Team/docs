---
icon: arrow-down-from-line
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

# Getting Started

First you need to install the bot onto your system. Installation on **Linux** servers is advised, but installing the bot on Windows and MacOS is still possible through **Docker** or the raw **Jar**.

## Installation Methods

These are all currently available installation methods for ScpTools.

{% tabs %}
{% tab title="Installer" %}
#### Installer (Linux)

The installer is the recommended way to install the bot. It is easy to use and allows for easy setup using the onboard configurator. It's only downside is the Linux exclusivity.

{% content-ref url="installer.md" %}
[installer.md](installer.md)
{% endcontent-ref %}
{% endtab %}

{% tab title="Docker" %}
#### Docker (Linux, Windows, MacOS)

When the installer cannot be used for installation, or you don't want to install java onto your machine, you can run the bot in a docker container.

{% content-ref url="docker.md" %}
[docker.md](docker.md)
{% endcontent-ref %}
{% endtab %}

{% tab title="Manual" %}
#### Manual (Linux, Windows, MacOS)

A basic way to install the bot. You can just download the `.jar` from the latest release and then run it on a server with the right java version (**22**) installed.

{% content-ref url="manual.md" %}
[manual.md](manual.md)
{% endcontent-ref %}
{% endtab %}

{% tab title="Source" %}
#### Source (Linux, Windows, MacOS)

If you want the latest version of the bot you can compile it from source. This is a bit more complicated and requires some technical knowledge.

{% content-ref url="source.md" %}
[source.md](source.md)
{% endcontent-ref %}
{% endtab %}
{% endtabs %}

## Fist Time Setup

{% hint style="success" %}
If you used the installer script and configured it with the build in configurator you can skip this
{% endhint %}

When first installing the bot you need to tweak some settings to get it working. This small guide will help you to find them and eliminate issues.

### 1. Mandatory Settings

On first startup you have probably experienced the bot crashing with an error. That is because you need to enter in three important id's for it to start up. These are the `token`, `client secret` and `guild id`. They can be found in the `config.yml` just at the top.

```yaml
# The token of your bot application, create one here https://discord.com/developers/
token: ""
# The client secret of your bot, get it from here https://discord.com/developers/ under OAuth section
client_secret: ""
# Your server ID, you can get it by activating discord developer mode and right-clicking your server
guild_id: ""
```

You can get 2 of these values from the official [Discord Developer Portal](https://discord.com/developers/applications). Create a bot application and then navigate to the `OAuth` and `Bot` sections. There you can find the buttons for resetting the applications `client secret` and `token`. Reset them, copy them and at last paste them into the config.

![img](https://github.com/user-attachments/assets/8f0be2d6-29b9-4b71-bc9c-3fc829e59b0a) ![img](https://github.com/user-attachments/assets/1bdffa7c-2339-4a5b-ac1f-5816bc7165bf)

The last value, meaning your guild id is just your discord server id. You can easily retrieve it by activating developer mode in the settings (Settings --> Advanced --> Developer Mode) and then right-clicking on your server.

Learn more about configuring on the [Config Page](broken-reference)

### 2. Language

If you don't like the standard English version of the bot, you can switch to the German version or copy the translation files (located in the `lang` folder) and change them to your liking.

```yaml
# Which language should the bot use?
#Choose from these supported languages or duplicate one of the translation files and change it yourself
# available translations: ["en_US", "de_DE"]
load_translation: "en_US"
```

_Learn more on this topic on the_ [_Translation Page_](broken-reference)

### 3. Feature Settings

For some features you need to tweak the configs. Generally it is good to look into the config and search for the section containing the feature to look what they need.

> \[!NOTE]\
> The status bots and support system have their own seperate configs, located in the same folder as the `config.yml`

### 4. Webserver and CedMod

If you have CedMod installed on your server you might want to use the integrated CedMod link in SCPTools. There's also a small webserver implemented that can handle discord OAuth request.

#### CedMod

If you want to activate CedMod, navigate to the CedMod section of the config and change `active` to `true`. You will need your instance url as well as an api key. This api key can only be obtained when asking CedMod staff directly, so head to their [discords support channel](https://discord.gg/rzAYbzCXRv) and request it.

```yaml
cedmod:
  # This activates the CedMod Api integration. This feature is only used for the following functions, only activate if you have these features in use: Regulars
  # CedMod Api is only available to users who request access from the CedMod team, ask on their discord for more information - https://discord.gg/p69SGfwxxm
  active: false
  # Include https://
  instance_url: ""
  # Put the plain API key here
  api_key: ""
```

#### Webserver

The webserver is a special feature that must be active for the `verify` and `regulars` feature. It handles Discord OAuth requests to link users steam and discord accounts. Follow the instructions in the config to activate it and make sure you configure your firewall correctly to filter requests.

```yaml
# ** WARNING ** For this setting to work, you need to activate the webserver.
#The webserver is generally just a redirect to receive data from the discord OAuth Api, so it
# should not interrupt any other web stuff running on your server.
verify:
  # This link can be obtained from the oauth section on the discord developer portal. First, enter the redirect you entered in the webserver section exactly
  # as described here: <uri>:<port><redirect_uri>, e.g. http://localhost:80/auth/discord/redirect. After entering the redirect, click on save to proceed with the
  # setup. You now have to scroll down to the 'OAuth2 URL Generator' where you need to click on 2 options, 'identify' and 'connections', after that scroll down
  # and select your redirect for the redirect url. Now you can copy the generated url into your clipboard. Paste it in here.
  oauth_link: ""
  # Which channel should verify logs be sent to?
  verify_log_channel: ""
```
