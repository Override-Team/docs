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

# SCPToolsBot

[![](https://img.shields.io/badge/Discord-%235865F2.svg?\&logo=discord\&logoColor=white)](https://discord.gg/cAXU9Y7T9a)

ScpToolsBot is an application to enhance your Scp Secret Laboratory server by providing quality-of-life features in combination with moderation and team management tools. It also integrates with plugins like CedMod to build on already existing infrastructure and to use features they offer.

## Quick Setup

Install the installer from the [latest release](https://github.com/Vxrpenter/SCPToolsBot/releases) or download it from the master branch:

<pre class="language-sh"><code class="lang-sh"><strong>sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/Vxrpenter/SCPToolsBot/master/installer.sh)"
</strong></code></pre>

For more (detailed) installation methods, look into the setup guide:

{% content-ref url="setup/getting-started.md" %}
[getting-started.md](setup/getting-started.md)
{% endcontent-ref %}

## Build Information

Full releases are marked as such in the release. If a release contains the `alpha` tag, it is experimental and features and more have not been tested fully.

Releases containing the `beta` tag are mostly tested but could still be considered unstable.

Releases will be marked as stable if they're thought to run well after testing. If a release is marked as unstable, it might not run well or produce bugs, for example, memory leaks

When a new build is released, it might take some time until the wiki is updated

Changelogs only contain the most important information, and small one-line changes will not be included if they don't have a major effect on stability and/or performance

### Special Thanks

* Special thanks goes to [ced777ric](https://github.com/ced777ric) who helped me a lot with the cedmod api integration, especially when trying to find the specific endpoints use case or usability
* Also to [SeekEDstroy](https://github.com/SeekEDstroy) for help with user id linking and for pointing out some bugs
* A big thank you goes [Kaeseekuchen](https://github.com/Kaeseekuchen) for providing many feature ideas, real server data and enviorments for testing and feature improvements

***

<div align="center"><img src="https://repobeats.axiom.co/api/embed/82101d834cd627138b1d62d9f205c25a6b1746e0.svg" alt=""></div>
