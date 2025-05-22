---
icon: mask
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

# Secretlab Api

The `SecretLab Api` integration provides easy interaction and data handling with the:  [https://api.scpslgame.com](https://api.scpslgame.com)

## Usage

All functions for the `Secretlab Api` are located in the `io.github.vxrpenter.secretlab.SecretLab` class, and can easily imported with one line:

```kotlin
import io.github.vxrpenter.secretlab.SecretLab
```

The [`SecretLab`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.secretlab/-secret-lab/index.html) class has to be supplied with the servers `api-key` and it's `account-id` before making any requests. This is a short representation of correct [`SecretLab`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.secretlab/-secret-lab/index.html) invocation:

<pre class="language-kotlin"><code class="lang-kotlin">import io.github.vxrpenter.secretlab.SecretLab
<strong>
</strong>val api = "API_KEY"
val accountId = "1235644644"
    
val secretLab = SecretLab(api, accountId)    
</code></pre>

## Exceptions

All functions that are contained in the [`SecretLab`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.secretlab/-secret-lab/index.html) class throw a [`CallFailureException`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.secretlab.exceptions/-call-failure-exception/index.html) inherited from a [`SecretLabException`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.secretlab.exceptions/-secret-lab-exception/index.html) when a call to the api fails for any reason. You can could catch it like this:

{% code lineNumbers="true" %}
```kotlin
try {
  val secretLab = SecretLab(api, accountId).ip()
} catch (e: Exception) {
  println("An error has occured during an secretlab api call")
  return
}
```
{% endcode %}

## Examples

Fetching server information through the `Secretlab Api`. This returns a [`Server`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.secretlab.data/-server/index.html) object:

{% code lineNumbers="true" %}
```kotlin
import io.github.vxrpenter.secretlab.SecretLab

fun main() {
    // The server-specific api key can be obtained by typing !api show into the server console
    val api = "API_KEY"
    // The account id can be optained by the same way
    val accountId = "ACCOUNT_ID"
    
    // Get current online players using the SecretLab Api
    val players = SecretLab(api, accountId).serverInfo(false, players = true)?.servers?.get(0)?.players
}
```
{% endcode %}
