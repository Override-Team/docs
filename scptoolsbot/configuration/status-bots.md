---
icon: signal-bars
---

# Status Bots

The Status Bots are multiple bot instances that receive information about your scp:sl servers and display it accordingly.

{% tabs %}
{% tab title="Getting Started" %}
## Getting Started

The status bots general settings.

{% code lineNumbers="true" %}
```yaml
# Determines if the bot(s) are active or not
active: false

# Your servers api key. You can get it from the console by typing < !api show >
api: ""
# Can be obtained by typing < !id > into your console
account_id: ""

# ** WARNING ** Turning off messes with template playerlists
# Turn this of if you don't want playerlists to be periodically updated
check_playerlist: true

# Should the server status be posted to a specified channel?
post_server_status: false
# The channel that the server status is going to be posted to
post_channel : ""
# Status page url, change this if you have a custom server status page set up, if not leave it as is
page_url: "https://status.scpslgame.com/"
```
{% endcode %}

<details>

<summary>Active</summary>

Determines if Status Bots are active

</details>

<details>

<summary>Api</summary>

{% hint style="warning" %}
You can only obtain an api key when your server is verified.
{% endhint %}

The api key of your server (scp:sl). You can obtain it by running `!api show` in your server console. If you are not receiving a key, type `!api reset` and then again `!api show`

</details>

<details>

<summary>Account Id</summary>

{% hint style="warning" %}
You can only obtain an account id when your server is verified.
{% endhint %}

The account id of your server (scp:sl). You can obtain it by running `!id` in your server console

</details>

<details>

<summary>Check Playerlist</summary>

Determines if playerlist's that have been created with the `/template` command be regularly checked and updated

</details>

<details>

<summary>Post Server Status</summary>

Determines if the current server status (online/offline/unreachable) should be posted to a channel.

</details>

<details>

<summary>Post Channel</summary>

{% hint style="warning" %}
Only works if `post_server_status` is active
{% endhint %}

The channel in which server status messages will be posted

</details>

<details>

<summary>Page Url</summary>

If you have a custom status page set up, you can reset this link with it

</details>
{% endtab %}

{% tab title="Rates" %}
## Rates

The check/retry/idle rates of the status bots.

{% code lineNumbers="true" %}
```yaml
# ** WARNING ** If this value is under 10, the api will rate limit all requests
# The rate at which the bot request updated information from the api
check_rate: 10
# If the retrieval of information fails, the bot wil retry for how many times you entered here
retry_to_fetch_data: 5
# When the bot fails to retrieve information, it will suspect a rate limit until passing the
# number you entered here
suspect_rate_limit_until: 2
# The time after the bot idles (it will automatically change to a higher check cooldown)
idle_after: 60
# The rate at which the bot checks for new information when it idles
idle_check_rate: 30
```
{% endcode %}

<details>

<summary>Check Rate</summary>

The rate (in seconds) at which the bot tries getting new information from the secret lab api. This rate will be applied to all instances

</details>

<details>

<summary>Retry to Fetch Data</summary>

How many times the bot retries after marking the api as unreachable

</details>

<details>

<summary>Suspect Rate Limit Until</summary>

How many retries the bot considers as rate limited requests

</details>

<details>

<summary>Idle After</summary>

The time the bot waits after not receiving any new data before idling

</details>

<details>

<summary>Idle Check Rate</summary>

The rate at which the bot requests new information from the secret lab api when idling

</details>
{% endtab %}

{% tab title="Instances" %}
## Instances

The different bot instances each provide data about a single server.

{% code lineNumbers="true" %}
```yaml
# The bot instances you want to create are entered here. To create a second one, copy over the already
# existing element and paste it underneath the other one (separate with comma)
instances: [
  {
    # The token for the bot you want to be the status bot
    token: "",
    # The name of the server the bot represents (can be anything you like)
    name: "",
    # The port of the server that this bot represents (e.g., 7777 as the default port)
    server_port: 0,
    # How many times should the bot retry to fetch data for this specific server until
    # declaring it as offline or unavailable
    retries: 4,
    playerlist: {
      # Activates the bots automatic playerlist placement
      active: false,
      # The channels the playerlist should be sent to and updated
      channel_ids: []
    }
  },
]
```
{% endcode %}

<details>

<summary>Instances</summary>

The list of instances objects, they will be loaded from top to bottom

</details>

<details>

<summary>Token</summary>

The token of the bot instance

</details>

<details>

<summary>Name</summary>

The name that will be displayed to users

</details>

<details>

<summary>Server Port</summary>

The port of the server, data is being queried from

</details>

<details>

<summary>Retries</summary>

How often the bot retries after marking the server as offline/unreachable

</details>

<details>

<summary>Playerlist</summary>

`Active` -  Determines if a persistent playerlist should be created

`Channel Ids` - The id's of the channels the playerlist will be sent to

</details>
{% endtab %}
{% endtabs %}

<details>

<summary></summary>



</details>

h
