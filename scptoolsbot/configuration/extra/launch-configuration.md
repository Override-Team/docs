---
icon: rocket-launch
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

# Launch Configuration

The launch configuration defines the order in which processed are started and if they are started at all.

{% tabs %}
{% tab title="Launch Options" %}
## Launch Options

The launch options contain general settings for the launch order.

{% code lineNumbers="true" %}
```json
"launch_options": {
  "ignore_broken_entries": false
},
```
{% endcode %}

<details>

<summary>Ignore Broken Entries</summary>

{% hint style="danger" %}
A broken launch configuration is not good. You should delete it and let it be regenerated before you start the bot again
{% endhint %}

Defines if entries that are missing from the config, or configured incorrectly should be ignored on startup. If this option is set to `false`, the bot will notify the user of the broken entry or sometimes crash to prevent further errors.

</details>
{% endtab %}

{% tab title="Launch Order" %}
## Launch Order

{% hint style="warning" %}
This is only an example for the main bot startup, you can find the whole configuration in /SCPToolsBot/configs/extra/launch-configuration.json
{% endhint %}

h

{% code lineNumbers="true" %}
```json
"launch_order": [
    {
      "id": "",
      "engage": true,
      "separate_thread": false,
      "sections": [
        {
          "id": "",
          "engage": true,
          "log_action": true
        }
      ]
    }
]
```
{% endcode %}

<details>

<summary>Id</summary>

The id of the process, all available Id's are:

`main:BOT`, `main:STATUS_CLUSTER`, `main:COMMAND_MANAGER`, `main:COMMAND_LISTENER`, `main:STATUS_COMMAND_LISTENER`, `main:BUTTON_LISTENER`, `main:ENTITY_SELECT_LISTENER`, `main:MODAL_LISTENER`, `main:STRING_SELECT_LISTENER`, `main:NOTICE_OF_DEPARTURE_CHECKER`, `main:REGULARS_CHECKER`

</details>

<details>

<summary>Engage</summary>

Determines if the process should be engaged

</details>

<details>

<summary>Separate Thread</summary>

{% hint style="warning" %}
Currently not implemented
{% endhint %}

Determines if the process should be started on a separate thread

</details>

<details>

<summary>Sections</summary>

Id - [#section-ids](launch-configuration.md#section-ids "mention")

Engage - Defines if the section should be engaged

Log Action - Defines if the action should be logged in the console

</details>
{% endtab %}
{% endtabs %}

## Section Id's

<table data-full-width="false"><thead><tr><th>Main  Id</th><th>Section Id</th></tr></thead><tbody><tr><td><code>main:COMMAND_LISTENER</code></td><td><code>section:HELP_COMMAND</code>, <code>section:TEMPLATE_COMMAND</code>, <code>section:VERIFY_COMMAND</code>, <code>section:NOTICE_OF_DEPARTURE_COMMAND</code>, <code>section:REGULARS_COMMAND</code>, <code>section:PLAYER_COMMAND</code>, <code>section:SETTINGS_COMMAND</code>, <code>section:APPLICATION_COMMAND</code></td></tr><tr><td><code>main:STATUS_COMMAND_LISTENER</code></td><td><code>section:STATUS_COMMAND</code>, <code>section:STATUS_PLAYERLIST_COMMAND</code>, <code>section:STATUS_TEMPLATE_COMMAND</code></td></tr><tr><td><code>main:BUTTON_LISTENER</code></td><td><code>section:HELP_BUTTONS</code>, <code>section:TICKET_BUTTONS</code>, <code>section:APPLICATION_BUTTONS</code>, <code>section:VERIFY_BUTTONS</code>, <code>section:NOTICE_OF_DEPARTURE_BUTTONS,</code> <code>section:REGULARS_BUTTONS</code></td></tr><tr><td><code>main:ENTITY_SELECT_MENU</code></td><td><code>section:TICKET_ENTITY_SELECT_MENUS</code></td></tr><tr><td><code>main:MODAL_LISTENER</code></td><td><code>section:TICKET_MODALS</code>, <code>section:APPLICATION_MODALS</code>, <code>section:NOTICE_OF_DEPARTURE_MODALS</code></td></tr><tr><td><code>main:STRING_SELECT_LISTENER</code></td><td><code>section:TICKET_STRING_SELECT_MENUS</code>, <code>section:APPLICATION_STRING_SELECT_MENUS</code>, <code>section:REGULARS_STRING_SELECT_MENU</code></td></tr></tbody></table>
