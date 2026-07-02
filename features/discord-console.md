---
icon: terminal
---

# Discord Console

xDiscord can send server logs to a Discord channel and execute commands sent in that channel.

```yaml
discord:
  console:
    enabled: true
    channel-id: "CHANNEL_ID"
    min-level: "INFO"
    flush-interval-seconds: 5
    max-lines-per-message: 20
    commands:
      enabled: true
      strip-leading-slash: true
      confirm-execution: true
      allowed-role-ids: []
```

## Security

Use `allowed-role-ids` to restrict who can execute commands.

If it is empty, anyone with access to the channel may be able to execute commands, depending on the channel permissions.
