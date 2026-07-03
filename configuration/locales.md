---
icon: language
---

# Files And Locales

xDiscord keeps global technical files in the plugin root. Locale-specific text and localized gameplay files stay inside `locales/<language>/`.

Default structure:

```text
plugins/xDiscord/config.yml
plugins/xDiscord/discord.yml

plugins/xDiscord/locales/en_US/database.yml
plugins/xDiscord/locales/en_US/gui.yml
plugins/xDiscord/locales/en_US/messages.yml
plugins/xDiscord/locales/en_US/rewards.yml

plugins/xDiscord/locales/pt_BR/database.yml
plugins/xDiscord/locales/pt_BR/gui.yml
plugins/xDiscord/locales/pt_BR/messages.yml
plugins/xDiscord/locales/pt_BR/rewards.yml
```

## Active Locale

The active locale is read from:

```text
plugins/xDiscord/config.yml
```

```yaml
settings:
  language: "pt_BR"
```

Change it to `en_US` if you want the plugin to use the English files.

Do not put `config.yml` or `discord.yml` inside a locale folder. `discord.yml` is global because token, guild ID, role IDs, command names, and channel IDs should not change per language.

All player-facing text, Discord modal text, Discord embeds, custom command responses, and Minecraft messages live in `messages.yml`.

## Automatic Updates

When a new version adds configuration keys, xDiscord applies defaults automatically without deleting your existing files.

If new keys do not appear immediately, run:

```text
/xdiscord reload
```
