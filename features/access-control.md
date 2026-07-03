---
icon: lock
---

# Access Control

xDiscord can restrict unlinked players in two ways.

## Protected Worlds

File:

```text
plugins/xDiscord/config.yml
```

```yaml
required-verification:
  cache-on-join: true
  bypass-permission: "xdiscord.bypasslink"
  worlds:
    enabled: false
    names:
      - "survival"
    deny-commands:
      - "spawn {player}"
```

When enabled, an unlinked player found in one of the configured worlds receives a message and the configured console commands run.

Common use cases:

* Send the player back to spawn or lobby.
* Block survival, mines, farms, or economy worlds until the account is linked.
* Keep staff exempt with `xdiscord.bypasslink`.

## Discord Whitelist

The Discord whitelist is disabled by default.

```yaml
discord-whitelist:
  enabled: false
  lookup-timeout-seconds: 5
  allow-on-database-error: false
  allowed-player-names: []
```

When enabled, only players already linked in the xDiscord database can join. This is strict: new players who are not linked yet are kicked before joining.

Use it only when your server has an external or staff-assisted linking flow, or when you want a private linked-only server.
