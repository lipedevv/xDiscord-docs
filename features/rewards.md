---
icon: gift
---

# Recompensas

Arquivo:

```text
plugins/xDiscord/locales/<idioma>/rewards.yml
```

## Modo automatico

```yaml
rewards:
  enabled: true
  mode: "AUTO"
  only-first-link: true
  commands:
    - "lp user {player} permission set servidor.vinculado true"
    - "money give {player} 5000"
```

Nesse modo, os comandos rodam assim que a conta e vinculada.

## Modo manual

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
      name: "&a&lRESGATAR RECOMPENSA"
```

O jogador precisa abrir `/vincular` e clicar no item da recompensa.

## Anti-duplicacao

O plugin salva o resgate em `xdiscord_rewards`, impedindo resgate duplicado.
