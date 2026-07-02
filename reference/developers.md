---
icon: code
---

# API para desenvolvedores

O xDiscord registra uma API propria.

```java
XDiscordAPI api = XDiscordProvider.get();
```

Exemplo:

```java
api.links().findByPlayerUuid(player.getUniqueId()).thenAccept(optional -> {
    optional.ifPresent(link -> {
        String discordId = link.discordId();
    });
});
```

## xCore

Plugins novos devem depender de `xCore`:

```yaml
depend:
  - xCore
```

O xCore tambem fornece compatibilidade com o nome antigo `fCore`.

## Mensagens interativas

```java
core.messages().sendInteractive(
    player,
    "<green>Clique aqui",
    "<yellow>Copiar comando",
    "COPY",
    "/vincular ABC123"
);
```

Acoes aceitas:

```text
RUN_COMMAND
SUGGEST_COMMAND
OPEN_URL
COPY_TO_CLIPBOARD
```
