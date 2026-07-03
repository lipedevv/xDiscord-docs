---
icon: rocket
---

# Quickstart

After installing `xCore.jar` and `xDiscord.jar`, start the server once to generate the configuration files.

## 1. Choose The Locale

The default locale is `pt_BR`. To use English:

```yaml
settings:
  language: "en_US"
```

File:

```text
plugins/xDiscord/config.yml
```

Restart the server or run `/xdiscord reload`.

## 2. Configure The Bot

File:

```text
plugins/xDiscord/discord.yml
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
/verify
```

In Discord:

```text
/link code: ABC123
```

You can also use the Discord panel with button/modal if enabled.
