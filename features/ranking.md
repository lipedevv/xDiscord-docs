---
icon: ranking-star
---

# Ranking no Discord

Comando:

```text
/top tipo: tempo
/top tipo: money
/top tipo: pesca
```

## Configuracao

Arquivo:

```text
plugins/xDiscord/locales/<idioma>/discord.yml
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

## Tipos

* `tempo`: usa estatistica nativa do Minecraft.
* `money`: usa placeholder configurado.
* `pesca`: usa placeholder configurado.

Quando o tipo depende de PlaceholderAPI, o ranking usa os jogadores online que possuem valor no placeholder.
