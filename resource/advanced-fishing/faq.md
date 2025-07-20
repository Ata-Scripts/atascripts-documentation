# FAQ

### Localization

ATA Fishing supports multiple languages. You can find the language files in the locales folder:

* English: locales/en.lua
* German: locales/de.lua
* Turkish: locales/tr.lua
* ....

To add a new language:

1. Copy one of the existing language files
2. Rename it (e.g., fr.lua for French)
3. Translate all strings in the file
4. Change the Config.Locale value in config.lua to your language code

### Hotspot System

Hotspots are special locations where players have increased chances to catch specific fish:

1.  To create a hotspot, add the hotspot vector3 coordinate to a fish in the Config.FishMarket table:\


    ```lua
       {
           name = "anchovy",
           -- other properties
           hotspot = vector3(-2033.64, -1042.25, 5.88),
       }
    ```
2. Players fishing within Config.ChanceSystem.hotspot\_radius of a hotspot will have increased chances to catch that specific fish.

### Technical Information

#### Database Structure

ATA Fishing creates a database table called ata\_fishing\_users with the following structure:

* identifier: Player identifier (VARCHAR(100))
* level: Player's fishing level (INT)
* xp: Player's fishing XP (INT)

#### Events

**Client Events**

* ata\_fishing:openMarket: Opens the fish market UI
* ata\_fishing:startFishing: Starts the fishing process

**Server Events**

* ata\_fishing:catchFish: Triggered when a player catches a fish
* ata\_fishing:brokenRod: Triggered when a player's fishing rod breaks

#### Callbacks

**Server Callbacks**

* ata\_fishing:getUserData: Gets player fishing data (level, XP, items)
* ata\_fishing:sellItem: Handles selling a fish
* ata\_fishing:buyFishRod: Handles buying a fishing rod

### Troubleshooting

#### Common Issues

1. Missing Items: Ensure all fish items are correctly added to your inventory system.
2. Discord Webhook Error: Check that you've entered valid Discord webhook URLs in server/discord.lua.
3. SQL Errors: Make sure your database connection is working properly. The script automatically creates necessary tables.
4. Dependencies: Ensure you have the latest version of ata\_core installed.

#### Getting Support

If you encounter any issues or have questions about the script:

* Check the script documentation and configuration files
* Contact us through our Discord server
