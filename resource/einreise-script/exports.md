# Exports

### Exports

#### Server-side Exports

```lua
-- Give a player a legal or illegal entry status
-- @param src: player source/ID
-- @param einreise: 'legal' or 'illegal'
exports['ata_einreise']:GiveEinreise(src, 'legal')

-- Get a player's entry status
-- @param src: player source/ID
-- @returns: 'legal', 'illegal', or nil if not found
local status = exports['ata_einreise']:GetEinreise(src)
```

### Open Menu (Joining UI) \[check player sql and if nothing to choose opened menu automaticly]

```lua
TriggerClientEvent('ata_einreise:ShowJoin:client', src)
```

### Show Admin Menu

```lua
TriggerClientEvent('ata_einreise:ShowAdminMenu', src)
```

### Teleport Back (if admin use /einreise and want to get back last location)

```lua
TriggerClientEvent('ata_einreise:BackToCity', src)
```
