# Fallen Economy

Fallen Economy is a Paper 1.21.11 economy/shop setup for a PvP-focused survival server.
It combines EconomyShopGUI configs with a custom `FallenEconomy.jar` for configurable buy shop, auctions, and buy orders.

## Included

- `server-root/plugins/EconomyShopGUI/sections/`: section files for EconomyShopGUI v6+.
- `server-root/plugins/EconomyShopGUI/shops/`: buy-only shop categories and sell-only values.
- `server-root/plugins/FallenEconomy.jar`: custom `/buy`, `/ah`, and `/order` plugin.
- `server-root/commands.yml`: clean aliases for EconomyShopGUI sell commands.
- `docs/`: full setup and maintenance documentation.

## Core Behavior

- `/shop`: buy-only PvP/rare/supply server shop.
- `/sell`: sell interface alias for EconomyShopGUI.
- `/buy`: configurable server buy shop from `FallenEconomy.jar`.
- `/buy config`: admin buy-shop editor for adding/removing items and setting prices.
- `/ah`: auction house from `FallenEconomy.jar`.
- `/ah sell <price>`: lists the held item stack.
- `/order`: buy orders from `FallenEconomy.jar`.
- `/order create <unitPrice> <amount>`: creates an item order using the held item type.
- Currency display name: `Essence`.
- Sell values are generated from Paper API 1.21.11 materials.
- Sell values are coefficient-based: `baseValue * currencyPerPoint * optional multipliers`.

## Read Next

- `docs/INSTALLATION.md`: install steps.
- `docs/COMMANDS.md`: command map and aliases.
- `docs/PRICING.md`: coefficient pricing system.
- `docs/AUCTION_AND_ORDERS.md`: custom auction/order module.
- `docs/REGENERATE.md`: how to rebuild configs after price changes.
