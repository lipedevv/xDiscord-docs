---
icon: square-cursor
---

# Discord Panel

The Discord panel allows players to start linking from Discord.

Flow:

1. The bot sends or edits an embed in a channel.
2. The user clicks the button.
3. A modal asks for the Minecraft username.
4. Minecraft receives a link request.
5. The player accepts by clicking the chat message or running `/link accept`.

## Configuration

```yaml
discord:
  link-panel:
    enabled: true
    channel-id: "CHANNEL_ID"
    message-id: ""
    button-id: "xdiscord_link_open"
    button-label: "Link account"
```

`message-id` is filled automatically. On restart or reload, the bot edits the existing message instead of sending a duplicate.
