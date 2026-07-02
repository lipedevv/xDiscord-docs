---
icon: database
---

# Database

File:

```text
plugins/xDiscord/locales/<locale>/database.yml
```

## SQLite

Default:

```yaml
database:
  type: "sqlite"
  sqlite:
    file: "data/database.db"
```

The file is stored at:

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

## Tables

xDiscord creates these tables automatically:

```text
xdiscord_links
xdiscord_history
xdiscord_rewards
```

`xdiscord_rewards` stores whether the automatic/manual reward has already been claimed.
