# Data Files

All runtime data lives in:

```text
plugins/FallenEconomy/
```

| File | Purpose |
| --- | --- |
| `config.yml` | Main plugin settings. |
| `money.yml` | Internal `$` balances. |
| `buy-shop.yml` | Native `/shop` `$` entries for End, Nether, Gear, and Food. |
| `essence-shop.yml` | PlayerPoints Essence entries shown through `/essenceshop`. |
| `sell-values.yml` | Per-item sell values paid in `$`. |
| `auctions.yml` | Active `$` auction listings. |
| `orders.yml` | Active `$` buy orders and escrow state. |
| `tool-timers.yml` | Online-time counters used by owner-bound timed tools. |

`balances.yml` from older versions is intentionally left untouched and is not converted into `money.yml`.
