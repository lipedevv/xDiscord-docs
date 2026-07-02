---
icon: rocket
---

# Quickstart

After installing `xCore.jar` and `xDiscord.jar`, start the server once to generate the configuration files.

## 1. Choose The Locale

The default locale is `en_US`. To use Brazilian Portuguese:

```yaml
settings:
  language: "pt_BR"
```

File:

```text
plugins/xDiscord/locales/en_US/config.yml
```

Restart the server or run `/xdiscord reload`.

## 2. Configure The Bot

File:

```text
plugins/xDiscord/locales/en_US/discord.yml
```

Main fields:

```yaml
discord:
  enabled: true
  token: "BOT_TOKEN"
  guild-id: "SERVER_ID"
  invite-url: "https://discord.gg/yourserver"
  verified-role-id: "VERIFIED_ROLE_ID"
```

## 3. Configure The Database

SQLite works out of the box:

```yaml
database:
  type: "sqlite"
  sqlite:
    file: "data/database.db"
```

For MySQL, see [Database](../configuration/database.md).

## 4. Use It In Game

In Minecraft:

```text
/verificar
```

In Discord:

```text
/vincular codigo: ABC123
```

You can also use the Discord panel with button/modal if enabled.
