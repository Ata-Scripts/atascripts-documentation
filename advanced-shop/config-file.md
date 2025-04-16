# Config File

```lua
Config = {}

-- General settings
Config.Debug = false
Config.AdminCommands = true -- Allow admin commands for shop management
Config.InteractionWithTarget = true -- defualt : false / if you want to use qb-target or ox_target set to true


-- Inventory settings
Config.Inventory = {
    imagePath = "nui://qb-inventory/html/images/", -- Path to inventory item images
    defaultImage = "./imgs/empty.png" -- Default image for items without an image
}

-- Shop default settings (used when creating new shops)
Config.DefaultShopSettings = {
    blipId = 52, -- Blip icon on the map
    blipColor = 2,
    blipScale = 0.8,
    blipName = "Supermarket",
    npcModel = "s_m_m_linecook", -- Default NPC model for shop interactions
    interactionRange = 2.0,
    defaultTheme = "light", -- "light" or "dark" theme
    defaultLogo = "imgs/logo.png", -- Default logo (relative to html folder)
    OpenMenuText = "Open Shop",
    initialCash = 10000, -- Starting cash for new shops
    isOpen = true, -- Whether the shop is open by default
}

Config.UI = {
    ['cash_out_help'] = 'Lorem ipsum dolor sit amet consectetur. Nam id fringilla posuere sodales et. Sed pellentesque commodo sit volutpat imperdietporttitor..'
}



-- Default categories for new shops
Config.DefaultCategories = {"foods","drinks" , "tools" , "others"}

-- Item templates that can be added to markets
Config.ItemTemplates = {
        {
        name = "water_bottle",
        BuyPrice = 5,
        description = 'Refreshing bottled water',
        category = 'drinks'
        },
        {
        name = "sandwich",
        BuyPrice = 10,
        description = 'A tasty sandwich',
        category = 'foods'
        },
        {
        name = "beer",
        BuyPrice = 12,
        description = 'Cold beer',
        category = 'drinks'
        },
        {
        name = "tosti",
        BuyPrice = 8,
        description = 'Grilled cheese sandwich',
        category = 'foods'
        },
        {
        name = "coffee",
        BuyPrice = 6,
        description = 'Hot coffee to keep you awake',
        category = 'drinks'
        },
        {
        name = "cola",
        BuyPrice = 7,
        description = 'Refreshing cola drink',
        category = 'drinks'
        },
        {
        name = "phone",
        BuyPrice = 250,
        description = 'Smartphone device',
        category = 'others'
        },
        {
        name = "bandage",
        BuyPrice = 15,
        description = 'Medical bandage for small wounds',
        category = 'others' 
        },
        {
        name = "lockpick",
        BuyPrice = 50,
        description = 'Tool for picking locks',
        category = 'tools'
        },

}

-- Permissions
Config.Permissions = {
    adminGroups = {"admin", "superadmin", "god"}, -- Groups that can use admin commands
    managementCommands = {
        addMarket = true, -- Allow adding markets with commands
        removeMarket = true, -- Allow removing markets with commands
    }
} 
```
