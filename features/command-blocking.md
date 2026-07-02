---
icon: shield-x
---

# Command Blocking

You can block commands for players who are not linked.

File:

```text
plugins/xDiscord/locales/<locale>/config.yml
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

The match is prefix-based. If you configure `money pay`, only commands starting with `money pay` will be blocked.

Message:

```yaml
command-blocked-not-linked: "{prefix}&cYou must link your Discord account before using this command."
```
