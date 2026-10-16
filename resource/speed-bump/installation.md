# Installation

## Installation

### 1. Add the resource

Extract your downloaded package and put the `ata_SpeedBump` folder inside your server's resources folder. For example:

```
resources/
└── [ata]/
    └── ata_SpeedBump/
        ├── fxmanifest.lua
        ├── config.lua
        ├── client/
        ├── server/
        ├── shared/
        ├── html/
        └── stream/
```

Keep the resource name `ata_SpeedBump` so the start commands and integrations in this guide match your installation. Do not leave it inside a second nested `ata_SpeedBump` folder.

### 2. Install the dependencies

Install `ox_lib` and `oxmysql`. Make sure your database connection is working before starting ATA SpeedBump.

The script does not need inventory items or edits to your framework files.

### 3. Set the start order

In `server.cfg`, start the database library, ox\_lib and your framework before ATA SpeedBump:

```cfg
ensure oxmysql
ensure ox_lib

# Add ONE line matching your framework:
# ensure es_extended
# ensure qb-core
# ensure qbx_core

ensure ata_SpeedBump
```

Uncomment the framework line that matches your server, or keep your existing framework start block above `ensure ata_SpeedBump`. For standalone use, no framework line is needed.

The framework is detected automatically. There is no framework selector in `config.lua`.

### 4. Give administrators access

You can grant access through ACE permissions or your framework's admin groups.

#### ACE permissions

Add this to `server.cfg` if your administrators already belong to `group.admin`:

```cfg
add_ace group.admin ata_speedbump.admin allow
```

If a player is not already in that group, assign their actual license identifier:

```cfg
# Replace REPLACE_WITH_PLAYER_LICENSE with the player's real license value.
add_principal identifier.license:REPLACE_WITH_PLAYER_LICENSE group.admin
```

For standalone servers, use ACE permissions to grant admin access.

#### Framework permissions

The default groups are:

```lua
Config.AdminGroups = { admin = true, superadmin = true, god = true }
```

| Framework  | How access is checked                                                              |
| ---------- | ---------------------------------------------------------------------------------- |
| ESX        | The player's ESX group must have a `true` entry in `Config.AdminGroups`.           |
| QBCore     | QBCore's permission check is called for each group listed in `Config.AdminGroups`. |
| Qbox       | The player must have a matching `group.<name>` ACE, such as `group.admin`.         |
| Standalone | The player must have the `ata_speedbump.admin` ACE.                                |

The explicit `ata_speedbump.admin` ACE works regardless of the detected framework. Custom admin systems can be connected through `Bridge.isAdmin` in `server/editable.lua`.

### 5. Review the configuration

Open `config.lua` and choose your notification mode, streaming distance, maximum placement length and default speed settings. See Config File for the complete reference.

### 6. Start the resource

Restart your server, or run these commands in the server console after adding a new resource folder:

```
refresh
ensure ata_SpeedBump
```

The `ata_speedbumps` table is created automatically on startup. You do not need to import a separate SQL file. The database user needs permission to create the table and read, insert, update and delete its rows.

### 7. Place your first bump

1. Join the server as an authorized administrator.
2. Enter `/speedbump` in chat.
3. Click **New bump** and select a model.
4. Click **Pick points in the world**.
5. Left-click the start point and the end point, then press **Enter**.
6. Click **Next**, review the settings and click **Create**.

Test the placement in a regular vehicle. Emergency-class vehicles are exempt from scripted speed limits and tire spikes by default.

For the full workflow and controls, see Admin Panel.
