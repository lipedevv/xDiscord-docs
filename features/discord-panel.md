---
icon: square-cursor
---

# Painel no Discord

O painel permite vincular pelo Discord.

Fluxo:

1. O bot envia/edita um embed em um canal.
2. O usuario clica no botao.
3. Um modal pede o nick do Minecraft.
4. O Minecraft recebe uma solicitacao.
5. O jogador aceita com clique no chat ou `/vincular aceitar`.

## Configuracao

```yaml
discord:
  link-panel:
    enabled: true
    channel-id: "ID_DO_CANAL"
    message-id: ""
    button-id: "xdiscord_link_open"
    button-label: "Vincular conta"
```

`message-id` e preenchido automaticamente. Ao reiniciar ou usar reload, o bot edita a mensagem existente em vez de mandar outra.
