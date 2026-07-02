---
icon: crown
---

# Sync VIP e nickname

## Cargo verificado

```yaml
discord:
  verified-role-id: "ID_DO_CARGO"
```

Ao vincular, o bot adiciona esse cargo.

Ao desvincular, o bot remove esse cargo.

## VIP sync

Se o jogador tiver grupo/permissao no Minecraft, o bot adiciona cargo correspondente no Discord.

```yaml
discord:
  vip-sync:
    enabled: true
    groups:
      - minecraft-group: "arcano"
        permission: "group.arcano"
        discord-role-id: "ID_CARGO_ARCANO"
      - minecraft-group: "mistico"
        permission: "group.mistico"
        discord-role-id: "ID_CARGO_MISTICO"
      - minecraft-group: "epico"
        permission: "group.epico"
        discord-role-id: "ID_CARGO_EPICO"
```

O plugin tenta ler o grupo primario do LuckPerms. Se o jogador estiver online, tambem confere a permissao configurada.

## Nickname sync

```yaml
discord:
  nickname-sync:
    enabled: true
    format: "{player}"
```

Exemplo final:

```text
Lipe_Tato
```

O bot precisa de `Manage Nicknames`.
