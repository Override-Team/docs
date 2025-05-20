---
icon: user
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

# Regulars

Regulars provide an easy and reliable way to automatically give players roles based on playtime or xp earned. Regulars are created in the `./SCPToolsBot/regulars/`, you can find the folder structure down below:&#x20;

<div align="left"><figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure></div>

## Configuration

{% tabs %}
{% tab title="Manifest" %}
## Manifest

The manifest defines the regular group. It is the starting point of every regular folder and cannot be missing.

{% code lineNumbers="true" %}
```yaml
# The name of the group that will be displayed to the users
name: ""
# The description of the group that will be displayed to the users
description: ""
# The custom role will be a group role, given to all users that have selected this group
custom_role:
  use: false
  id: ""
```
{% endcode %}

<details>

<summary>Name</summary>

The name of the regular group that will be displayed to users

</details>

<details>

<summary>Description</summary>

The description of the regular role that will be displayed to the users

</details>

<details>

<summary>Custom Role</summary>

`Use` - Determines if a custom role is going to be used

{% hint style="warning" %}
Only works if `use` is active
{% endhint %}

`Id` - The id of the custom role

</details>
{% endtab %}

{% tab title="Config" %}
## Config

The config contains the configuration of the roles. It defines when to apply the roles/what requirements need to be met for them to be applied.

{% code lineNumbers="true" %}
```yaml

# The list of roles that will be available for users. To create more copy an already existing entry.
# To remove a regular, delete an entry.
roles: [
  {
    # The roleId of the role. Activate developer mode and right-click the role
    id: "",
    # The description of the role that will be displayed to the user
    description: "",
    # Which type of requirement do you want to use? The requirement_type will define if the role is given to the player when reaching a certain
    # playtime, a certain level, or both. Choose between the types: [PLAYTIME, XP, BOTH]
    requirement_type: "PLAYTIME",
    # Which playtime (in hours) does the user need to reach before getting the role?
    playtime_requirement: 25,
    # Which xp level (in end levels) should the user need to reach before getting the role?
    xp_requirement: 5
  }
]
```
{% endcode %}

<details>

<summary>Id</summary>

The id of the role that will be given to the user

</details>

<details>

<summary>Description</summary>

The description of the regular role that will  be displayed to the user

</details>

<details>

<summary>Requirement Type</summary>

The type of requirement that needs to be met for the role to be applied. Available types are:

`PLAYTIME`, `XP`, `BOTH`

</details>

<details>

<summary>Playtime Requirement</summary>

The playtime (in hours) that needs to be met for the role to apply

</details>

<details>

<summary>Xp Requirement</summary>

The xp (in levels) that needs to be met for the role to apply

</details>
{% endtab %}
{% endtabs %}
