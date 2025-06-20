---
icon: code-pull-request
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

# Release v1.1.0

{% hint style="danger" %}
The `updates.json` config in `.SCPToolsBot/configs/extra/` is configured to delete commands, launch option configs and translations, when they are out of date. Make a backup before updating. You can deactivate this once the configuration has been generated under the `settings` section.
{% endhint %}

The version 1.1.0 introduces many fixes, enhancements as well as new features to the SCPToolsBot. Because of this, many configuration files have been changed, breaking installs. The newly implemented update manager will show you what configs have been updated.

## Config.yml

Add this underneath the `cedmod` configuration:

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

New `date_formatting` option for notice of departures:

```yaml

notice_of_departure:
  # Activates the notice of departure feature
  active: false
  # The formatting that is used to format the notice of departure dates
  date_formatting: "dd.MM.yyyy"
  # Which channel should the form be sent to, to be accepted by moderators?
  decision_channel_id: ""
  # Which channel should the notice messages be sent to?
  notice_channel_id: ""
  # List of role's that are able to accept/dismiss/revoke notices (INPUT ID'S ONLY)
  roles_access_notices: []
  # Put the following in the type: [NANOSECONDS, MICROSECONDS, MILLISECONDS, SECONDS, MINUTES, HOURS, DAYS]
  check_type: "HOURS"
  # The rate at that the notices are checked.
  check_rate: 1
```

## Other

All of these files have been changed/removed. You can simply delete them and let them be regenerated, if you want to make it simple. If you have edited these files, backup you current files and then let the new ones be generated. Then you can re-add you custom changes.

* Removed `color-config`&#x20;
* Updated `commands.json`&#x20;
* Updated `launch-configuration.json`&#x20;
* Updated all language files
