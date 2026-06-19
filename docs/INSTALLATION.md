# Installation

Target server: Paper `1.21.11`.

Required:

```text
plugins/FallenEconomy.jar
```

Optional:

- `PlayerPoints.jar` for Essence, `/essence`, and `/essenceshop`
- `Vault.jar` if other plugins need to read/write Fallen `$`

Not required:

- EconomyShopGUI
- a separate Vault economy provider

First generated files:

```text
plugins/FallenEconomy/config.yml
plugins/FallenEconomy/money.yml
plugins/FallenEconomy/buy-shop.yml
plugins/FallenEconomy/essence-shop.yml
plugins/FallenEconomy/sell-values.yml
plugins/FallenEconomy/auctions.yml
plugins/FallenEconomy/orders.yml
```

If PlayerPoints is missing, the plugin still loads and all `$` features continue to work.
