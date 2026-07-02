---
icon: gift
---

# Rewards

File:

```text
plugins/xDiscord/locales/<locale>/rewards.yml
```

## Automatic Mode

```yaml
rewards:
  enabled: true
  mode: "AUTO"
  only-first-link: true
  commands:
    - "lp user {player} permission set server.linked true"
    - "money give {player} 5000"
```

In this mode, commands run as soon as the account is linked.

## Manual Mode

```yaml
rewards:
  mode: "MANUAL"
  manual:
    item:
      enabled: true
      slot: 15
      material: "PLAYER_HEAD"
      head:
        type: "URL"
        value: "http://textures.minecraft.net/texture/5b85e29f29ec9a90e482ea5b8391bcb4560bbae0dcd15d7ce1d86016b4356e98"
      name: "&a&lCLAIM REWARD"
```

The player must open `/vincular` and click the reward item.

## Duplicate Protection

xDiscord stores reward claims in `xdiscord_rewards`, preventing duplicate claims.
