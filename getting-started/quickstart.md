---
icon: rocket
---

# Configuracao rapida

Depois de instalar `xCore.jar` e `xDiscord.jar`, inicie o servidor uma vez para gerar os arquivos.

## 1. Escolha o idioma

O idioma padrao e `en_US`. Para usar portugues:

```yaml
settings:
  language: "pt_BR"
```

Arquivo:

```text
plugins/xDiscord/locales/en_US/config.yml
```

Reinicie ou use `/xdiscord reload`.

## 2. Configure o bot

Arquivo:

```text
plugins/xDiscord/locales/pt_BR/discord.yml
```

Campos principais:

```yaml
discord:
  enabled: true
  token: "TOKEN_DO_BOT"
  guild-id: "ID_DO_SERVIDOR"
  invite-url: "https://discord.gg/seuservidor"
  verified-role-id: "ID_DO_CARGO_VERIFICADO"
```

## 3. Configure o banco

SQLite vem pronto por padrao:

```yaml
database:
  type: "sqlite"
  sqlite:
    file: "data/database.db"
```

Para MySQL, veja [Banco de dados](../configuration/database.md).

## 4. Use no jogo

No Minecraft:

```text
/verificar
```

No Discord:

```text
/vincular codigo: ABC123
```

Ou use o painel com botao/modal, se estiver ativado.
