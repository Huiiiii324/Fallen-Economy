# Buy Shop

`/shop` and `/buy` open the same native buy-only shop.

## Normal Shop

The normal shop uses `$` by default and is stored in:

```text
plugins/FallenEconomy/buy-shop.yml
```

Starter categories:

- End
- Nether
- Gear
- Food

Each item stores:

- `category`
- `currency`
- `item`
- `price`
- `created-at`

Admin add command:

```text
/buy config add <price> <category> [money|essence]
```

Example:

```text
/buy config add 350 Gear money
```

## Essence Shop

`/essenceshop` is separate and uses PlayerPoints Essence. It is stored in:

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
