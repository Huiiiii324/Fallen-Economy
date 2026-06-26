# Buy Shop

`/shop` opens the native buy-only shop.

Clicking a shop item opens a confirmation GUI instead of buying instantly. Players can change the purchase amount with `-1`, `+1`, `-8`, `+8`, `-16`, `+16`, `-32`, `+32`, `-64`, and `+64`, then choose Buy or Do Not Buy.

## Normal Shop

The normal shop uses `$` by default and is stored in:

```text
plugins/FallenEconomy/buy-shop.yml
```

Starter `$` categories:

- End
- Nether
- Gear
- Food

Spawner and other special Essence items are intentionally not shown in `/shop`. They live in `/essenceshop`.

Each item stores:

- `category`
- `item`
- `price`
- `created-at`

`price` is the cost of the configured item stack. If an entry is `16x End Stone` for `80`, buying `32x` costs `160`.

Admin add command for normal `$` shop entries:

```text
/shop edit add <price> <category>
```

Example:

```text
/shop edit add 350 Gear
```

## Essence Shop

`/essenceshop` is the player/admin view for special Essence items. It is stored in:

```text
plugins/FallenEconomy/essence-shop.yml
```

Starter category:

- Spawners

Admin add command:

```text
/essenceshop config add <price> <category>
```

Spawner shop entries use real `SPAWNER` items with `entity-type` stored through Bukkit item metadata. `Arrow of Slow Falling` uses a real `TIPPED_ARROW` with Slow Falling potion data.
