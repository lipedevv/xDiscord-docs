---
icon: discord
---

# Discord Bot

File:

```text
plugins/xDiscord/discord.yml
```

## Main Configuration

```yaml
discord:
  enabled: true
  token: ""
  guild-id: ""
  invite-url: "https://discord.gg/yourserver"
  verified-role-id: ""
  command-name: "link"
  code-option-name: "code"
```

Texts such as bot status, command descriptions, modal labels, panel embeds, and command responses are configured in:

```text
plugins/xDiscord/locales/<locale>/messages.yml
```

## Creating The Bot

1. Open the Discord Developer Portal.
2. Create an application.
3. Open the `Bot` tab.
4. Create or copy the bot token.
5. Enable required intents if Discord asks for them.
6. Invite the bot with `applications.commands`.
7. If you use roles, give the bot `Manage Roles`.

## Recommended Bot Permissions

For all features:

* `applications.commands`
* `Manage Roles`
* `Manage Nicknames`
* Permission to read and send messages in the panel channel.
* The bot role must be above every role it will manage.
