---
icon: link
---

# Account Linking

The main flow uses a temporary code.

## Minecraft

```text
/verify
```

The player opens the GUI, clicks the link item, and receives a code.

## Discord

```text
/link code: ABC123
```

When the code is valid:

* The link is saved in the database.
* The verified role can be applied.
* Rewards can be executed or made available for manual claiming.
* VIP sync can apply Discord roles.
* Nickname sync can change the member nickname in Discord.

## Unlinking

In the GUI, if the player is already linked, the main item can open the unlink confirmation menu.

Admin commands:

```text
/verify unlink <player>
/xdiscord unlink <player>
```
