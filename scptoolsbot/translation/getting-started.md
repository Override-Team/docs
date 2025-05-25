---
icon: power-off
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

# Getting Started

The translations contain all messages/text that is displayed by ScpTools (excluding logs). It also comes with build in formatting code support.

## Creating a new translation

{% stepper %}
{% step %}
### Navigation

Navigate to .`/SCPToolsBot/lang/`
{% endstep %}

{% step %}
### Copy

Copy the `en_US` translation as a base
{% endstep %}

{% step %}
### Translate

Open up the translation and change everything except for the variables. Also make sure to leave all text that is surrounded like this `%var%` as is. You can use [markdown](https://support.discord.com/hc/en-us/articles/210298617-Markdown-Text-101-Chat-Formatting-Bold-Italic-Underline) and [#formatting-codes](getting-started.md#formatting-codes "mention")
{% endstep %}

{% step %}
### Rename

Rename your translation file like this: `language_Type`, e.g. de\_DE, en\_US, en\_UK
{% endstep %}

{% step %}
### Configure

Navigate to `./SCPToolsBot/configs/config.yml` and change load\_translation to your files name (excluding `.yml`). Find more configuration here [getting-started.md](../setup/getting-started.md "mention")
{% endstep %}
{% endstepper %}

## Formatting Codes

| Color Code        | Display                                                                                                   | Function                                            |
| ----------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| `&dark_gray&`     | <div><figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure></div>      | Apply the color gray                                |
| `&red&`           | <div><figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color red                                 |
| `&green&`         | <div><figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color green                               |
| `&gold&`          | <div><figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color gold                                |
| `&light_blue&`    | <div><figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color light blue                          |
| `&pink&`          | <div><figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color pink                                |
| `&teal&`          | <div><figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color teal                                |
| `&white&`         | <div><figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div>  | Apply the color white                               |
| `&bold&`          | <div><figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure></div>  | Apply bold                                          |
| `&reset&`         | <div><figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>  | Reset all colors, bold and underline                |
| `&underline&`     | <div><figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure></div> | Apply underline                                     |
| `&filler&`        | ---                                                                                                       | Fills up a whole row of an embed                    |
| `&singlefiller&`  | ---                                                                                                       | Adds a single empty character                       |
| `&filler<count>&` | ---                                                                                                       | Replace `<count>` with a number of blank characters |
