# Exports

### Exports

ATA Fishing provides exports to interact with the fishing system from other resources:

#### Server Exports

```lua
-- Get player's fishing level
local level = exports['ata_fishing']:GetPlayerLevel(playerId)

-- Get player's fishing XP
local xp = exports['ata_fishing']:GetPlayerXP(playerId)

-- Add XP to a player
exports['ata_fishing']:AddPlayerXP(playerId, amount)

-- Set a player's level
exports['ata_fishing']:SetPlayerLevel(playerId, level)
```

