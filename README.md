---
icon: link
cover: .gitbook/assets/Logo xDiscord.png
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
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# xDiscord

**xDiscord** is a Minecraft + Discord account linking plugin for modern Paper/Spigot servers. It depends on **xCore** and provides account verification, Discord bot commands, rewards, a button/modal linking panel, Discord console logs, custom Discord commands, command blocking for unlinked players, and Discord role synchronization.

## Main Features

* Account linking with `/verify` in Minecraft and `/link` in Discord.
* Discord linking panel with button, modal, and in-game accept/deny request.
* Fully configurable GUI for linking, linked account status, unlink confirmation, and reward claiming.
* Rewards in automatic or manual mode.
* SQLite and MySQL support with HikariCP.
* Verified role and VIP role synchronization from LuckPerms groups or permissions.
* Automatic Discord nickname synchronization.
* Command blocking and world restrictions for players who are not linked.
* Optional Discord whitelist for already linked players, disabled by default.
* Persistent audit logs for link, unlink, reward, command block, world block, and whitelist events.
* `/xdiscord doctor` diagnostics for setup checks.
* Custom Discord slash commands.
* Discord ranking command `/top`.
* Localized configuration files under `plugins/xDiscord/locales/<locale>/`.

## Start Here

* [Installation](getting-started/installation.md)
* [Quickstart](getting-started/quickstart.md)
* [Files And Locales](configuration/locales.md)
* [Discord Bot](configuration/discord-bot.md)
