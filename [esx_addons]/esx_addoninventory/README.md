# esx_addoninventory

## Download

### Using Git
- Clone repository from github
- Move esx_addoninventory to you resource folder

```
cd Downloads
git clone https://github.com/esx-framework/esx-legacy.git
```

### Using Release
- Download https://github.com/esx-framework/esx-legacy/archive/refs/tags/1.7.5.zip
- Move esx_addoninventory to you resource folde

## Installation
- Import `esx_addoninventory.sql` in your database
- Add this in your `server.cfg`:

```
ensure esx_addoninventory
```

## Usage
There are two types of inventories: shared and not shared.

- Shared inventories dont belong to a specific user. Example: foodstore items.
- None-shared inventories are created for every user in the server. They are created in db when player is loaded, Example: property items

### `addon_inventory` database information
An addon inventory must be configured in the database before using it. Don't forget to run a server restart afterwards (you can alternative restart the script and relog all clients)

| `name`   | `label` | `shared` |
| -------- | ------- | -------- |
| name of the inventory | label of the inventory (not used) | is the inventory shared with others? (boolean either `0` or `1`) |

```lua
TriggerEvent('esx_addoninventory:getSharedInventory', 'society_police', function(inventory)
	inventory.addItem('bread', 1)
end)

TriggerEvent('esx_addoninventory:getInventory', 'property', 'steam:0123456789', function(inventory)
	inventory.removeItem('water', 1)
end)

```
# Legal
### License
esx_addoninventory - inventories!

Copyright (C) 2015-2022 Jérémie N'gadi

This program Is free software: you can redistribute it And/Or modify it under the terms Of the GNU General Public License As published by the Free Software Foundation, either version 3 Of the License, Or (at your option) any later version.

This program Is distributed In the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty Of MERCHANTABILITY Or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License For more details.

You should have received a copy Of the GNU General Public License along with this program. If Not, see http://www.gnu.org/licenses/.