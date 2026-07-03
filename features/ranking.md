---
icon: ranking-star
---

# Discord Ranking

Command:

```text
/top type: time
/top type: money
/top type: fishing
```

## Configuration

File:

```text
plugins/xDiscord/discord.yml
```

```yaml
discord:
  top-command:
    enabled: true
    name: "top"
    option-name: "type"
    limit: 10
    types:
      money:
        placeholder: "%vault_eco_balance%"
      fishing:
        placeholder: "%fpesca_pescados%"
```

## Types

* `time`: uses native Minecraft playtime statistics.
* `money`: uses the configured placeholder.
* `fishing`: uses the configured placeholder.

Legacy aliases such as `tempo` and `pesca` are still accepted by the handler.

When a type depends on PlaceholderAPI, the ranking uses online players that return a numeric value for the configured placeholder.
