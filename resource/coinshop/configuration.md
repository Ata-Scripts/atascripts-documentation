# Configuration

#### Basic Settingslua

```lua
Config.DefualtGarage = 'pillboxgarage' -- Default garage for purchased vehicles
```

#### Commands

```lua
Config.CMD = {
    ['open_menu'] = 'coin',      -- Open shop menu
    ['set_coin'] = 'setcoin',    -- Set player coins
    ['add_coin'] = 'addcoin',    -- Add coins to player
    ['remove_coin'] = 'removecoin', -- Remove coins from player
    ['see_coins'] = 'lookupcoin',   -- Check player coins
}
```

#### Permissions

```lua
Config.Permission = {
    ['ALL'] = { -- All permissions
        'license:f8bc6aa65d475e72c5d619f893d22f384081ab79'
    },
    ['SET_COIN'] = { -- Set coin permission
        'steam:f8bc6aa65d472f384081ab79'
    },
    -- ... more permissions
}
```

#### Menu Items Structurelua

```lua
{
    count = "1",           -- Item quantity
    img = "img/item.png",  -- Item image
    label = "ITEM NAME",   -- Display name
    price = "100",         -- Coin price
    name = "item_name",    -- Inventory name
    category = "ITEMS",    -- Category: CARS, ITEMS, WEAPONS
    information = "Description" -- Item description
}
```

Coin Packageslua

```lua
Config.coinPackages = {
    {
        count_coin = "200",    -- Coin amount
        img = "img/Package.png", -- Package image
        price_coin = "$2.99",   -- Price
        link = "https://ata.tebex.io" -- Purchase link
    },
    -- ... more packages
}
```

#### Discord Webhooks

The script includes webhooks for:

* Item purchases
* Vehicle purchases
* Weapon purchases
* Admin commands
* System notifications
