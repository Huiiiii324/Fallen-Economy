# Auction And Orders

Auctions and orders are built into Fallen Economy and use the internal `$` balance from `money.yml`.

## Auctions

```text
/ah
/ah sell <price>
/ah cancel <id>
/ah sort <mode>
```

## Orders

```text
/order
/order create <unitPrice> <amount>
/order fill <id> [amount]
/order cancel <id>
/order sort <mode>
```

Order creation withdraws the full `$` escrow. Cancelling refunds the unfilled amount.

When a player fills an order, the seller is paid immediately and the ordered
items are delivered to the order creator. If the creator is offline, pending
items are stored in `plugins/FallenEconomy/order-deliveries.yml` and delivered
automatically the next time they join.
