---
icon: message
---

# Mensagens

Arquivo:

```text
plugins/xDiscord/locales/<idioma>/messages.yml
```

As mensagens suportam:

* Cores legacy com `&`.
* Hex e MiniMessage quando enviado pelo xCore.
* Placeholders internos.
* PlaceholderAPI, se instalada.
* Mensagens em lista.

Exemplo:

```yaml
prefix: "&a&lxDiscord &8» "

reward-claimed: "{prefix}&aRecompensa resgatada com sucesso."
command-blocked-not-linked: "{prefix}&cVoce precisa vincular sua conta do Discord para usar esse comando."
```

## Hover e click

O xCore possui API para mensagens interativas:

```java
core.messages().sendInteractive(
    player,
    "<green>Clique para copiar",
    "<yellow>Copiar comando",
    "COPY",
    "/vincular ABC123"
);
```
