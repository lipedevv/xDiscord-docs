---
icon: message
---

# Messages

File:

```text
plugins/xDiscord/locales/<locale>/messages.yml
```

Messages support:

* Legacy colors with `&`.
* Hex and MiniMessage when sent through xCore.
* Internal placeholders.
* PlaceholderAPI, if installed.
* Multi-line message lists.

Example:

```yaml
prefix: "&a&lxDiscord &8» "

reward-claimed: "{prefix}&aReward claimed successfully."
command-blocked-not-linked: "{prefix}&cYou must link your Discord account before using this command."
```

## Hover And Click

xCore exposes an API for interactive messages:

```java
core.messages().sendInteractive(
    player,
    "<green>Click to copy",
    "<yellow>Copy command",
    "COPY",
    "/vincular ABC123"
);
```
