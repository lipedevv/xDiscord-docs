---
icon: download
---

# Installation

## Requirements

* Modern Paper/Spigot server.
* Java 21 or newer.
* `xCore.jar` installed.
* `xDiscord.jar` installed.
* A Discord bot created in the Discord Developer Portal.

## Files

Place both jars in your server `plugins/` folder:

```text
plugins/
  xCore.jar
  xDiscord.jar
```

`xDiscord` requires `xCore`:

```yaml
depend:
  - xCore
```

`xCore` also provides compatibility with the old `fCore` plugin name, so older plugins can keep working while you migrate.

## First Start

Start the server once. xDiscord will create:

```text
plugins/xDiscord/locales/en_US/
plugins/xDiscord/locales/pt_BR/
plugins/xDiscord/data/
```

Then configure the locale, Discord bot, and database.
