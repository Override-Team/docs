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

# Commands

{% hint style="warning" %}
There are two arrays of commands, `commands` and `status_commands`. You can find all commands in `./SCPToolsBot/configs/extra/commands.json`
{% endhint %}

All commands that the bot can execute are defined in this global config. They can be changed to whatever the user likes, as long as the id's stay the same. This config also allows for the creation of entirely new commands.

{% code lineNumbers="true" %}
```json
{
  "commands": [
    {
      "active": true,
      "inherit": "",
      "name": "",
      "description": "",
      "default_permissions": [],
      "options": [
        {
          "type": "",
          "name": "",
          "description": "",
          "isRequired": true,
          "choices": [
            {
              "name": "",
              "id": ""
            }
          ]
        }
      ],
      "subcommands": [
        {
          "inherit": "",
          "name": "",
          "description": "",
          "options": [
            {
              "inherit": "",
              "name": "",
              "description": "",
              "options": [
                {
                  "type": "",
                  "name": "",
                  "description": "",
                  "isRequired": true
                }
              ]
            }
          ]
        }
      ]
    }
  ]
}
```
{% endcode %}

<details>

<summary>Active</summary>

Determines if the command is active

</details>

<details>

<summary>Inherit</summary>

The inheritance is an id that tells the bot which inner functions to run when it receives a command. This is determined by loading the inheritance id every time a command is executed and searching for the function that it should execute. Available inheritance id's are:

`commands.help.default`, `commands.template.default`, `commands.verify.default`, `commands.notice_of_departure.default`, `commands.regulars.default`, `commands.settings.default`, `commands.application.default`, `status_commands.status.default`, `status_commands.playerlist.default`, `status_commands.template.default`

</details>

<details>

<summary>Name</summary>

{% hint style="warning" %}
Commands can be lowercase only
{% endhint %}

The name of the command that will be displayed to users

</details>

<details>

<summary>Description</summary>

{% hint style="warning" %}
The description can not be empty
{% endhint %}

The description of the command that will be shown to users

</details>

<details>

<summary>Default permissions</summary>

The permissions that are needed to run the command. Available permissions can be found in this [javadocs](https://javadoc.io/doc/net.dv8tion/JDA/latest/net/dv8tion/jda/api/Permission.html)

</details>

<details>

<summary>Options</summary>

`Type` - The type of the option. Available types can be found in this [javadoc](https://javadoc.io/doc/net.dv8tion/JDA/latest/net/dv8tion/jda/api/interactions/commands/OptionType.html)

`Name` - The name of the option that will be shown to users

`Description` - The description of the option that will be shown to users

`Is Required` - Defines if the option is required to run the command

`Choices` - [#choices](commands.md#choices "mention")

</details>

<details>

<summary>Choices</summary>

`Name` - The name of the choice that will be shown to users

`Id` - The id of the choice

</details>

<details>

<summary>Subcommands</summary>

{% hint style="warning" %}
Currently no subcommands are implemented
{% endhint %}

`Inherit` - The inheritance id of the subcommand.

`Name` - The name of the subcommand that will be shown to users

`Description` - The description of the subcommand that will be shown to users

`Options` - [#options](commands.md#options "mention")

</details>
