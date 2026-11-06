# Config File

## Config File

The settings are in `ata_AmbientSound/shared/config.lua`. The configuration below matches the release package. Restart the server after changing it (see the warning in Installation).

Zones and global sounds created in the editor are saved in `data/zones.json`. They are not written to `config.lua`.

### config.lua

```lua
AmbientConfig = {
    AdminAce = 'ata_ambientsound.admin', -- ace that may open /soundadmin
    UpdateMs = 50,
    MaxAudibleZones = 8,
    MaxZones = 200,
    MaxPoints = 64,
    PreloadDistance = 15,
    SpreadDistance = 8.0,   -- metres over which a sound turns from "around you" to "from the zone"
    AirCutoff = 2500,       -- Hz left at a zone's fade distance (air absorption)
    WallCutoff = 650,       -- Hz through a wall
    WallVolume = 0.45,      -- volume through a wall
    RegionBlend = 80.0,     -- metres global sounds blend at area borders
    RegionDuck = 1.0,       -- how much your zones fade out the global sound (1 = fully)
    Night = { from = 20, to = 6, blendHours = 1.0 },
    FadeSeconds = 1.2,
    LingerSeconds = 4.0,
    MuteGtaAmbience = true, -- silence GTA's own ambience so only your sounds play
    MuteScenes = {
        'FBI_HEIST_H5_MUTE_AMBIENCE_SCENE',
        'CHARACTER_CHANGE_IN_SKY_SCENE',
        'DLC_MPHEIST_TRANSITION_TO_APT_FADE_IN_RADIO_SCENE',
        'GTAO_Mute_Traffic_Ambience_Scene',
        'MP_POSITIONED_RADIO_MUTE_SCENE',
        'ATA_SILENCE_WIND_SCENE',
    },
    MuteZones = true,       -- also switch off GTA's ambient zones
    NoWind = true,          -- keep wind at 0 (trees and flags stop moving)
    MuteEmitters = {
        'LOS_SANTOS_VANILLA_UNICORN_01_STAGE', 'LOS_SANTOS_VANILLA_UNICORN_02_MAIN_ROOM', 'LOS_SANTOS_VANILLA_UNICORN_03_BACK_ROOM',
    },
    MaxVolume = 0.6,        -- 100% in the menu = this much of full volume
    ZoneHeight = 30,        -- metres above the highest corner
    Placing = {             -- control ids: https://docs.fivem.net/docs/game-references/controls/
        speed = 0.6,
        addPoint = 24,      -- left mouse
        undoPoint = 25,     -- right mouse
        done = 191,         -- ENTER
        cancel = 194,       -- BACKSPACE
        detect = 21,        -- hold SHIFT: pick an interior / MLO or a prop
        fast = 36,          -- hold LEFT CTRL: fly faster
        propPadding = 1.5,  -- metres around a picked prop
    },
    -- optional nicer names for files in html/sounds
    Sounds = {
        { name='Forest / light wind and birds', url='sounds/forest.mp3' },
        { name='Forest / pouring rain', url='sounds/forest_rain.mp3' },
        -- ...
    }
}
```

### Settings reference

| Setting           | Default                    | Description                                                                                                                                |
| ----------------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `AdminAce`        | `'ata_ambientsound.admin'` | ACE that may open `/soundadmin` and save zones.                                                                                            |
| `UpdateMs`        | `50`                       | How often (ms) sound positions are updated while a zone is audible.                                                                        |
| `MaxAudibleZones` | `8`                        | How many of the nearest zones can play at the same time.                                                                                   |
| `MaxZones`        | `200`                      | Maximum number of zones that can be saved.                                                                                                 |
| `MaxPoints`       | `64`                       | Maximum corners per zone.                                                                                                                  |
| `PreloadDistance` | `15`                       | Extra metres around a zone's fade distance where its sound is loaded in advance.                                                           |
| `SpreadDistance`  | `8.0`                      | Metres over which the sound turns from "all around you" (inside) to "coming from the zone" (outside).                                      |
| `AirCutoff`       | `2500`                     | Highest frequency (Hz) left at a zone's fade distance. Far sounds get darker, like in real air.                                            |
| `WallCutoff`      | `650`                      | Highest frequency (Hz) heard through a wall, for example an outdoor zone heard from inside a building.                                     |
| `WallVolume`      | `0.45`                     | Volume left through a wall (0 to 1).                                                                                                       |
| `RegionBlend`     | `80.0`                     | Metres over which the global sounds of two neighbouring areas crossfade at their border.                                                   |
| `RegionDuck`      | `1.0`                      | How much your zones fade out the global sound when you get close to them. `1` = fully, `0` = not at all.                                   |
| `Night`           | `20` to `6`                | Night hours (game clock) for zones and areas with a night sound. `blendHours` is the crossfade time around the start and end of the night. |
| `FadeSeconds`     | `1.2`                      | How long a sound takes to fade in or out.                                                                                                  |
| `LingerSeconds`   | `4.0`                      | How long a sound you walked away from keeps running silently, so it fades back in instead of restarting when you return.                   |
| `MuteGtaAmbience` | `true`                     | Mutes GTA's own ambience (birds, insects, city hum, distant traffic, world radios) so only your sounds play.                               |
| `MuteScenes`      | 6 scenes                   | GTA audio scenes kept running while `MuteGtaAmbience` is on. `ATA_SILENCE_WIND_SCENE` comes with this resource and mutes GTA's wind.       |
| `MuteZones`       | `true`                     | Also switches off GTA's ambient zones (city hum, sirens, room tones).                                                                      |
| `NoWind`          | `true`                     | Keeps the wind at 0. Side effect: trees, flags and water stop moving.                                                                      |
| `MuteEmitters`    | Vanilla Unicorn            | Fixed music sources in the world that are switched off.                                                                                    |
| `MaxVolume`       | `0.6`                      | 100% on a volume slider in the editor plays at this much of full volume, so ambience never gets too loud.                                  |
| `ZoneHeight`      | `30`                       | Height of drawn zones in metres above their highest corner. The bottom sits 3 m under the lowest corner.                                   |

#### Placing controls

| Setting               | Default | Action                                                                                   |
| --------------------- | ------- | ---------------------------------------------------------------------------------------- |
| `Placing.speed`       | `0.6`   | Fly camera speed.                                                                        |
| `Placing.addPoint`    | `24`    | Add a corner, or pick the highlighted interior / prop. Default Left Mouse Button.        |
| `Placing.undoPoint`   | `25`    | Remove the last corner. Default Right Mouse Button.                                      |
| `Placing.done`        | `191`   | Finish. Default Enter.                                                                   |
| `Placing.cancel`      | `194`   | Cancel. Default Backspace.                                                               |
| `Placing.detect`      | `21`    | Hold to pick an interior / MLO or a prop instead of drawing corners. Default Left Shift. |
| `Placing.fast`        | `36`    | Hold to fly faster. Default Left Ctrl.                                                   |
| `Placing.propPadding` | `1.5`   | Metres added around a picked prop's size.                                                |

These are FiveM control IDs. See the [official control reference](https://docs.fivem.net/docs/game-references/controls/) for other keys.

#### Sound names

Every audio file in `html/sounds` appears in the sound library automatically, named after its file name. The `Sounds` list only gives some files a nicer name:

```lua
{ name='Harbor / foghorn and gulls', url='sounds/harbor_foghorn.ogg' },
```

### Global sound areas

`shared/regions.lua` defines the 16 areas of the **Global Sounds** map (Countryside, West Coast, Los Santos City, Beaches, Airport, Port, Sandy Shores and more). Each area has an `id`, a `name`, a map `color` and a list of world `x`/`y` corners:

```lua
AmbientRegions = {
    { id='countryside', name='Countryside', color='#a3e635', points={
        {x=-2750,y=1450},{x=-500,y=1650},{x=1500,y=1450},{x=2050,y=550}, ... } },
    ...
}
```

Areas lower in the list sit on top of the ones above them. Keep the `id` of an area unchanged after you gave it a sound, because the saved sound is linked to that id.

### Adding your own sounds

1. Put `.mp3`, `.ogg` or `.wav` files in `ata_AmbientSound/html/sounds`.
2. Use only letters, digits, `_`, `-` and `.` in the file name. FiveM cannot serve files with spaces.
3. Restart the server.

The file appears in the sound library and in Create Custom Ambient, with its length and a category picked from its name. A name like `rain-tin-roof.ogg` goes into **Rain & storm** as "Tin roof". If a file name is not allowed, the server console tells you which file to rename.

Ambient sounds work best as loops of 1 to 5 minutes, mono, around 96 kbps. Every player downloads the sound files once, so keep the library reasonable in size.
