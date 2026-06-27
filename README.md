# Fallen Economy

Server package for the standalone Fallen Economy plugin on Paper `1.21.11`.

`FallenEconomy.jar` now handles the normal `$` economy, shop, selling, auction house, and buy orders by itself. Essence is separate and comes from PlayerPoints for `/essence`, `/essenceshop`, spawners, keys, and future bounty integration.

## Included

- `server-root/plugins/FallenEconomy.jar`
- `server-root/plugins/FallenKillEffects.jar`
- `server-root/plugins/FallenEconomy/config.yml`
- `server-root/plugins/FallenKillEffects/config.yml`
- `server-root/plugins/FallenEconomy/buy-shop.yml`
- `server-root/plugins/FallenEconomy/essence-shop.yml`
- `server-root/plugins/FallenEconomy/sell-values.yml`

## Currency Split

- `$`: internal `money.yml`, used by `/shop`, `/sell`, `/ah`, `/order`, `/balance`, `/pay`, and Vault compatibility.
- `Essence`: PlayerPoints-backed, used by `/essence` and `/essenceshop`.

Vault is optional and exposes only `$`. PlayerPoints is optional for server startup, but required for Essence features.

## Main Commands

- `/shop`: normal `$` shop categories.
- `/shop edit`: normal `$` shop editor.
- `/essenceshop`: Essence shop, currently spawners.
- `/sell`, `/sell hand`, `/sell all`: sell items for `$`.
- `/balance`, `/bal`, `/money`, `/pay`: `$` balance and transfers.
- `/ah`: auction house using `$`.
- `/order`: buy orders using `$`.
- `/feconomy`: admin `$` and Essence management.

Shop item clicks open a confirmation GUI first. Players can choose the purchase amount with `-1`, `+1`, `-8`, `+8`, `-16`, `+16`, `-32`, `+32`, `-64`, and `+64`, then buy or cancel.

Utility tools can be issued as normal tools, owner-bound timed tools, or limited-use Sell Wands:

```text
/feconomy tools give <player> <pickaxe|shovel|axe>
/feconomy tools give timed <player> <pickaxe|shovel|axe> <hours>
/feconomy tools give <player> sellwand <uses>
```

Timed pickaxes, shovels, and axes are bound to the issued owner and only drain while that owner is online. Ownership can transfer only when the owner drops the tool or loses it on death. Sell Wand uses are consumed only after a successful container sale.

## Fallen Kill Effects

`FallenKillEffects.jar` adds `/killeffects` and `/killeffect`.

- GUI with selectable kill effects.
- Locked effects are bought with PlayerPoints Essence.
- Sovereign can use every effect for free through `fallenkilleffects.free` or `group.sovereign`.
- Player choices are stored in `plugins/FallenKillEffects/data.yml`.
