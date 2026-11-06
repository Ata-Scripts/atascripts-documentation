# Installation

## Installation

### 1. Add the resources

Extract your downloaded package and put the `[ata_AmbientSound]` folder inside your server's resources folder. It contains both resources:

```
resources/
└── [ata_AmbientSound]/
    ├── ata_AmbientSound/
    │   ├── fxmanifest.lua
    │   ├── audio/
    │   ├── client/
    │   ├── data/
    │   ├── html/
    │   ├── server/
    │   └── shared/
    └── ata_AmbientCreator/
        ├── fxmanifest.lua
        ├── client.lua
        ├── server.lua
        ├── worker/
        ├── node_modules/
        └── data/
```

Keep the resource names `ata_AmbientSound` and `ata_AmbientCreator`. The two resources find each other by name, and the creator writes its mixes into `ata_AmbientSound/html/sounds`. Do not leave them inside a second nested folder with the same name.

`ata_AmbientCreator` is optional. Without it everything works except **Create Custom Ambient**.

### 2. Dependencies

`ata_AmbientSound` has no dependencies. It does not need a framework, a database, ox\_lib or any SQL import. Zones are saved in `ata_AmbientSound/data/zones.json`.

`ata_AmbientCreator` needs the `yarn` resource, which comes with FXServer in `resources/[system]/[builders]/`. Most servers already start it through `ensure [system]` or `ensure yarn`. FFmpeg is included with the resource; you do not need to install it yourself.

### 3. Set up server.cfg

Add these lines to `server.cfg`:

```cfg
ensure ata_AmbientSound
add_ace group.admin ata_ambientsound.admin allow

# Optional: Create Custom Ambient
add_unsafe_child_process_permission ata_AmbientCreator
add_filesystem_permission ata_AmbientCreator write ata_AmbientSound
ensure ata_AmbientCreator
```

| Line                                                                  | Why it is needed                                                               |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| `ensure ata_AmbientSound`                                             | Starts the sound zones and the editor.                                         |
| `add_ace group.admin ata_ambientsound.admin allow`                    | Lets admins open `/soundadmin`.                                                |
| `add_unsafe_child_process_permission ata_AmbientCreator`              | Allows the creator to run FFmpeg to mix sounds.                                |
| `add_filesystem_permission ata_AmbientCreator write ata_AmbientSound` | Allows the creator to save finished mixes into `ata_AmbientSound/html/sounds`. |
| `ensure ata_AmbientCreator`                                           | Starts the creator. It must start after `ata_AmbientSound`.                    |

{% hint style="warning" %}
The two permission lines are only read when the server starts. After adding them, restart the whole server, not only the resource.
{% endhint %}

### 4. Give administrators access

Only admins can open the editor. A player is an admin when they have the `ata_ambientsound.admin` ACE (or `command.soundadmin`).

If your administrators already belong to `group.admin`, the line from step 3 is enough. If a player is not in that group yet, add their license:

```cfg
# Replace REPLACE_WITH_PLAYER_LICENSE with the player's real license value.
add_principal identifier.license:REPLACE_WITH_PLAYER_LICENSE group.admin
```

You can change the ACE name with `AdminAce` in `shared/config.lua`.

### 5. Start the server

Restart the server. Every player downloads the sounds once when they join (about 310 MB with the full library), after that they are cached.

{% hint style="danger" %}
**Do not restart or stop `ata_AmbientSound` while players are online.**

The resource contains GTA audio data (the wind and background mute). The game loads it when a player joins, and changing it while players are connected can crash their game. Restart the server, or make sure nobody is online, when you update it. Restarting `ata_AmbientCreator` is safe at any time.
{% endhint %}

### 6. Create your first zone

1. Join the server as an admin.
2. Type `/soundadmin` in chat.
3. Click **Create Zone**. The fly camera opens.
4. Click the corners of the area, then press **Enter**. Hold **SHIFT** instead to pick an interior / MLO or a prop.
5. Press **Browse**, pick a sound and click **Use this sound**.
6. Set the volume and how far it is heard from outside, then click **Save**.

Walk into the zone to hear it. For the full workflow and controls, see [Admin Panel](admin-panel.md).

From the server console you can open the editor for a player with `soundadmin <player ID>`.
