---
icon: hammer-brush
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

# CedMod Api

The `CedMod Api` integration provides easy interaction and data handling of the api of [https://cedmod.nl/](https://cedmod.nl/)

## Usage

All functions for the `CedMod Api` are located in the `io.github.vxrpenter.cedmod.Cedmod` class, and can easily imported with one line:

<pre class="language-kotlin"><code class="lang-kotlin"><strong>import io.github.vxrpenter.cedmod.Cedmod
</strong></code></pre>

The [`Cedmod`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.cedmod/-cedmod/index.html) class has to be supplied with the servers `api-key` and it's `instance-url` before making any requests. This is a short representation of correct [`Cedmod`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.cedmod/-cedmod/index.html) invocation:

{% code lineNumbers="true" %}
```kotlin
import io.github.vxrpenter.cedmod.Cedmod

val api = "API_KEY"
val instanceUrl = "https://myservername.cmod.app"

val cedmod = Cedmod(api, instanceUrl)
```
{% endcode %}

## Exceptions

All functions that are contained in the [`Cedmod`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.cedmod/-cedmod/index.html) class throw a [`CallFailureException`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.cedmod.exceptions/-call-failure-exception/index.html) inherited from a [`CedmodException`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.cedmod.exceptions/-cedmod-exception/index.html) when a call to the api fails for any reason. You can could catch it like this:

{% code lineNumbers="true" %}
```kotlin
try {
  val cedmod = Cedmod(api, instanceUrl).changelogGet()
} catch (e: Exception) {
  println("An error has occured during an cedmod api call")
  return
}
```
{% endcode %}

## Examples

Issuing a ban for a user, using the `CedMod Api`. This returns a status code of the interaction

{% code lineNumbers="true" %}
```kotlin
import io.github.vxrpenter.cedmod.Cedmod

fun main() {
    // The api key of the server. This can only be obtained after asking cedmod staff to active it for the specific instance
    val api = "API_KEY"
    // Url of the instance being normally https://myservername.cmod.app
    val instanceUrl = "INSTANCE_URL"

    // Issues a ban to the cedmod api. The userId is typically steam/discord id with @steam or @discord attached.
    Cedmod(api, instanceUrl).banPostIssue(userId = "USER_ID@steam", reason = "REASON", duration = 1, appealable = true, banlists = listOf(1111))
}
```
{% endcode %}

Fetching a player and their stats using the `CedMod Api`. This returns a [`Player`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.cedmod.data/-player/index.html) object

```kotlin
import io.github.vxrpenter.cedmod.Cedmod

fun main() {
    // The api key of the server. This can only be obtained after asking cedmod staff to active it for the specific instance
    val api = "API_KEY"
    // Url of the instance being normally https://myservername.cmod.app
    val instanceUrl = "INSTANCE_URL"
    
    val steamId = "USER_ID"

    // Returns a player object with stats like playtime, kills etc.
    val player = (api, instanceUrl).playerQuery(q = "$steamId@steam", activityMin = 365, basicStats = true)
}
```
