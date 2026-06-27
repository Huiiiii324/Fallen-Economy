# Commands

| Command | Description |
| --- | --- |
| `/shop` | Open normal `$` shop categories. |
| `/shop <end|nether|gear|food>` | Open a normal shop category. |
| `/shop sort <mode>` | Set normal shop sort mode. |
| `/shop edit` | Open the normal `$` shop editor. |
| `/shop edit add <price> <category>` | Add held item to the normal `$` shop config. |
| `/shop edit remove <id>` | Remove a normal shop item. |
| `/shop edit price <id> <price>` | Change a normal shop item price. |
| `/essence` | Show PlayerPoints Essence balance. |
| `/essenceshop` | Open Essence shop. |
| `/essenceshop config add <price> <category>` | Add held item to Essence shop config. |
| `/sell` | Open sell GUI. |
| `/sell hand` | Sell held stack for `$`. |
| `/sell all` | Sell sellable storage inventory items for `$`. |
| `/balance`, `/bal`, `/money` | Show `$` balance. |
| `/pay <player> <amount>` | Transfer `$`. |
| `/ah`, `/auction`, `/auctions` | Open auction house using `$`. |
| `/ah sell <price>` | List held stack for `$`. |
| `/order`, `/orders` | Open buy orders using `$`. |
| `/order create <unitPrice> <amount>` | Create a funded `$` buy order. |
| `/feconomy balance/give/take/set` | Manage `$`. |
| `/feconomy essence balance/give/take/set` | Manage PlayerPoints Essence. |
| `/feconomy tools give <player> <pickaxe|shovel|axe>` | Give one normal Fallen utility tool. |
| `/feconomy tools give timed <player> <pickaxe|shovel|axe> <hours>` | Give one owner-bound timed tool. The timer drains only while the owner is online. |
| `/feconomy tools give <player> sellwand <uses>` | Give one Sell Wand with limited successful uses. |
| `/killeffects`, `/killeffect` | Open the kill effects GUI. |
| `/killeffects clear` | Disable selected kill effect. |
| `/killeffects reload` | Reload kill effects config. |

Shop and Essence shop item clicks open a confirmation GUI before charging the player.

Timed utility tools can transfer ownership only if the current owner drops them or loses them on death. Moving a tool through a chest does not rebind it.
