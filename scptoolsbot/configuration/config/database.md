---
icon: server
---

# Database

{% hint style="warning" %}
By default, the database does not need any extra configuration
{% endhint %}

You are able to configure the database the bot uses to your liking using these settings. Make sure you know what you are doing because the bot cannot function without a working database.

{% code lineNumbers="true" %}
```yaml
database:
  # Defines which datatype should be used, choose between [NONE, SQLITE]
  # ** WARNING ** if you set this to none, and no other database option is given, the process will crash on startup
  use_predefined_database_sets: "SQLITE"
  # ** WARNING ** When using custom, you may experience issues. This is a work in progress feature, so it is unstable, report problems on the GitHub page
  # Which type of custom db should be used: [SQLITE, MYSQL, POSTGRESQL, MARIADB]
  custom_type: ""
  # Here you can input a custom database url to connect to. Make sure to not include https:// or http://, just use the plain url for
  # database connection, e.g., < localhost:3306/test >
  custom_url: ""
  # Here you've input the custom db password
  custom_username: ""
  # Here you have to enter the password of your db session
  custom_password: ""
```
{% endcode %}

<details>

<summary>Use Predifined Database</summary>

The bot has databases that are already configured and ready to use without any setup. You can choose from:

`NONE`, `SQLITE`

</details>

<details>

<summary>Custom Type</summary>

The type of which database you use. Note that only SQL databases are supported, databases such as LiteDB will not work. The supported types are:

`SQLITE`, `MYSQL`, `POSTGRESQL`, `MARIADB`

</details>

<details>

<summary>Custom Url</summary>

{% hint style="warning" %}
If you are using docker, make sure to bind the ports correctly in your compose config.
{% endhint %}

The url to your database. Make sure to include the port, e.g. `localhost:3006/test`

</details>

<details>

<summary>Custom Username</summary>

Your database user.

</details>

<details>

<summary>Custom Password</summary>

The password to your database user.

</details>
