---
icon: ranking-star
---

# Discord Ranking

Command:

```text
/top tipo: tempo
/top tipo: money
/top tipo: pesca
```

## Configuration

File:

```text
plugins/xDiscord/locales/<locale>/discord.yml
```

```yaml
discord:
  top-command:
    enabled: true
    name: "top"
    option-name: "tipo"
    limit: 10
    types:
      money:
        placeholder: "%vault_eco_balance%"
      pesca:
        placeholder: "%fpesca_pescados%"
```

## Types

* `tempo`: uses native Minecraft playtime statistics.
* `money`: uses the configured placeholder.
* `pesca`: uses the configured placeholder.

When a type depends on PlaceholderAPI, the ranking uses online players that return a numeric value for the configured placeholder.
