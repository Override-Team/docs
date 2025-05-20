---
icon: alien-8bit
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

# Features

These are features that need some configuration before being used.

{% tabs %}
{% tab title="Verify" %}
## Verify

{% hint style="warning" %}
Webserver must be active for verify to work
{% endhint %}

This feature let's users connect their steam and discord to cache correct data from e.g. the CedMod api

{% code lineNumbers="true" %}
```yaml
# ** WARNING ** For this setting to work, you need to activate the webserver.
# The webserver is generally just a redirect to receive data from the discord OAuth Api, so it
# should not interrupt any other web stuff running on your server.
verify:
  # Activates the verify feature, make sure you have configured webserver accordingly
  active: false
  # This link can be obtained from the oauth section on the discord developer portal. First, enter the redirect you entered in the webserver section exactly
  # as described here: <uri>:<port><redirect_uri>, e.g. http://localhost:80/auth/discord/redirect. After entering the redirect, click on save to proceed with the
  # setup. You now have to scroll down to the 'OAuth2 URL Generator' where you need to click on 2 options, 'identify' and 'connections', after that scroll down
  # and select your redirect for the redirect url. Now you can copy the generated url into your clipboard. Paste it in here.
  oauth_link: ""
  # Which channel should verify logs be sent to?
  verify_log_channel: ""
```
{% endcode %}

<details>

<summary>Active</summary>

Determines if the verify feature is active

</details>

<details>

<summary>OAuth Link</summary>

This is the link users will be prompted to click when verifying. To activate OAuth for your application, head to the [discord developer portal](https://discord.com/developers/applications). Head to the OAuth section and follow these steps:

1. Enter the redirect you entered on [webserver setup](webserver.md).&#x20;
2. Click on `identify` and `connections`
3. Select your redirect link and generate a OAuth link

</details>

<details>

<summary>Verify Log Channel</summary>

The id of the channel you want to send verify logs to.

</details>
{% endtab %}

{% tab title="Notice of Departure" %}
## Notice of Departure

This feature let's staff members define a time period in which they are not available. This period will be regularly checked and admin's will be notified if the time runs out.

{% code lineNumbers="true" %}
```yaml
notice_of_departure:
  # Activates the notice of departure feature
  active: false
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
{% endcode %}

<details>

<summary>Active</summary>

Determines if notice of departures is active

</details>

<details>

<summary>Decision Channel</summary>

The id of the channel that the message for regular decision will be sent to. This decision message can only be accessed by users who permitted to. If decision is accepted or denied a message will be sent to the sender, notifying them of the decision

</details>

<details>

<summary>Notice Channel</summary>

The id of the channel that the accepted notices will be sent to. These notice messages contain a button for revoking the notice if needed.

</details>

<details>

<summary>Roles Access Notices</summary>

An array of roles who should be able permitted to accept/deny/revoke notices.&#x20;

</details>

<details>

<summary>Check Type</summary>

The type of time-format the checker should follow. Available formats are:

`NANOSECONDS`, `MICROSECONDS`, `MILLISECONDS`, `SECONDS`, `MINUTES`, `HOURS`, `DAYS`

</details>

<details>

<summary>Check Rate</summary>

The rate at which notices should be checked/validated

</details>
{% endtab %}

{% tab title="Regulars" %}
## Regulars

{% hint style="warning" %}
Regulars needs extra configuration, check out the regular page to learn more. [Webserver](webserver.md), [Verify](features.md#verify) and [CedMod](integration.md#cedmod) or [XP](integration.md#xp) integration must be activated for regulars to function.
{% endhint %}

{% code lineNumbers="true" %}
```yaml
regulars:
  # Activates regulars, make sure you have correctly configured the regular's configs, as well as activated the necessary compatibility settings
  active: false
  # Should example configuration be created (deactivate if you want to delete the example config)
  create_example_configuration: true
  # Should the bot only load from the specified folder within the /regulars/ folder?
  only_load_certain_folder: false
  # Specify which folders should be specified if the option above is active
  only_load_folders: []
```
{% endcode %}

<details>

<summary>Active</summary>

Determines if regulars is active

</details>

<details>

<summary>Create Example Configuration</summary>

If active, an example configuration directory is created under `/SCPToolsBot/regulars/` . Deactivate this after you know how to configure regulars correctly

</details>

<details>

<summary>Only Load Certain Folders</summary>

Determines if only certain folders should be loaded

</details>

<details>

<summary>Only Load Folders</summary>

{% hint style="warning" %}
only works if `only_load_certain_folder` is active
{% endhint %}

An array consisting of the folders that should be loaded

</details>
{% endtab %}
{% endtabs %}
