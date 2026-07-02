---
icon: terminal
---

# Console no Discord

O xDiscord pode enviar logs do servidor para um canal e executar comandos enviados nesse canal.

```yaml
discord:
  console:
    enabled: true
    channel-id: "ID_DO_CANAL"
    min-level: "INFO"
    flush-interval-seconds: 5
    max-lines-per-message: 20
    commands:
      enabled: true
      strip-leading-slash: true
      confirm-execution: true
      allowed-role-ids: []
```

## Seguranca

Use `allowed-role-ids` para limitar quem pode executar comandos.

Se ficar vazio, qualquer pessoa com acesso ao canal pode executar comandos, dependendo da configuracao do canal.
