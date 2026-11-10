# Installation

### step 1: add the resource

1. put `ata_VehiclePlate` in your resources folder
2. add `ensure ata_VehiclePlate` to your server.cfg, after oxmysql, your framework and your inventory
3. start the server

the database tables are made on the first start, nothing to import

### step 2: add the items

the item pictures are in the `items` folder, copy them into your inventory images folder

**ox\_inventory** (`ox_inventory/data/items.lua`)

```lua
['license_plate'] = { label = 'License Plate', weight = 500, stack = false, close = true, server = { export = 'ata_VehiclePlate.useLicensePlate' } },
['screwdriver']   = { label = 'Screwdriver', weight = 200, stack = true, close = true, server = { export = 'ata_VehiclePlate.useScrewdriver' } },
['plate_flipper'] = { label = 'Plate Flipper', weight = 300, stack = true, close = true, server = { export = 'ata_VehiclePlate.usePlateFlipper' } },
['plate_holder']  = { label = 'Plate Holder', weight = 300, stack = false, close = true, server = { export = 'ata_VehiclePlate.usePlateHolder' } },
```

**QBCore / Qbox** (`qb-core/shared/items.lua`)

```lua
license_plate = { name = 'license_plate', label = 'License Plate', weight = 500, type = 'item', image = 'license_plate.png', unique = true, useable = true, shouldClose = true, description = 'A license plate' },
screwdriver   = { name = 'screwdriver', label = 'Screwdriver', weight = 200, type = 'item', image = 'screwdriver.png', unique = false, useable = true, shouldClose = true, description = 'Takes plates and holders off' },
plate_flipper = { name = 'plate_flipper', label = 'Plate Flipper', weight = 300, type = 'item', image = 'plate_flipper.png', unique = false, useable = true, shouldClose = true, description = 'Flips the plate' },
plate_holder  = { name = 'plate_holder', label = 'Plate Holder', weight = 300, type = 'item', image = 'plate_holder.png', unique = true, useable = true, shouldClose = true, description = 'A plate holder' },
```

**qs-inventory / codem-inventory**

add the same four items, `license_plate` and `plate_holder` have to be unique

**ESX inventory**

ESX items have no metadata, so plates and holders are put on from the shop, you only need these two

```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES
    ('screwdriver', 'Screwdriver', 1, 0, 1),
    ('plate_flipper', 'Plate Flipper', 1, 0, 1);
```

### step 3: pick your country

in `config.lua`

```lua
Config.Country = 'DE'
```

or in game with `/plateadmin` → Settings → Default plates, see [Country Plates](country-plates.md)

### step 4: shop location

```lua
locations = {
    -- preview: the counter where the picked plate is shown (x, y, z, heading)
    { coords = vector3(318.51, -1076.88, 29.48), blip = true, preview = vector4(319.35, -1077.85, 29.765, 0.0) },
},
```

add as many as you want, `/plateshop` also opens it anywhere (set `Config.Shop.command = ''` to turn that off)

### step 5: discord logs (optional)

open `bridge/editable_server.lua` and paste a webhook per section

```lua
Webhooks = {
    purchases = '',     -- plates bought or given
    plates = '',        -- put on and taken off vehicles
    owners = '',        -- new owner, plate removed
    designs = '',       -- designs shared with a code
    admin = '',         -- catalog, settings and plate positions changed in /plateadmin
}
```

webhooks stay on the server, players never see them
