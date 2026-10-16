# Config File

### Configuration

The config.lua file allows you to customize various aspects of the fishing system.

#### Basic Settings

```lua
Config.Locale = 'en' -- Default language (options: 'en', 'de', 'tr')

Config.Admins = { 
    'admin',
    'god',
    -- 'superadmin', -- Uncomment to add more admin groups
}

Config.FishRod = {
    item_name = "fishing_rod", -- Item name of the fishing rod
    price = 100, -- Price of the fishing rod
    Min_WaitTime = 10000, -- Min time to wait for a fish (10 seconds)
    Max_WaitTime = 30000, -- Max time to wait for a fish (30 seconds)
}
```

#### XP System

Configure how much XP players gain for catching different tiers of fish:

```lua
Config.Xp = {
    ['common'] = { 
        min = 10, -- Min XP for common fish
        max = 20, -- Max XP for common fish
    },
    ['rare'] = {
        min = 21, -- Min XP for rare fish
        max = 40, -- Max XP for rare fish
    },
    ['epic'] = {
        min = 41, -- Min XP for epic fish
        max = 60, -- Max XP for epic fish
    },
    ['legendary'] = {
        min = 61, -- Min XP for legendary fish
        max = 80, -- Max XP for legendary fish
    },
}
```

#### Chance System

Control fishing mechanics and probabilities:

```lua
Config.ChanceSystem = {
    -- Broken Fishing Rod
    broken_rod_chance = 3, -- Chance to break rod (default 3%)
    
    -- Minigame Score 
    minigame_min_score = 90, -- Min score to catch a fish (default 90)

    -- Hotspot settings
    hotspot_radius = 30.0, -- How close to a hotspot players must be (in meters)
    hotspot_chance = 30, -- Bonus chance (%) for catching fish in hotspots
    
    -- Chance to catch nothing
    nothing_chance = {
        min = 5,  -- Minimum chance to catch nothing at max level 
        max = 20, -- Maximum chance to catch nothing at level 1
    },
    
    -- Tier base weights: chance distribution at level 1
    tier_base = {
        common = 60,     -- % chance for common fish at level 1
        rare = 25,       -- % for rare fish at level 1
        epic = 10,       -- % for epic fish at level 1
        legendary = 5,   -- % for legendary fish at level 1
    },
    
    -- Tier max weights: chance distribution at max level
    tier_max = {
        common = 10,     -- % chance for common fish at max level
        rare = 25,       -- % for rare fish at max level
        epic = 30,       -- % for epic fish at max level
        legendary = 35,  -- % for legendary fish at max level
    },
}
```

#### Leveling System

Configure the maximum level and XP requirements for each level:

```lua
Config.levels = {
    MAX_LEVEL = 30, -- Maximum level players can reach
    xp_needed = {
        -- [level] = XP needed to reach this level (from previous level)
        [2] = 100, -- 100 XP needed to reach level 2 from level 1
        [3] = 200,
        -- ...and so on
    }
}
```

#### Fish Market NPC

Configure the NPC for the fish market:

```lua
Config.NPC = {
    {
        model = 'a_m_m_hillbilly_01', -- Model of the NPC
        coords = vector3(-1836.74, -1260.41, 7.62), -- Location
        heading = 323.59, -- Heading/direction
        text = '[E] Open Fish Market', -- Interaction text
        eventName = 'ata_fishing:openMarket', -- Event name (don't change)
        eventData = {}, -- Event data (don't change)
        eventType = 'client', -- Event type (don't change)
        animation = 'WORLD_HUMAN_STAND_FISHING', -- NPC animation
        target = true,  -- Use target system (like qb-target/ox-target) or text UI
    },
    -- You can add more NPCs by copying this structure
}
```

#### Fish Market Items

Configure the available fish in the market:

```lua
Config.FishMarket = {
    {
        name = "salmon", -- Item name
        label = "Salmon", -- Display name
        description = "Fish", -- Description
        img = "./imgs/items/salmon.png", -- Image path
        price = 520, -- Selling price
        tier = 'common', -- Tier (common, rare, epic, legendary)
        -- hotspot = vector3(-2033.64, -1042.25, 5.88), -- Optional hotspot location
    },
    -- Add more fish by copying this structure
}
```

