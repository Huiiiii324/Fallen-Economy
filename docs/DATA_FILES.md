# Data Files

Fallen Economy stores persistent data in YAML files inside:

```text
plugins/FallenEconomy/
```

## buy-shop.yml

Stores configured `/buy` shop items.

Contains:

- next buy-shop id
- serialized item stack
- price in the active currency
- creation timestamp

Do not edit this while the server is running.

## config.yml

Main settings file.

Created from the bundled default config on first startup.

## auctions.yml

Stores active auction listings.

Contains:

- next auction id
- seller UUID
- seller name
- serialized item stack
- price
- creation timestamp

Do not edit this while the server is running.

## orders.yml

Stores active buy orders.

Contains:

- next order id
- creator UUID
- creator name
- material
- unit price
- original amount
- remaining amount
- creation timestamp

Do not edit this while the server is running.

## balances.yml

Stores internal economy balances.

Only used when Vault economy is unavailable and internal fallback is enabled.

## Backups

Before manual edits, stop the server and copy:

```text
plugins/FallenEconomy/auctions.yml
plugins/FallenEconomy/orders.yml
plugins/FallenEconomy/balances.yml
plugins/FallenEconomy/buy-shop.yml
```
