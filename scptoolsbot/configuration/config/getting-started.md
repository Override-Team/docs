---
icon: power-off
---

# Getting Started

This is the most standard configuration, consisting of token, secret, language, updating etc

{% tabs fullWidth="false" %}
{% tab title="Tokens" %}
## Tokens

{% hint style="danger" %}
Not entering the token, secret or guild id can result in crashes/immediate shutdown
{% endhint %}

These are values that are essential for the bot's functionality, they can not be missing/aren't optional

```yaml
# The token of your bot application, create one here https://discord.com/developers/
token: ""
# The client secret of your bot, get it from here https://discord.com/developers/ under OAuth section
client_secret: ""
# Your server ID, you can get it by activating discord developer mode and right-clicking your server
guild_id: ""
```

<details>

<summary>Token</summary>

The discord bot token can be found on the [discord developer portal](https://discord.com/developers/applications) after creating a new application. For a detailed guide on the creation of a discord app, [look here](https://discord.com/developers/docs/quick-start/getting-started). Search for it in the bot section.

</details>

<details>

<summary>Client Secret</summary>

The client secret can be found on the [discord developer portal](https://discord.com/developers/applications) after creating a new application. For a detailed guide on the creation of a discord app, [look here](https://discord.com/developers/docs/quick-start/getting-started). Search for it in the OAuth section.

</details>

<details>

<summary>Guild Id</summary>

The guild id is the Id of your discord server. You can copy it after activating discords developer mode:

1. Head to the Settings
2. Go to the Advanced section
3. Activate "Developer Mode"
4. `Right-Click` your Server and click on `copy guild id`

</details>
{% endtab %}

{% tab title="Language" %}
## Language

{% hint style="warning" %}
Only languages which translation files are in the `/ScpToolsBot/lang/` can be entered in the language field
{% endhint %}

The langage changes all text that is displayed by the bot to the users. Log messages are not affected from this.

```yaml
# Which language should the bot use?
#Choose from these supported languages or duplicate one of the translation files and change it yourself
# available translations: ["en_US", "de_DE"]
load_translation: "en_US"
```

You can easily replace the en\_US with any language that is avaidible. Avaidible languages are:

<details>

<summary>Languages</summary>

* `en_US` - (US) English version of the bot
* `de_DE` - (DE) German version of the bot

</details>

If you want to translate the bot into your own language or change something about the translation, look here:

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}
{% endtab %}

{% tab title="Debug & Updates" %}
## Debug

{% hint style="warning" %}
The advanced debug option can spam your console, to make reading live logs, almost impossible. Only use it if you know what you are doing. Also note that `advanced_debug` can only be activated when `debug` is also activated.
{% endhint %}

These are the avaidible debug modes. They are supposed to be used for finding errors in the configurations or the bot itself.

```yaml
# Activates debug logging, which gives you much more information on what the bot is doing.
debug: false
# ** Warning ** This feature is not recommended
#Displays all available information
advanced_debug: false
```

<details>

<summary>Debug</summary>

This shown so called `DEBUG` logs. They contain some additional information about the bot's processes and running tasks.

</details>

<details>

<summary>Advanced Debug</summary>

This shows so called `TRACER` logs. They contain all information about the bot's processes and running tasks.

</details>

## Updates

This regulates which types of updates will be shown to users. Note that the update checker itself cannot be deactivated, just regulated.

```yaml
# Settings for the update checker
updates:
  # Activate to ignore all versions that contain the beta tag
  ignore_beta: false
  # Activate to ignore all versions that contain the alpha tag
  ignore_alpha: true
```

<details>

<summary>Ignore Beta</summary>

All updates that have `beta` in their tag will be ignored by the update checker and not be shown in the console

</details>

<details>

<summary>Ignore Alpha</summary>

All updates that have `alpha` in their tag will be ignored by the update checker and not be shown in the console

</details>
{% endtab %}

{% tab title="Activity" %}
## Activity

{% hint style="warning" %}
The default activity displays `PLAYING /help`. The /help command can only be used by administrators, making this activity misleading in a way. Remove it to be sure prevent frustration.
{% endhint %}

```yaml
# The activity type of the bot, choose from the available list: [COMPETING, CUSTOM_STATUS, LISTENING, PLAYING, WATCHING]
activity_type: "PLAYING"
# The text that is being displayed in the activity
activity_content: "/help"
```

<details>

<summary>Activity Type</summary>

The activity type, is the type of display that will be used, e.g. `PLAYING`. Avaidible activity types are:

`COMPETING`; `CUSTOM_STATUS`, `LISTENING`, `PLAYING` and `WATCHING`

</details>

<details>

<summary>Activity Content</summary>

{% hint style="danger" %}
Leaving this field empty, will result in a crash
{% endhint %}

The activity content is the text that will be displayed next to the activity type.

</details>
{% endtab %}
{% endtabs %}
