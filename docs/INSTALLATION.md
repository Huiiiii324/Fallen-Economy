# Installation

Target server: Paper `1.21.11`.

## Required Plugins

- EconomyShopGUI v6+.
- Optional Vault-compatible economy provider. If Vault is missing, `FallenEconomy.jar` uses internal balances.
- Permission plugin, recommended: LuckPerms.

## Before Installing

Remove the old SellGUI plugin if it conflicts with EconomyShopGUI sell commands:

- remove the old SellGUI `.jar` from `plugins/`
- remove or archive the old SellGUI config folder
- restart the server after plugin changes

## Copy Files

Copy these paths into the server root:

```text
server-root/plugins/EconomyShopGUI/sections -> plugins/EconomyShopGUI/sections
server-root/plugins/EconomyShopGUI/shops    -> plugins/EconomyShopGUI/shops
server-root/plugins/FallenEconomy.jar        -> plugins/FallenEconomy.jar
server-root/commands.yml                    -> commands.yml
```

If `commands.yml` already exists, merge the `aliases:` section instead of replacing unrelated aliases.

## Reload

Use one of these:

```text
/sreload
```

or fully restart the server. Restarting is safer after adding/removing plugins.

## LuckPerms Baseline

```text
/lp group default permission set EconomyShopGUI.shop true
/lp group default permission set EconomyShopGUI.shop.all true
/lp group default permission set EconomyShopGUI.sellall true
/lp group default permission set EconomyShopGUI.sellall.all true
/lp group default permission set EconomyShopGUI.sellallitem true
/lp group default permission set EconomyShopGUI.sellallitem.all true
/lp group default permission set EconomyShopGUI.sellallhand true
/lp group default permission set EconomyShopGUI.sellallhand.all true
/lp group default permission set EconomyShopGUI.sellgui true
/lp group default permission set EconomyShopGUI.sellgui.all true
```

Optional admin/internal-balance permissions:

```text
/lp group admin permission set falleneconomy.admin true
```

## Verification

After install, test:

```text
/shop
/sell
/ah
/order
```

Expected behavior:

- `/shop` opens buy-only categories.
- `/sell` opens the sell GUI or sell command alias.
- `/ah` opens Fallen auction house.
- `/order` opens Fallen buy orders.
