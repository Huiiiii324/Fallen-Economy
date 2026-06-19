# Buy Orders

`/order` is built into Fallen Economy and uses `$`.

Commands:

```text
/order
/order create <unitPrice> <amount>
/order fill <id> [amount]
/order cancel <id>
/order sort <newest|oldest|price_asc|price_desc|amount>
```

Creating an order withdraws the full `$` escrow immediately. Cancelling refunds remaining escrow.

Data file:

```text
plugins/FallenEconomy/orders.yml
```
