# Fallen Economy Plugin

Custom Paper 1.21.11 plugin for the Fallen Economy package.

## Features

- `/ah` auction house
- `/ah sell <price>`
- auction purchase confirmation GUI
- auction price limits and listing limits
- `/order` buy orders
- `/order create <unitPrice> <amount>`
- `/order fill <id> [amount]`
- Vault economy support when present
- internal Essence balances when Vault is missing

## Build

From the workspace root:

```text
powershell -ExecutionPolicy Bypass -File tools\build_fallen_economy_plugin.ps1
```

The built jar is copied to:

```text
Fallen Economy\server-root\plugins\FallenEconomy.jar
```
