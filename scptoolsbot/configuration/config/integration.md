---
icon: webhook
---

# Integration

These are settings for integrating plugins or services into the bot. A good example is CedMod, which stores lot's of interesting and useful data, that can be used for e.g. Playtime-Roles.

{% tabs %}
{% tab title="CedMod" %}
## CedMod

{% hint style="warning" %}
The CedMod integration needs a valid CedMod api key to function. This key can only be requested from CedMod staff. Go to their [discord's support](https://discord.com/invite/p69SGfwxxm) channel, to obtain it.
{% endhint %}

This integration incorporates CedMod into ScpTools, allowing for some available features.

{% code lineNumbers="true" %}
```yaml
cedmod:
  # This activates the CedMod Api integration. This feature is only used for the following functions, only activated if you have these features in use: Regulars
  # CedMod Api is only available to users who request access from the CedMod team, ask on their discord for more information - https://discord.gg/p69SGfwxxm
  active: false
  # Include https://
  instance_url: ""
  # Put the plain API key here
  api_key: ""
```
{% endcode %}

<details>

<summary>Active</summary>

Defines if the CedMod integration is active

</details>

<details>

<summary>Instance Url</summary>

{% hint style="warning" %}
Include https://
{% endhint %}

The url to your cedmod instance, e.g. `https://testserver.cedmod.app`

</details>

<details>

<summary>Api Key</summary>

Your api key, which you can obtain from the api key section in your CedMod-Panel. Create a new api user and make sure to give them the appropriate permissions (to be sure, just assign all)

</details>
{% endtab %}

{% tab title="XP" %}
## XP

{% hint style="warning" %}
This integration does currently not support any custom level functions.
{% endhint %}

{% code lineNumbers="true" %}
```yaml
# ** NOTICE ** Custom level functions are currently not supported because of technical complexity
# This is a work-in-progress compatibility implementation of the XP plugin by RowspannSCP https://github.com/RowpannSCP/XP. It is intended to be used with the
# regulars feature for providing additional goals for playtime roles. This feature is highly WIP and will probably take a bit longer to implement, as I have to
# inspect their code to find some necessary information. The current config options are subject to change.
XP:
  # This activates the XP integration. This feature is only used for the following functions, only activated if you have these features in use: Regulars
  active: false
  # ** WARNING ** LiteDB will not be supported in any coming version as it would be really challenging to implement, in the end, bringing no real advantage
  # The address of the database which the plugin uses. If the plugin and bot are running on the same DB, the bot will identify it and not connect to the database
  # a second time and just pull data from the existing connection. Make sure you give the bot's user enough rights to do so.
  # Example database address: < localhost:3306/test >
  database_address: ""
  # The username of the database user you want the bot to use
  database_user: ""
  # The password of the user you want the bot to use
  database_password: ""
  # ** WARNING ** To keep this feature as simple as possible, there will only be one auth type supported. Also, Northwood authtype is currently not supported
  # Which type of authorization table do you want to query from?
  # Available auth types are [STEAM, DISCORD]
  auth_type: ""
  # This affects the 'a' parameter in the standard level function. This is the standard function used by the XP plugin: -50 + sqrt((4 * xp / a) + 9800) / 2
  additional_parameter: 1
```
{% endcode %}

<details>

<summary>Active</summary>

Determines if XP integration is active

</details>

<details>

<summary>Database Address</summary>

{% hint style="warning" %}
LiteDB will not not supported because it is a No-SQL database. If you are using docker, make sure you bind the ports correctly.
{% endhint %}

The address to your `MySQL` or `MariaDB` database. The address may look something like this: `localhost:3306/test`&#x20;

</details>

<details>

<summary>Database User</summary>

Your database user

</details>

<details>

<summary>Database Password</summary>

The password of your database user.

</details>

<details>

<summary>Auth Type</summary>

{% hint style="warning" %}
`NORTHWOOD` authorization will not be supported
{% endhint %}

What authorization table do you want to query from? Available types are:

`STEAM`, `DISCORD`

</details>

<details>

<summary>Additional Parameter</summary>

An additional parameter in the function so you can customize the calculated level output correctly:

$$f(xp) = -50 + \sqrt{(4 * xp : a) + 9800 \over 2}$$

</details>
{% endtab %}
{% endtabs %}
