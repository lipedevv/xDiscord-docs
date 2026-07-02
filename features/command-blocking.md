---
icon: shield-x
---

# Bloqueio de comandos

Voce pode bloquear comandos para quem nao esta vinculado.

Arquivo:

```text
plugins/xDiscord/locales/<idioma>/config.yml
```

```yaml
blocked-commands-if-not-linked:
  enabled: true
  bypass-permission: "xdiscord.bypasslink"
  commands:
    - "kit"
    - "mercado"
    - "money pay"
```

O bloqueio usa prefixo. Se configurar `money pay`, apenas comandos que comecam com `money pay` serao bloqueados.

Mensagem:

```yaml
command-blocked-not-linked: "{prefix}&cVoce precisa vincular sua conta do Discord para usar esse comando."
```
