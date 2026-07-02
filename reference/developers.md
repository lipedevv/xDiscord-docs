---
icon: code
---

# Developer API

xDiscord registers its own public API.

```java
XDiscordAPI api = XDiscordProvider.get();
```

Example:

```java
api.links().findByPlayerUuid(player.getUniqueId()).thenAccept(optional -> {
    optional.ifPresent(link -> {
        String discordId = link.discordId();
    });
});
```

## xCore

New plugins should depend on `xCore`:

```yaml
depend:
  - xCore
```

xCore also provides compatibility with the old `fCore` name.

## Interactive Messages

```java
core.messages().sendInteractive(
    player,
    "<green>Click here",
    "<yellow>Copy command",
    "COPY",
    "/vincular ABC123"
);
```

Accepted actions:

```text
RUN_COMMAND
SUGGEST_COMMAND
OPEN_URL
COPY_TO_CLIPBOARD
```
