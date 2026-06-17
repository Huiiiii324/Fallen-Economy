# Auction And Orders

`FallenEconomy.jar` provides a basic auction house and buy-order system without a third-party auction plugin.

## Auction House

Commands:

```text
/ah
/ah sell <price>
/ah sort <newest|oldest|price_asc|price_desc|amount>
/ah cancel <id>
```

Behavior:

- `/ah sell <price>` lists the entire held item stack.
- Price must be between `auction.min-price` and `auction.max-price` in `plugins/FallenEconomy/config.yml`.
- Players have a configurable listing limit.
- Clicking an auction opens a confirmation GUI before purchase.
- Seller is paid after the buyer confirms and payment succeeds.

## Buy Orders

Commands:

```text
/order
/order create <unitPrice> <amount>
/order fill <id> [amount]
/order sort <newest|oldest|price_asc|price_desc|amount>
/order cancel <id>
```

Behavior:

- Create an order while holding the item type you want to buy.
- The buyer pays the full order value into escrow immediately.
- Sellers fill orders by holding the matching item and using `/order fill`, or by clicking the order GUI.
- Cancelled orders refund the remaining escrow.

## Economy

- If Vault economy is available, Fallen Economy uses it.
- If Vault is missing, Fallen Economy uses internal balances from `plugins/FallenEconomy/balances.yml`.
- Admins can use `/feconomy give <player> <amount>` with `falleneconomy.admin` when internal economy is active.

## Permissions

```text
falleneconomy.ah
falleneconomy.ah.sell
falleneconomy.order
falleneconomy.order.create
falleneconomy.admin
```
