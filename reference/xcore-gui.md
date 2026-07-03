---
icon: table-cells
---

# xCore GUI And Items

xDiscord is built on top of xCore menus, items, and heads. You can use the same API in your own plugins.

## Getting xCore

Add `xCore` as a dependency in `plugin.yml`:

```yaml
depend:
  - xCore
```

Then get the API:

```java
import com.felipedevv.xCore.api.XCoreAPI;
import com.felipedevv.xCore.api.XCoreProvider;

XCoreAPI core = XCoreProvider.get();
```

Some builder classes still live under `com.felipedevv.fCore.api.*` for compatibility.

## Creating Items

```java
import com.felipedevv.fCore.api.item.ItemBuilder;
import org.bukkit.Material;
import org.bukkit.inventory.ItemStack;

ItemStack item = ItemBuilder.of(Material.DIAMOND)
    .name("&b&lSpecial Diamond")
    .lore(
        "&7This item was created with xCore.",
        "",
        "&eClick to use."
    )
    .amount(1)
    .glow(true)
    .customModelData(10)
    .build();
```

Useful methods:

```java
ItemBuilder.of(Material.PLAYER_HEAD);
ItemBuilder.from(existingItem);
builder.name("&aName");
builder.lore("&7Line 1", "&7Line 2");
builder.amount(5);
builder.glow(true);
builder.customModelData(123);
builder.placeholder("player", player.getName());
```

## Creating Heads

Player head:

```java
ItemStack head = core.heads().getPlayerHead(player);
```

Head by name:

```java
ItemStack head = core.heads().getPlayerHead("Steve");
```

Head by texture URL:

```java
ItemStack head = ItemBuilder.of(Material.PLAYER_HEAD)
    .headTextureUrl("http://textures.minecraft.net/texture/...")
    .name("&aCustom Head")
    .lore("&7Texture from Minecraft textures.")
    .build();
```

Head with `HeadBuilder`:

```java
import com.felipedevv.fCore.api.head.HeadBuilder;

ItemStack profileHead = HeadBuilder.create()
    .player(player)
    .name("&a{player}")
    .lore("&7Click to open profile.")
    .placeholder("player", player.getName())
    .glow(true)
    .build();
```

Supported head sources:

```java
HeadBuilder.create().player(player);
HeadBuilder.create().playerName("Steve");
HeadBuilder.create().uuid(uuid);
HeadBuilder.create().base64(base64);
HeadBuilder.create().textureUrl(url);
```

## Creating A Menu

```java
import com.felipedevv.fCore.api.menu.Menu;
import com.felipedevv.fCore.api.item.ItemBuilder;
import org.bukkit.Material;

Menu menu = core.menus().builder()
    .title("&8Example Menu")
    .size(27)
    .button(13, ItemBuilder.of(Material.PLAYER_HEAD)
        .headPlayer(player.getName())
        .name("&aYour Profile")
        .lore("&7Click to view your profile.")
        .build(), event -> {
            event.setCancelled(true);
            player.sendMessage("Clicked profile!");
        })
    .build();

menu.open(player);
```

Slots are zero-based. In a 27-slot menu, slot `13` is the center.

## Fill And Decorative Items

Use fill only when the menu actually needs a framed background. For cleaner menus, leave it out.

```java
ItemStack glass = ItemBuilder.of(Material.GRAY_STAINED_GLASS_PANE)
    .name(" ")
    .build();

Menu menu = core.menus().builder()
    .title("&8Filled Menu")
    .size(27)
    .fill(glass)
    .decorative(10, ItemBuilder.of(Material.BOOK).name("&eInfo").build())
    .build();
```

## Creating Items From Config

xCore can build items from a `ConfigurationSection`:

```yaml
profile-item:
  material: "PLAYER_HEAD"
  use-player-head: true
  name: "&aProfile of {player}"
  lore:
    - "&7Discord: &f{discord}"
    - ""
    - "&eClick to open."
  glow: true
  custom-model-data: 0
```

```java
Map<String, String> placeholders = Map.of(
    "player", player.getName(),
    "discord", "felipe"
);

ItemStack item = core.items().fromConfig(section, player, placeholders);
```

Custom head from config:

```yaml
reward:
  material: "PLAYER_HEAD"
  use-player-head: false
  head:
    type: "URL" # PLAYER, NAME, UUID, BASE64, URL
    value: "http://textures.minecraft.net/texture/..."
  name: "&aReward"
  lore:
    - "&7Click to claim."
```

## xDiscord Default GUI

The default xDiscord link GUI is intentionally simple:

```yaml
gui:
  size: 27
  fill:
    enabled: false
  item:
    slot: 13
    material: "PLAYER_HEAD"
    use-player-head: true
```

This opens a 27-slot inventory without filler and places the player head in the center.
