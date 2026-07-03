---
icon: message
---

# Messages

File:

```text
plugins/xDiscord/locales/<locale>/messages.yml
```

This is the single file for player-facing text:

* Minecraft chat messages.
* Discord panel embeds.
* Discord modal title, labels, and placeholders.
* Discord slash command descriptions.
* Discord custom command responses.
* Reward, whitelist, doctor, and error messages.

Messages support:

* Legacy colors with `&`.
* Hex and MiniMessage when sent through xCore.
* Internal placeholders.
* PlaceholderAPI, if installed.
* Multi-line message lists.

Example:

```yaml
prefix: "&a&lxDiscord &8> "

reward-claimed: "{prefix}&aReward claimed successfully."
command-blocked-not-linked: "{prefix}&cYou must link your Discord account before using this command."

discord:
  bot-status: "Use /verify in the server"
  link-panel:
    modal:
      title: "Link account"
      nick-label: "Your Minecraft nickname"
    embed:
      title: "Link your account"
```

## Hover And Click

xCore exposes an API for interactive messages:

```java
core.messages().sendInteractive(
    player,
    "<green>Click to copy",
    "<yellow>Copy command",
    "COPY",
    "/link ABC123"
);
```
