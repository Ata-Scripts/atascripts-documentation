# FAQ

## FAQ

<details>

<summary>Which frameworks are supported?</summary>

All of them. The resource is standalone: it works with ESX, QBCore, Qbox or no framework at all. It does not need a database, ox\_lib or oxmysql.

</details>

<details>

<summary>How do I open the editor?</summary>

Type `/soundadmin` in chat. Your player needs the `ata_ambientsound.admin` ACE. From the server console you can open it for a player with `soundadmin <player ID>`.

</details>

<details>

<summary>I get "You do not have permission to edit sound zones." What should I check?</summary>

Add the ACE to your admin group and make sure your player is in that group:

```cfg
add_ace group.admin ata_ambientsound.admin allow
add_principal identifier.license:REPLACE_WITH_PLAYER_LICENSE group.admin
```

A framework group such as ESX `admin` does not give the ACE by itself.

</details>

<details>

<summary>Do I need to import an SQL file?</summary>

No. Zones and global sounds are saved in `ata_AmbientSound/data/zones.json`. A backup of the previous version is kept in `data/zones.backup.json` on every save.

</details>

<details>

<summary>A player crashed when I restarted the resource. Why?</summary>

`ata_AmbientSound` contains GTA audio data (the wind and background mute), which the game loads when a player joins. Restarting or stopping it while players are connected can crash them. Update it with a server restart or when nobody is online. Restarting `ata_AmbientCreator` is safe.

</details>

<details>

<summary>I do not hear a zone. What should I check?</summary>

* The zone is **On** and has a sound.
* You are inside it, or within its **Heard from outside** distance.
* Turn on the debug view (bug button) to see the zone and a line to every sound you hear.
* Your game's music / effects volume is not muted.
* The sound file name has no spaces (see below).

Only the 8 nearest zones play at the same time (`MaxAudibleZones`).

</details>

<details>

<summary>I added a sound but it does not play, or it is missing from the library.</summary>

Use only letters, digits, `_`, `-` and `.` in the file name. FiveM cannot serve files with spaces; the server console names any file you must rename. Files must be `.mp3`, `.ogg` or `.wav` inside `html/sounds`, and the server must be restarted after adding them.

</details>

<details>

<summary>How do I get GTA's own ambience and wind back?</summary>

Set `MuteGtaAmbience = false` in `shared/config.lua` to keep GTA's birds, city hum and traffic. Set `NoWind = false` to let wind move trees and flags again. The wind sound itself stays muted by the resource's audio data.

</details>

<details>

<summary>Why are trees and flags not moving?</summary>

`NoWind = true` keeps the wind at 0 so GTA's wind does not rumble under your ambience. Set it to `false` if you prefer moving trees.

</details>

<details>

<summary>The sounds are too loud or too quiet.</summary>

Set each zone's **Volume** in the editor. `MaxVolume` (0.6 by default) is what 100% in the editor means, so raise or lower it to change all sounds at once.

</details>

<details>

<summary>SHIFT does not highlight an interior or a prop.</summary>

Hold SHIFT and point the crosshair directly at the building or object. Some map objects are part of the map itself and cannot be picked as props; draw the corners around them instead. For interiors you can also stand inside and use **Use the interior I'm standing in**.

</details>

<details>

<summary>The Create Custom Ambient button is grey.</summary>

`ata_AmbientCreator` is not running. Check that it is started after `ata_AmbientSound`, that the `yarn` resource is running, and that these lines are in `server.cfg` before the server starts:

```cfg
add_unsafe_child_process_permission ata_AmbientCreator
add_filesystem_permission ata_AmbientCreator write ata_AmbientSound
```

Restart the whole server after adding them.

</details>

<details>

<summary>Does Create Custom Ambient work on Linux servers?</summary>

Yes. FFmpeg for Windows is included. On Linux it is downloaded once on the first start, so the server needs internet access that one time.

</details>

<details>

<summary>Do I need to restart after creating a custom mix?</summary>

No. A new mix is available right away for every player. It is sent to players by `ata_AmbientCreator` until the next server restart, after which it is served like the other sounds.

</details>

<details>

<summary>Can I delete a custom mix?</summary>

Yes. Open the sound library, click the mix and use the trash button. A mix that is still used by a zone or a global area cannot be deleted; give those another sound first.

</details>

<details>

<summary>Can I use a sound from a website?</summary>

Yes. In the sound library use **Own link** and paste a direct `.mp3` or `.ogg` link. The website must allow CORS, otherwise the sound will not play. YouTube links are not supported.

</details>

<details>

<summary>Does it affect performance with many zones?</summary>

No. Only the 8 nearest zones play at the same time, sounds are streamed instead of fully decoded, and the server only sends the zone list when it changes. Up to 200 zones can be saved (`MaxZones`).

</details>

<details>

<summary>How much do players download?</summary>

Every player downloads the sound files once when they join, then they are cached. With the full library this is about 310 MB. Remove sounds you do not use from `html/sounds` to make it smaller.

</details>

<details>

<summary>Can I change the global sound areas?</summary>

Yes. They are defined in `shared/regions.lua` with world x/y corners. Keep each area's `id` unchanged after giving it a sound.

</details>

<details>

<summary>Which files can I edit in the Escrow version?</summary>

`shared/config.lua` and `shared/regions.lua` in `ata_AmbientSound`, and the whole `ata_AmbientCreator` resource. The Open Source version provides the complete source code.

</details>

<details>

<summary>The resource will not start, or saving fails. What should I check?</summary>

Check the server console and the client F8 console for the actual error. Make sure the folders are named `ata_AmbientSound` and `ata_AmbientCreator` and contain `fxmanifest.lua` directly. If saving fails, check that `data/zones.json` is not read-only or broken; when it is broken, saving is turned off to protect it and the editor shows a warning.

If you still need help, [join our Discord](https://discord.gg/5tVUgq8) and include the error, your framework, the resource version and the steps that reproduce it.

</details>
