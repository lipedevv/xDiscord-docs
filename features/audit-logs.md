---
icon: clipboard-list
---

# Audit Logs

xDiscord stores important security and account events in the `xdiscord_audit` table.

File:

```text
plugins/xDiscord/config.yml
```

```yaml
audit:
  enabled: true
  log-to-console: true
  actions:
    - "*"
```

Recorded events include:

* `LINK`
* `UNLINK`
* `REWARD_CLAIM`
* `COMMAND_BLOCKED`
* `WORLD_BLOCKED`
* `WHITELIST_NOT_LINKED`
* `WHITELIST_DB_ERROR`

Set `log-to-console: false` if you want audit data only in the database.

To record only selected events:

```yaml
audit:
  enabled: true
  actions:
    - "LINK"
    - "UNLINK"
    - "WHITELIST_NOT_LINKED"
```
