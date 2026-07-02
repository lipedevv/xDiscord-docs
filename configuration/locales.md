---
icon: language
---

# Files And Locales

xDiscord separates configuration files by locale.

Default structure:

```text
plugins/xDiscord/locales/en_US/config.yml
plugins/xDiscord/locales/en_US/database.yml
plugins/xDiscord/locales/en_US/discord.yml
plugins/xDiscord/locales/en_US/gui.yml
plugins/xDiscord/locales/en_US/messages.yml
plugins/xDiscord/locales/en_US/rewards.yml

plugins/xDiscord/locales/pt_BR/config.yml
plugins/xDiscord/locales/pt_BR/database.yml
plugins/xDiscord/locales/pt_BR/discord.yml
plugins/xDiscord/locales/pt_BR/gui.yml
plugins/xDiscord/locales/pt_BR/messages.yml
plugins/xDiscord/locales/pt_BR/rewards.yml
```

## Active Locale

The active locale is read from:

```text
plugins/xDiscord/locales/en_US/config.yml
```

```yaml
settings:
  language: "en_US"
```

Change it to `pt_BR` if you want the plugin to use the Portuguese files.

## Automatic Updates

When a new version adds configuration keys, xDiscord applies defaults automatically without deleting your existing files.

If new keys do not appear immediately, run:

```text
/xdiscord reload
```
