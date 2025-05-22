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

The SecretLab Api provides easy interaction and data handling with the:  [https://api.scpslgame.com](https://api.scpslgame.com)

## Usage

All methods for the `Secretlab Api` are located in the `io.github.vxrpenter.secretlab.SecretLab` class, and can easily impored with one line:

```kotlin
import io.github.vxrpenter.secretlab.SecretLab
```

The `SecretLab` class has to be supplied with the servers `api-key` and it's `account-id` before making any requests. This is a short representation of correct `SecretLab` invocation:

<pre class="language-kotlin"><code class="lang-kotlin">import io.github.vxrpenter.secretlab.SecretLab
<strong>
</strong><strong>fun main() {
</strong><strong>    val api = "API_KEY"
</strong>    val accountId = "ACCOUNT_ID"
    
    val secretLab = SecretLab(api, accountId)
}
</code></pre>

## Examples

Fetching server information through the `Secretlab Api`. This returns a `Server` object:

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
