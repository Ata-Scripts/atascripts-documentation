# Exports

Open Menu in client side:

```lua
TriggerEvent('ata_coinshop:openMenu')
```

#### Server Exports

**GetCoin**

```lua
exports['ata_coinshop']:GetCoin(identifier)
```

Returns the coin amount for a player

* **Parameters:**
  * `identifier`: Player's identifier (steam/license)
* **Returns:**
  * Number: Player's coin amount
* **Example:**

```lua
local coins = exports['ata_coinshop']:GetCoin('steam:123456789')
```

**AddCoin**

```lua
exports['ata_coinshop']:AddCoin(identifier, amount)
```

Adds coins to a player's balance

* **Parameters:**
  * `identifier`: Player's identifier
  * `amount`: Number of coins to add
* **Example:**

```lua
exports['ata_coinshop']:AddCoin('steam:123456789', 100)
```

**RemoveCoin**

```lua
exports['ata_coinshop']:RemoveCoin(identifier, amount)
```

Removes coins from a player's balance

* **Parameters:**
  * `identifier`: Player's identifier
  * `amount`: Number of coins to remove
* **Example:**

```lua
exports['ata_coinshop']:RemoveCoin('steam:123456789', 50)
```

**SetCoin**

```lua
exports['ata_coinshop']:SetCoin(identifier, amount)
```

Sets a player's coin balance

* **Parameters:**
  * `identifier`: Player's identifier
  * `amount`: New coin balance
* **Example:**

```lua
exports['ata_coinshop']:SetCoin('steam:123456789', 200)
```

#### Client Events

**Open Menu Event**

```lua
TriggerEvent('ata_coinshop:openMenu')
```

Opens the coin shop menu for the player

* **Example:**

```lua
RegisterCommand('shop', function()
    TriggerEvent('ata_coinshop:openMenu')
end)
```

#### Integration Examples

**Adding Coins on Player Join**

```lua
AddEventHandler('playerConnecting', function()
    local identifier = GetPlayerIdentifier(source)
    exports['ata_coinshop']:AddCoin(identifier, 100) -- Give 100 coins on join
end)
```

**Checking Coins Before Purchase**

```lua
local function CanPlayerAfford(identifier, price)
    local coins = exports['ata_coinshop']:GetCoin(identifier)
    return coins >= price
end
```

**Custom Shop Integration**

```lua
RegisterCommand('customshop', function()
    local identifier = GetPlayerIdentifier(source)
    local coins = exports['ata_coinshop']:GetCoin(identifier)
    
    if coins >= 50 then
        exports['ata_coinshop']:RemoveCoin(identifier, 50)
        -- Give item to player
    end
end)
```

#### Database Integration

The script uses the following database structure:

* ESX: `users` table with `coinVIP` column
* QB-Core: `players` table with `coinVIP` column

Next Step: Would you like me to add more examples or specific integration scenarios?
