---
icon: ticket
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

# Tickets

The bots ticket system that is built for scp:sl

{% tabs %}
{% tab title="Settings" %}
## Settings

The general settings for tickets

```yaml
settings:
  # The channel all new ticket creation will be sent to
  ticket_log_channel: ""
  # The channel where the application message (active/not active) will be sent to
  application_message_channel: ""
```

<details>

<summary>Ticket Log Channel</summary>

The id of the channel ticket logs will be send to

</details>

<details>

<summary>Application Message Channel</summary>

The id of the channel the application messa

</details>
{% endtab %}

{% tab title="Application Types" %}
## Application Types

{% hint style="warning" %}
This is just a showcase, you can find all predefined application types in the `/SCPToolsBot/configs/ticket-settings.yml`
{% endhint %}

The types (roles/positions) of application that users are able to send

{% code lineNumbers="true" %}
```yaml
# The types of roles that can be applied for. Duplicate one of the roles that already exist
# to create a new one, you can add as many as you like
application_types: [
  {
    # The name of the role
    name: "Supporter",
    # The role description, meaning their supposed work in the team
    description: "Helps users ingame and handles reports",
    # The roles emoji that will be shown in the list of applicable roles
    emoji: "",
    #  The roles id, meaning the discord role itself
    role_id: ""
  }
]
```
{% endcode %}

<details>

<summary>Name</summary>

The name of the application type that will be displayed to the user

</details>

<details>

<summary>Description</summary>

The description of the application type that will be displayed to the user

</details>

<details>

<summary>Emoji</summary>

The emoji of the application type that will be displayed to the user

</details>

<details>

<summary>Role Id</summary>

The id of the role that this application type represents

</details>
{% endtab %}

{% tab title="Types" %}
## Types

{% hint style="danger" %}
Do not add any more ticket types than defined in the config, they will not work and could result in a crash
{% endhint %}

{% hint style="warning" %}
This is just a showcase, you can find all predefined ticket types in the `/SCPToolsBot/configs/ticket-settings.yml`
{% endhint %}

The types of tickets that can be created, each with a different purpose and some own quirks

{% code lineNumbers="true" %}
```yaml
# ** WARNING ** Do not add or remove any types as it will cause errors
# The types of tickets that can be opened
types: [
  {
    # The name of the ticket type
    name: "General",
    # ** WARNING ** Don't change this as it will change how the bot defines
    # the type defining the ticket in the code
    type: "support::GENERAL",
    # The roles that will be added to the ticket once it is created
    roles: [ ],
    # The roles that can interact with the tickets log
    log_permissions_roles: [ ],
    # The channel that the ticket will be created under (ticket is a thread)
    parent_channel: "",
    child_rules: {
      # ** WARNING ** Do not remove the %r% in the type name as it will cause errors
      # The naming scheme the ticket type follows, the %r% stands for the number of the ticket
      parent_name: "Ticket #%r%",
      # ** WIP ** This feature has not been implemented yet, and it's implication is not certain for 100%
      # Should the status bar be displayed
      use_status_bar: true,
      # ** WIP ** This feature has not been implemented yet
      # Should the ticket be locked when first created, needing a staff member to unlock it
      lock_on_default: false
    }
  }
]
```
{% endcode %}

<details>

<summary>Name</summary>

The name of the ticket type that will be displayed to users

</details>

<details>

<summary>Type</summary>

The id of the ticket type that let's the bot define which internal functions to use

</details>

<details>

<summary>Roles</summary>

An array of  role id's that can interact with the ticket settings

</details>

<details>

<summary>Log Permission Roles</summary>

An array of role id's that can interact with the ticket logs

</details>

<details>

<summary>Parent Channel</summary>

The id of the channel new tickets will be created (as a threat) under

</details>

<details>

<summary>Child Rules</summary>

`Parent name` - The name that the created ticket will have

{% hint style="warning" %}
These two features are currently WIP
{% endhint %}

`Use Status Bar` -

`Lock on Default` -

</details>
{% endtab %}
{% endtabs %}
