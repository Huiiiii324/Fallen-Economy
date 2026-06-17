# Pricing

Sell prices are generated from the workspace config:

```text
tools/pricing.coefficients.json
```

Formula:

```text
sell = baseValue * currencyPerPoint * materialMultiplier * matchingRuleMultipliers
```

## Fields

- `currencyPerPoint`: global coefficient. Increase this to make every item sell for more Essence.
- `roundTo`: rounds generated prices to a step, for example `5` makes prices 5, 10, 15.
- `minimum`: lowest generated price.
- `baseValueOverrides`: changes the base point value before multipliers.
- `materialMultipliers`: multiplier for one exact item.
- `ruleMultipliers`: multiplier by `prefix`, `suffix`, `contains`, or exact `material`.
- `sellOverrides`: exact final sell price, skipping coefficient math.

## Examples

Double the whole economy:

```json
"currencyPerPoint": 2
```

Make ores worth 50% more:

```json
{
  "suffix": "_ORE",
  "multiplier": 1.5
}
```

Force totems to sell for exactly 500 Essence:

```json
"sellOverrides": {
  "TOTEM_OF_UNDYING": 500
}
```

After changes, regenerate:

```text
node tools/generate_fallen_shop_template.mjs
```
