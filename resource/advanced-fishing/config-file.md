# Config File

## Config File

The main settings are in `config.lua`. The configuration below matches the release package. Restart `ata_SpeedBump` after changing Lua configuration or integration files.

Placements created in the admin panel are stored in the database. They are not written to `config.lua`.

### config.lua

```lua
Config = {}

-- Command that opens the speed bump menu (admins only).
Config.Command = 'speedbump'

-- Admins: the ace `ata_speedbump.admin`, or one of these framework groups (ESX / QBCore / Qbox).
-- add_ace group.admin ata_speedbump.admin allow
Config.AdminGroups = { admin = true, superadmin = true, god = true }

-- Notifications: 'ox', 'esx', 'qb', 'qbox' or 'none'.
Config.Notify = 'ox'

-- Pieces are spawned within this distance (meters) of each player.
Config.StreamDistance = 250.0

-- Longest bump an admin can place (meters).
Config.MaxLength = 30.0

-- How fast cars lose speed when they reach a bump with a speed limit (m/s per second).
Config.SpeedLimitSlowdown = 8.0

-- Default speed limit (km/h) and how far before the bump it starts (meters).
Config.Defaults = { kmh = 30, distance = 15 }

-- Emergency vehicles ignore speed limits and tire spikes (see client/editable.lua).
Config.EmergencyIgnore = true

-- Point picking keys: https://docs.fivem.net/docs/game-references/controls/
Config.Placing = {
    speed = 0.6,
    addPoint = 24,
    undoPoint = 25,
    done = 191,
    cancel = 194,
}
```

### Settings reference

| Setting                     | Default                      | Description                                                                                                                         |
| --------------------------- | ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `Config.Command`            | `'speedbump'`                | Chat command without the leading slash. The default opens with `/speedbump`.                                                        |
| `Config.AdminGroups`        | `admin`, `superadmin`, `god` | Groups checked by the framework admin integration. Keep only the groups you want to allow.                                          |
| `Config.Notify`             | `'ox'`                       | Notification provider: `'ox'`, `'esx'`, `'qb'`, `'qbox'` or `'none'`.                                                               |
| `Config.StreamDistance`     | `250.0`                      | Distance in meters used to load placements around the rendered camera. Objects unload beyond this distance plus a 50 m buffer.      |
| `Config.MaxLength`          | `30.0`                       | Maximum horizontal distance between the two placement points, in meters. The final model length snaps to complete pieces.           |
| `Config.SpeedLimitSlowdown` | `8.0`                        | How quickly the scripted speed cap decreases, in meters per second per second. A higher positive value slows vehicles more sharply. |
| `Config.Defaults.kmh`       | `30`                         | Initial speed limit for a new placement, in km/h.                                                                                   |
| `Config.Defaults.distance`  | `15`                         | Initial approach distance for a new placement, in meters.                                                                           |
| `Config.EmergencyIgnore`    | `true`                       | Exempts GTA emergency-class vehicles, class 18, from scripted speed limits and tire spikes. Physical bump collision remains.        |

Changing `Config.Defaults` does not overwrite speed settings on existing saved placements. Edit those placements in the admin panel.

The menu offers **10–80 km/h** in steps of 5, and approach distances of **10, 15, 25 or 40 meters**. These menu controls are separate from the initial values in `Config.Defaults`.

#### Notifications

```lua
Config.Notify = 'ox'
```

Choose the mode that matches your server. Framework notification modes use the matching framework when it is detected. If a selected framework mode is unavailable, the default bridge falls back to ox\_lib notifications. `'none'` disables notifications from the bridge.

`ox_lib` remains a required dependency even when using another notification mode.

#### Placement controls

| Setting                    | Default | Action                                                                |
| -------------------------- | ------- | --------------------------------------------------------------------- |
| `Config.Placing.speed`     | `0.6`   | Base free-camera movement speed. Hold Left Shift for faster movement. |
| `Config.Placing.addPoint`  | `24`    | Set a point; default Left Mouse Button.                               |
| `Config.Placing.undoPoint` | `25`    | Remove the last selected point; default Right Mouse Button.           |
| `Config.Placing.done`      | `191`   | Confirm both selected points; default Enter.                          |
| `Config.Placing.cancel`    | `194`   | Cancel point picking; default Backspace.                              |

These are FiveM control IDs. See the [official control reference](https://docs.fivem.net/docs/game-references/controls/) for alternative bindings. Camera movement uses W/A/S/D, E/Q and mouse look; those controls are not configured by `Config.Placing`.

### Editable integrations

Both versions expose `client/editable.lua` and `server/editable.lua` for server-specific integrations.

#### client/editable.lua

| Function                                 | Purpose                                                   |
| ---------------------------------------- | --------------------------------------------------------- |
| `Bridge.framework()`                     | Detects Qbox, ESX, QBCore or no framework.                |
| `Bridge.notify(text, kind)`              | Routes notifications to your selected provider.           |
| `Bridge.ignoreSpeedLimit(vehicle)`       | Return `true` to exempt a vehicle from scripted slowdown. |
| `Bridge.ignoreSpikes(vehicle)`           | Return `true` to exempt a vehicle from tire spikes.       |
| `Bridge.onTyreBurst(vehicle, tyreIndex)` | Hook called after a tire is burst by this resource.       |

Emergency exemptions are based on vehicle class, not the driver's job or siren state. Customize the two ignore functions if your server needs different rules.

#### server/editable.lua

| Function                           | Purpose                                                                              |
| ---------------------------------- | ------------------------------------------------------------------------------------ |
| `Bridge.framework()`               | Detects the running framework.                                                       |
| `Bridge.isAdmin(src)`              | Determines who may open the panel and save or delete placements.                     |
| `Bridge.onSaved(src, bump, isNew)` | Hook after a successful placement save; `isNew` distinguishes creation from editing. |
| `Bridge.onDeleted(src, bump)`      | Hook after a saved placement is deleted.                                             |

The save and delete hooks are empty by default. They can be used for your own logging or integrations.

### Model definitions

`shared/kinds.lua` contains model names, segment sizes, cap sizes and dimensions. These values match the streamed models. Keep them unchanged unless you are developing matching replacement models with source access.

### Server export

Other server resources can read the current list of placements:

```lua
local bumps = exports['ata_SpeedBump']:getBumps()
```

Call it after ATA SpeedBump has finished loading its database records. The export returns a list sorted by descending ID. It is a read interface; changing its returned data is not a supported way to save or synchronize placements.
