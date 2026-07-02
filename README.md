---
icon: link
cover: ./Logo%20xDiscord.png
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# xDiscord

**xDiscord** is a Minecraft + Discord account linking plugin for modern Paper/Spigot servers. It depends on **xCore** and provides account verification, Discord bot commands, rewards, a button/modal linking panel, Discord console logs, custom Discord commands, command blocking for unlinked players, and Discord role synchronization.

## Main Features

* Account linking with `/verificar` in Minecraft and `/vincular` in Discord.
* Discord linking panel with button, modal, and in-game accept/deny request.
* Fully configurable GUI for linking, linked account status, unlink confirmation, and reward claiming.
* Rewards in automatic or manual mode.
* SQLite and MySQL support with HikariCP.
* Verified role and VIP role synchronization from LuckPerms groups or permissions.
* Automatic Discord nickname synchronization.
* Command blocking for players who are not linked.
* Custom Discord slash commands.
* Discord ranking command `/top`.
* Localized configuration files under `plugins/xDiscord/locales/<locale>/`.

## Start Here

* [Installation](getting-started/installation.md)
* [Quickstart](getting-started/quickstart.md)
* [Files And Locales](configuration/locales.md)
* [Discord Bot](configuration/discord-bot.md)
