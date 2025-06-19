---
icon: house
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

# SecretLab Kotlin

[![](https://img.shields.io/github/v/release/Vxrpenter/SecretLab-Kotlin?include_prereleases\&logo=github\&logoColor=black\&logoSize=amg\&labelColor=333834\&sort=date\&display_name=tag\&style=for-the-badge\&label=LATEST%20RELEASE\&color=green)](https://github.com/Vxrpenter/SecretLab-Kotlin/releases) [![](https://img.shields.io/maven-central/v/io.github.vxrpenter/secretlab-kotlin?style=for-the-badge\&logo=apache\&logoColor=red\&logoSize=amg\&labelColor=333834\&color=red)](https://central.sonatype.com/artifact/io.github.vxrpenter/secretlab-kotlin)&#x20;

{% hint style="warning" %}
Currently endpoint integration is still not finished
{% endhint %}

SecretLab Kotlin is a SCP: Secret Laboratory api wrapper. It includes compatibility with the main api, cedmod etc.

## Installation

{% tabs %}
{% tab title="Gradle (Kotlin)" %}
```kotlin
dependencies {
  implementation("io.github.vxrpenter:secretlab-kotlin:0.4.3")
}
```
{% endtab %}

{% tab title="Gradle (Groovy)" %}
```groovy
dependencies {
  implementation 'io.github.vxrpenter:secretlab-kotlin:0.4.3'
}
```
{% endtab %}

{% tab title="Maven" %}
```xml
<dependency>
    <groupId>io.github.vxrpenter</groupId>
    <artifactId>secretlab-kotlin</artifactId>
    <version>0.4.3</version>
</dependency>
```
{% endtab %}
{% endtabs %}

## Compatibility (short)

This is a short overview of all implemented api's. You can learn more about each by clicking on the link in the endpoints tab. It will present you with all endpoints information and their implementation state.

| Api                   | Implementation Begon | Completed            | link                         | Usage                                                | Endpoints                                                |
| --------------------- | -------------------- | -------------------- | ---------------------------- | ---------------------------------------------------- | -------------------------------------------------------- |
| Secret Laboratory Api | :white\_check\_mark: | :white\_check\_mark: | https://api.scpslgame.com/   | [secretlab-api.md](usage/secretlab-api.md "mention") | [secretlab-api.md](endpoints/secretlab-api.md "mention") |
| Cedmod Api            | :white\_check\_mark: | :x:                  | `Only available on instance` | [cedmod-api.md](usage/cedmod-api.md "mention")       | [cedmod-api.md](endpoints/cedmod-api.md "mention")       |
| Scplist Api           | :white\_check\_mark: | :white\_check\_mark: | https://scplist.kr/api       | [scplist-api.md](usage/scplist-api.md "mention")     | [scplist-api.md](endpoints/scplist-api.md "mention")     |

***

<div align="center"><img src="https://repobeats.axiom.co/api/embed/33474016edce12e76d8b6f721f57a86af6c1874a.svg" alt=""></div>
