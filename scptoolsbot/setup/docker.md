---
icon: docker
---

# Docker

{% hint style="warning" %}
The image itself, that it provided on [docker hub](https://hub.docker.com/repository/docker/vxrpenter/scptoolsbot) can run without a compose file, but will not work, due to the missing configuration bind. You have to download the compose config, as well as the `.env` to run the bot.
{% endhint %}

You can just download the `docker-compose.yml` and `.env` file and run docker compose to start up the image. If you want to change the bind location of the configs, go into the `.env` file and change the location to whatever you like.

{% tabs %}
{% tab title="Linux" %}
## Linux

Make sure you have docker, as well as docker compose installed on your system. If docker is not running, activate it with `sudo systemctl start docker`

<pre class="language-sh"><code class="lang-sh"><strong>mkdir ScpToolsBot
</strong>
cd ScpToolsBot

curl -L https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/docker-compose.yml

curl -L https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/.env

sudo docker compose up
</code></pre>
{% endtab %}

{% tab title="Windows" %}
## Windows

{% hint style="warning" %}
This install is not recommended and not encouraged. All errors during installation are **YOUR** responsibility
{% endhint %}

```powershell
mkdir ScpToolsBot

cd ScpToolsBot

iwr -outf docker-compose.yml https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/docker-compose.yml

iwr -outf .env https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/.env

docker compose up
```
{% endtab %}

{% tab title="MacOS" %}
## MacOS

{% hint style="warning" %}
This install is not recommended and not encouraged. All errors during installation are **YOUR** responsibility
{% endhint %}

```sh
mkdir ScpToolsBot

cd ScpToolsBot

curl -L https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/docker-compose.yml

curl -L https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/.env

sudo docker compose up
```
{% endtab %}
{% endtabs %}

***

If you want to build the image yourself you have to clone the repository and change the `docker-compose.yml` to this.

<pre class="language-yml" data-line-numbers><code class="lang-yml">services:
  bot:
    build: .
    ports:
      - "8080:8080"
    volumes:
<strong>      - ${CONFIG_PATH}/SCPToolsBot/:/bot/SCPToolsBot/
</strong></code></pre>
