---
icon: globe-pointer
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

# Webserver

The webserver is used for receiving information from discord OAuth requests. If you are not using the following features you can ignore it:

* Verify

If you want to configure these features, look into:

{% content-ref url="features.md" %}
[features.md](features.md)
{% endcontent-ref %}

{% code lineNumbers="true" %}
```yaml
webserver:
  # Should the webserver be launched? This feature is only used for regulars
  active: false
  # The port under which the webserver will be launched
  port: 8080
  # What uri to start the webserver under
  redirect_uri: "/auth/discord/redirect"
  # Where should the redirect be, include the full url e.g., https://localhost:80/auth/discord/redirect
  uri: ""
```
{% endcode %}

<details>

<summary>Active</summary>

Defines if the webserver should be started

</details>

<details>

<summary>Port</summary>

{% hint style="warning" %}
If you are using docker, make sure to bind the ports correctly in your compose config.
{% endhint %}

The port under which the webserver will be occupying.&#x20;

</details>

<details>

<summary>Redirect Uri</summary>

The uri the webserver will be trying to catch incoming connections from the discord OAuth api from.

</details>

<details>

<summary>Uri</summary>

{% hint style="warning" %}
Make sure  you are including http://, the correct port and the redirect url, exactly as is
{% endhint %}

The full redirect uri. Make sure you use your correct url, port etc. This could look something like this: `http://localhost:8080/auth/discord/redirect`

</details>

{% code lineNumbers="true" %}
```yaml
webserver:
  # Should the webserver be launched? This feature is only used for regulars
  active: false
  # The port under which the webserver will be launched
  port: 8080
  # What uri to start the webserver under
  redirect_uri: "/auth/discord/redirect"
  # Where should the redirect be, include the full url e.g., https://localhost:80/auth/discord/redirect
  uri: ""
```
{% endcode %}

h
