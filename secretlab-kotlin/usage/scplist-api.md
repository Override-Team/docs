---
icon: table-list
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

# Scplist Api

The `Scplist Api` integration provides easy interaction and data handling with the:  [https://scplist.kr/api](https://scplist.kr/api)

## Usage

All functions for the `Scplist Api` are located in the `io.github.vxrpenter.scplist.ScpList` class, and can easily imported with one line:

```kotlin
import io.github.vxrpenter.scplist.ScpList
```

The [`ScpList`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.scplist/-scp-list/index.html) class does not need to be supplied with anything This is a short representation of correct [`ScpList`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.scplist/-scp-list/index.html) invocation:

```kotlin
import io.github.vxrpenter.secretlab.SecretLab
    
val scpList =  ScpList() 
```

## Exceptions

All functions that are contained in the [`ScpList`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.scplist/-scp-list/index.html) class throw a [`CallFailureException`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.scplist.exceptions/-call-failure-exception/index.html) inherited from a [`ScpListException`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.scplist.exceptions/-scp-list-exception/index.html) when a call to the api fails for any reason. You can could catch it like this:

{% code lineNumbers="true" %}
```kotlin
try {
  val scpList = ScpList().server(ID)
} catch (e: Exception) {
  println("An error has occured during an scplist api call")
  return
}
```
{% endcode %}

## Examples

Fetching server information through the `ScpList Api`. This returns a [`Server`](https://vxrpenter.github.io/SecretLab-Kotlin/-secret-lab%20-kotlin/io.github.vxrpenter.scplist.data/-server/index.html) object:

{% code lineNumbers="true" %}
```kotlin
import io.github.vxrpenter.scplist.ScpList

fun main() {
    // Get players using the ScpListApi
    val players = ScpList().serverGet("ID")?.players
}
```
{% endcode %}
