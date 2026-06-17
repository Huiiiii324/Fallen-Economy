# Commands

The player-facing command set is intentionally short.

## Main Commands

| Command | Source | Purpose |
| --- | --- | --- |
| `/shop` | EconomyShopGUI | Buy-only server shop. |
| `/sell` | `commands.yml` alias | Opens EconomyShopGUI sell command. |
| `/sellhand` | `commands.yml` alias | Sells held item through EconomyShopGUI. |
| `/ah` | FallenEconomy.jar | Opens auction house. |
| `/auction` | FallenEconomy.jar alias | Opens auction house. |
| `/ah sell <price>` | FallenEconomy.jar | Lists held item stack. |
| `/ah sort <mode>` | FallenEconomy.jar | Sets auction sort. |
| `/ah cancel <id>` | FallenEconomy.jar | Cancels own auction. |
| `/order` | FallenEconomy.jar | Opens buy orders. |
| `/orders` | FallenEconomy.jar alias | Opens buy orders. |
| `/order create <unitPrice> <amount>` | FallenEconomy.jar | Creates a buy order for held item type. |
| `/order fill <id> [amount]` | FallenEconomy.jar | Fills an order with held items. |
| `/order cancel <id>` | FallenEconomy.jar | Cancels own order and refunds escrow. |

## Alias File

`server-root/commands.yml` contains:

```yaml
aliases:
  sell:
  - sellgui $1-
  sellhand:
  - sellall hand
```

`/ah`, `/auction`, `/order`, and `/orders` are provided by `FallenEconomy.jar`, so they do not need `commands.yml` aliases.

## Sort Modes

Supported sort modes:

```text
newest
oldest
price_asc
price_desc
amount
```

## EconomyShopGUI Notes

- Buy shop items use `sell: -1`, so they are buy-only in `/shop`.
- Sell value items use `buy: -1`, so they are sell-only.
- Pricing lore is hidden and replaced with custom `Essence` lore.
