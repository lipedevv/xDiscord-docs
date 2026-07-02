---
icon: database
---

# Banco de dados

Arquivo:

```text
plugins/xDiscord/locales/<idioma>/database.yml
```

## SQLite

Padrao:

```yaml
database:
  type: "sqlite"
  sqlite:
    file: "data/database.db"
```

O arquivo fica em:

```text
plugins/xDiscord/data/database.db
```

## MySQL

```yaml
database:
  type: "mysql"
  mysql:
    host: "localhost"
    port: 3306
    database: "minecraft"
    username: "root"
    password: ""
    useSSL: false
    pool-size: 10
```

## Tabelas

O plugin cria automaticamente:

```text
xdiscord_links
xdiscord_history
xdiscord_rewards
```

`xdiscord_rewards` guarda se a recompensa manual/automatica ja foi resgatada.
