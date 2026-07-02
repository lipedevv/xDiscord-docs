---
icon: triangle-alert
---

# Troubleshooting

## xDiscord Does Not Start

Make sure `xCore.jar` is in the `plugins/` folder.

## The Bot Keeps Thinking

Check the token, `guild-id`, and bot permissions. xDiscord uses `deferReply` and always tries to finish the response, but invalid token, invalid guild, or missing permissions can break interactions.

## Role Is Not Added

Check:

* `verified-role-id`
* VIP `discord-role-id`
* `Manage Roles` permission
* Discord role hierarchy

The bot role must be above every role it will manage.

## Nickname Does Not Change

Check:

* `discord.nickname-sync.enabled`
* `Manage Nicknames` permission
* Discord role hierarchy

## Panel Duplicates

Check `discord.link-panel.message-id`. xDiscord saves this ID automatically. If you clear it, the plugin will try to find an old bot message in the channel; if it cannot find one, it sends a new message.

## MySQL Does Not Connect

Check:

* host
* port
* database
* username/password
* firewall
* `useSSL`
