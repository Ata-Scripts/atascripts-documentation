# Config

```lua
Config = {}

-- AutoReplaceManifest: Automatically updates the fxmanifest.lua for all resources.
Config.AutoReplaceManifest = true

-- SelectedTheme: Specifies the theme for the loading screen from the themes directory.
Config.SelectedTheme = 'ata'  -- Path: client/themes/[THEME_NAME].lua
```

#### Details

* **AutoReplaceManifest**: When set to `true`, this option enables the script to automatically modify the `fxmanifest.lua` files across all server resources, simplifying installation and updates.
* **SelectedTheme**: This setting allows you to choose a predefined theme for the loading screen by specifying the theme name. The theme file should be located in `client/themes/[THEME_NAME].lua`. Replace `'ata'` with your desired theme name to customize the appearance according to your preference.
