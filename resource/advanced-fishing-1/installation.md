# Installation

### Installation

#### Step 1: Install the Resource

1. Download the ata\_fishing resource
2. Place it in your server's resources directory
3. Add ensure ata\_fishing to your server.cfg

#### Step 2: Database Setup

The script will automatically create the necessary database tables when it starts.

#### Step 3: Add Items

**For QBCore:**

Open qb-core/shared/items.lua and add the following items:

```lua
salmon                     = { name = 'salmon', label = 'Salmon', weight = 500, type = 'item', image = 'salmon.png', unique = false, useable = true, shouldClose = true, description = 'A fresh and tasty salmon caught from the river.' },
tuna                       = { name = 'tuna', label = 'Tuna', weight = 700, type = 'item', image = 'tuna.png', unique = false, useable = true, shouldClose = true, description = 'A big and meaty tuna, perfect for sushi.' },
trout                      = { name = 'trout', label = 'Trout', weight = 400, type = 'item', image = 'trout.png', unique = false, useable = true, shouldClose = true, description = 'A colorful trout, a fisherman's favorite.' },
bass                       = { name = 'bass', label = 'Bass', weight = 600, type = 'item', image = 'bass.png', unique = false, useable = true, shouldClose = true, description = 'A chunky bass, good for grilling.' },
mackerel                   = { name = 'mackerel', label = 'Mackerel', weight = 350, type = 'item', image = 'mackerel.png', unique = false, useable = true, shouldClose = true, description = 'Oily but delicious, full of flavor.' },
catfish                    = { name = 'catfish', label = 'Catfish', weight = 800, type = 'item', image = 'catfish.png', unique = false, useable = true, shouldClose = true, description = 'A slippery bottom-dweller, great fried.' },
cod                        = { name = 'cod', label = 'Cod', weight = 550, type = 'item', image = 'cod.png', unique = false, useable = true, shouldClose = true, description = 'Classic white fish, mild and flaky.' },
snapper                    = { name = 'snapper', label = 'Snapper', weight = 450, type = 'item', image = 'snapper.png', unique = false, useable = true, shouldClose = true, description = 'A bright red snapper, fresh from the sea.' },
anchovy                    = { name = 'anchovy', label = 'Anchovy', weight = 50, type = 'item', image = 'anchovy.png', unique = false, useable = true, shouldClose = true, description = 'Tiny but salty, good on pizza.' },
sardine                    = { name = 'sardine', label = 'Sardine', weight = 60, type = 'item', image = 'sardine.png', unique = false, useable = true, shouldClose = true, description = 'Packed with flavor in a small package.' },
halibut                    = { name = 'halibut', label = 'Halibut', weight = 700, type = 'item', image = 'halibut.png', unique = false, useable = true, shouldClose = true, description = 'A flat and tasty white fish.' },
grouper                    = { name = 'grouper', label = 'Grouper', weight = 750, type = 'item', image = 'grouper.png', unique = false, useable = true, shouldClose = true, description = 'Big, slow, and delicious.' },
flounder                   = { name = 'flounder', label = 'Flounder', weight = 400, type = 'item', image = 'flounder.png', unique = false, useable = true, shouldClose = true, description = 'Flat and delicate, great pan-fried.' },
perch                      = { name = 'perch', label = 'Perch', weight = 300, type = 'item', image = 'perch.png', unique = false, useable = true, shouldClose = true, description = 'Small but flavorful, caught in lakes.' },
herring                    = { name = 'herring', label = 'Herring', weight = 250, type = 'item', image = 'herring.png', unique = false, useable = true, shouldClose = true, description = 'Often smoked or pickled, a classic.' },
tilapia                    = { name = 'tilapia', label = 'Tilapia', weight = 400, type = 'item', image = 'tilapia.png', unique = false, useable = true, shouldClose = true, description = 'Mild and easy to cook, a popular choice.' },
eel                        = { name = 'eel', label = 'Eel', weight = 350, type = 'item', image = 'eel.png', unique = false, useable = true, shouldClose = true, description = 'Slimy but delicious when grilled.' },
swordfish                  = { name = 'swordfish', label = 'Swordfish', weight = 900, type = 'item', image = 'swordfish.png', unique = false, useable = true, shouldClose = true, description = 'A strong and meaty steak of the sea.' },
marlin                     = { name = 'marlin', label = 'Marlin', weight = 1000, type = 'item', image = 'marlin.png', unique = false, useable = true, shouldClose = true, description = 'A trophy fish, lean and firm.' },
pike                       = { name = 'pike', label = 'Pike', weight = 650, type = 'item', image = 'pike.png', unique = false, useable = true, shouldClose = true, description = 'Long and sharp-toothed, tricky to catch.' },
fishing_rod                = { name = 'fishing_rod', label = 'Fishing Rod', weight = 2000, type = 'item', image = 'fishing_rod.png', unique = false, useable = true, shouldClose = true, description = 'A fishing rod to catch fish.' },
```

**For ESX:**

Run the following SQL query in your database:

```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES
    ('salmon', 'Salmon', 1, 0, 1),
    ('tuna', 'Tuna', 1, 0, 1),
    ('trout', 'Trout', 1, 0, 1),
    ('bass', 'Bass', 1, 0, 1),
    ('mackerel', 'Mackerel', 1, 0, 1),
    ('catfish', 'Catfish', 1, 0, 1),
    ('cod', 'Cod', 1, 0, 1),
    ('snapper', 'Snapper', 1, 0, 1),
    ('anchovy', 'Anchovy', 1, 0, 1),
    ('sardine', 'Sardine', 1, 0, 1),
    ('halibut', 'Halibut', 1, 0, 1),
    ('grouper', 'Grouper', 1, 0, 1),
    ('flounder', 'Flounder', 1, 0, 1),
    ('perch', 'Perch', 1, 0, 1),
    ('herring', 'Herring', 1, 0, 1),
    ('tilapia', 'Tilapia', 1, 0, 1),
    ('eel', 'Eel', 1, 0, 1),
    ('swordfish', 'Swordfish', 1, 0, 1),
    ('marlin', 'Marlin', 1, 0, 1),
    ('pike', 'Pike', 1, 0, 1),
    ('fishing_rod', 'Fishing Rod', 1, 0, 1);
```

#### Step 4: Add Item Images

Copy all the images from the INSTALL/icons folder to your inventory resource's images folder:

* For QBCore: Copy to qb-inventory/html/images/
* For ESX: Copy to es\_extended/html/img/items/

#### Step 5: Setup Discord Webhooks (Optional)

Open server/discord.lua and add your Discord webhook URLs:

```lua
WebHooks = {
    ['ping_everyone'] = false, -- ping everyone when webhook message is sent (true/false)
    ['admin_actions'] = 'YOUR_WEBHOOK_URL_HERE',
    ['player_level_up'] = 'YOUR_WEBHOOK_URL_HERE',
    ['fishing_actions_catch'] = 'YOUR_WEBHOOK_URL_HERE',
}
```
