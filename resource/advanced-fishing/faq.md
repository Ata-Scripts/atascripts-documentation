# FAQ

## FAQ

<details>

<summary>Which frameworks are supported?</summary>

ESX, QBCore and Qbox are detected automatically. The resource also works without a framework when you grant the `ata_speedbump.admin` ACE and use ox notifications. `ox_lib` and `oxmysql` are required in every setup.

</details>

<details>

<summary>Does the script need inventory items?</summary>

No. Administrators place and manage the objects through the in-game panel. You do not need an inventory integration or usable items.

</details>

<details>

<summary>How do I open the admin panel?</summary>

Use `/speedbump`, or the command set in `Config.Command`. Your player must have permission. See Installation.

</details>

<details>

<summary>I get “You are not allowed to use this.” What should I check?</summary>

Give your administrator group the explicit ACE:

```cfg
add_ace group.admin ata_speedbump.admin allow
```

Make sure your player belongs to that group. Alternatively, check the framework groups in `Config.AdminGroups`. ESX uses the player's group; QBCore uses its permission function; Qbox checks matching `group.<name>` ACEs. A job such as police does not grant admin access by itself.

</details>

<details>

<summary>Do I need to import an SQL file?</summary>

No. The `ata_speedbumps` table is created automatically on startup. Check your oxmysql connection and database permissions if the table is missing.

</details>

<details>

<summary>Are placements saved after a restart?</summary>

Yes. Saved placements are loaded from the `ata_speedbumps` table when the resource starts. Unsaved previews are temporary.

</details>

<details>

<summary>Do changes need a restart?</summary>

Changes saved in the admin panel synchronize automatically. Changes to `config.lua` or the editable Lua integrations require a resource restart. Updating default speed settings does not rewrite existing placements.

</details>

<details>

<summary>Can I disable a bump without deleting it?</summary>

Yes. Open it, switch it to **Off** and click **Save**. Its database record is kept. Switch it back **On** and save when you want it restored.

</details>

<details>

<summary>Why is the finished length different from the line I drew?</summary>

The resource uses complete modular pieces and end caps. It rounds the drawn distance to a fitted model length. UK cushions are separate pieces with gaps. The placement screen shows both the drawn and fitted lengths.

</details>

<details>

<summary>Why do I get “The points are too close together” or “Too long”?</summary>

The selected model needs enough space to fit its pieces. Move the endpoints farther apart if they are too close. If the placement is too long, shorten it or review `Config.MaxLength`, which defaults to 30 meters between endpoints.

</details>

<details>

<summary>Why do tire spikes work in only one direction?</summary>

That is their intended behavior. They burst tires when a vehicle crosses the blades from the wrong direction. Use **Spikes face → Normal / Reversed** to change the permitted direction, then save and test both directions.

</details>

<details>

<summary>Why are police cars or ambulances unaffected?</summary>

`Config.EmergencyIgnore = true` exempts GTA emergency-class vehicles, class 18, from scripted slowdown and tire spikes. It does not remove the physical collision of a speed bump. Set it to `false` to remove the default exemption. Custom vehicles must be assigned to the emergency class to receive it automatically.

</details>

<details>

<summary>Why is a vehicle still above the selected speed when it reaches a bump?</summary>

The slowdown is gradual. Enable **Slow cars down**, check the placement's speed and approach distance, and test with a non-exempt vehicle. Increase the approach distance or review the positive `Config.SpeedLimitSlowdown` value if vehicles enter too quickly to reach the selected speed in time. Another resource controlling vehicle speed may also affect the result.

</details>

<details>

<summary>A placement is invisible, floating or partly below the road. What should I check?</summary>

Make sure it is **On** and within `Config.StreamDistance`. Check that the `stream` folder and `ata_speedbump.ytyp` are present. For alignment problems, stand near the road so its collision is loaded, open **Place → Pick again**, select both points on the intended road surface and save. If the map has changed since placement, re-pick the points on the updated road.

</details>

<details>

<summary>Why do objects disappear when I move far away?</summary>

Placements are streamed around the rendered camera instead of staying spawned everywhere. The default stream distance is 250 meters. Their database records remain saved, and the objects load again when you return.

</details>

<details>

<summary>I cannot see the search field. Is it missing?</summary>

The search field appears after there are more than five saved placements. It searches by placement name or street. Type filters are available separately.

</details>

<details>

<summary>Can I customize notifications, permissions or vehicle exemptions?</summary>

Yes. Use `config.lua`, `client/editable.lua` and `server/editable.lua`. These files are editable in the Escrow version too. See Config File for the available functions.

</details>

<details>

<summary>Can another script read the saved placements?</summary>

Yes. There is a server-side `getBumps` export. Call it after the resource has loaded its database records:

```lua
local bumps = exports['ata_SpeedBump']:getBumps()
```

Use the admin panel to create, update or delete records. The export is for reading the current list.

</details>

<details>

<summary>The resource will not start, or saving fails. What should I check?</summary>

Check the server console and client F8 console for the actual error. Confirm `ox_lib`, `oxmysql` and your framework start before `ata_SpeedBump`. Check your database connection, table permissions and that the extracted folder contains `fxmanifest.lua` directly. For a failed save, also check the selected points and maximum placement length.

If you still need help, [join our Discord](https://discord.gg/5tVUgq8) and include the error, framework, resource version and the steps that reproduce it.

</details>

