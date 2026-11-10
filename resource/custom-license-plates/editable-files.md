# Editable Files

these files are open, change them however you like

| file                                     | what                                                        |
| ---------------------------------------- | ----------------------------------------------------------- |
| `config.lua`                             | country, plate formats, shop starting values, bridge choice |
| `bridge/editable_server.lua`             | your own rules: jobs, who can buy or fit plates, logs       |
| `bridge/editable_client.lua`             | when the shop can open, HUD, notifications                  |
| `bridge/server.lua`, `bridge/client.lua` | framework, inventory and key script support                 |

## editable\_server.lua

every shop action passes `Hooks.allow` first, return `false, 'message'` to stop it

```lua
function Hooks.allow(src, action, args)
    -- only mechanics can put plates on and take them off
    if action == 'install' or action == 'uninstall' or action == 'use:license_plate' or action == 'use:screwdriver' then
        if Bridge.job(src) ~= 'mechanic' then return false, 'Only a mechanic can do this' end
    end
    return true
end
```

who can fit a plate or holder on a car

```lua
function Hooks.canUseVehicle(src, vehicle, realPlate, isOwner)
    -- police can fit plates on any vehicle
    if Bridge.job(src) == 'police' then return true end
    return isOwner
end
```

events for your own logs

```lua
AddEventHandler('ata_VehiclePlate:onPlatePurchased', function(d)
    print(('%s bought plate %s for $%d'):format(d.owner, d.text, d.price or 0))
end)
-- also: onPlateInstalled, onPlateRemoved, onPlateTransferred, onPlateChanged, onPlateDesignUpdated
```

## editable\_client.lua

```lua
-- can the shop open right now
function Hooks.canOpenShop(page)
    if IsPedInAnyVehicle(PlayerPedId(), false) then return false, 'Step out of your vehicle first' end
    return true
end

-- hide or show your HUD
function Hooks.onShopOpen(page) end
function Hooks.onShopClose() end

-- your own notify
function Hooks.notify(text, kind)
    Bridge.notify(text, kind)
end
```

## your garage is custom?

no problem, tell the script where you keep the cars

```lua
Config.VehicleTable = { name = 'my_garage', owner = 'owner', plate = 'plate' }
```

other tables that store a plate (trunk, glovebox, keys) get renamed with it, add yours here

```lua
Config.PlateLinks = {
    { table = 'trunkitems', column = 'plate' },
    { table = 'inventories', column = 'identifier', prefixes = { 'trunk-', 'glovebox-' } },
    { table = 'my_table', column = 'plate' },
}
```

your garage keeps the plate somewhere else? listen to this and update it yourself

```lua
AddEventHandler('ata_VehiclePlate:onRealPlateChanged', function(d)
    -- d.old, d.new, d.netId, d.actor
end)
```

## your inventory or key script isnt on the list?

open `bridge/server.lua`, copy one of the branches and change the export names, every key script is about 3 lines

```lua
['my-keys'] = {
    has = function(src, plate) return exports['my-keys']:HasKey(src, plate) end,
    give = function(src, plate) exports['my-keys']:GiveKey(src, plate) end,
    remove = function(src, plate) exports['my-keys']:RemoveKey(src, plate) end,
},
```
