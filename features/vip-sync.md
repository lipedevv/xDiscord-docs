---
icon: crown
---

# VIP Sync And Nickname

## Verified Role

```yaml
discord:
  verified-role-id: "ROLE_ID"
```

When the account is linked, the bot adds this role.

When the account is unlinked, the bot removes this role.

## VIP Sync

If the player has a Minecraft group or permission, the bot can add the matching Discord role.

```yaml
discord:
  vip-sync:
    enabled: true
    groups:
      - minecraft-group: "arcano"
        permission: "group.arcano"
        discord-role-id: "ARCANO_ROLE_ID"
      - minecraft-group: "mistico"
        permission: "group.mistico"
        discord-role-id: "MISTICO_ROLE_ID"
      - minecraft-group: "epico"
        permission: "group.epico"
        discord-role-id: "EPICO_ROLE_ID"
```

xDiscord tries to read the primary group from LuckPerms. If the player is online, it also checks the configured permission.

## Nickname Sync

```yaml
discord:
  nickname-sync:
    enabled: true
    format: "{player}"
```

Example result:

```text
Lipe_Tato
```

The bot needs `Manage Nicknames`.
