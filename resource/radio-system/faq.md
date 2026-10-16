# FAQ

## FAQ

<details>

<summary>Which frameworks are supported?</summary>

ESX, QBCore and Qbox. The script finds the running framework by itself. It also runs with no framework at all (standalone).

</details>

<details>

<summary>Which inventories are supported?</summary>

ALL OF INVENTORY IN FIVEM

</details>

<details>

<summary>I use another framework, inventory or notification script. What do I need to change?</summary>

Only `client/editable.lua` and `server/editable.lua`. The job, admin check, inventory and notification functions are all in these two files.

</details>

<details>

<summary>Who can open the admin panel?</summary>

Players with the `command` ace, or with one of the groups in `Config.AdminGroups`. On ESX it is the player group. On QBCore and Qbox it is the ace with that name. On standalone, give the ace yourself:

```
add_ace group.admin admin allow
```

</details>

<details>

<summary>Do I need to restart after changing something in the admin panel?</summary>

No. The change is saved to `config.lua` and applied to all players right away.

</details>

<details>

<summary>How many channels can a player join?</summary>

Up to `Config.MaxChannels`, and never more than four. The handheld, earpiece and vehicle radio share this limit.

</details>

<details>

<summary>Does the handheld radio need an item?</summary>

Yes. The handheld opens by using the `radio` item and the earpiece by using the `earpiece` item; there is no key for either. If the player loses the earpiece item, the earpiece disconnects.

</details>

<details>

<summary>How do players open the vehicle radio?</summary>

With the `/car_radio` command.

</details>

<details>

<summary>Can players put a password on any frequency?</summary>

if ferequance is empty , yes they can but all of players need password to join&#x20;

</details>

<details>

<summary>Can dead players use the radio?</summary>

No. Dead or downed players cannot open the radio or connect to a channel. You can add your own ambulance state in `Editable.isDead`.

</details>

<details>

<summary>Players get "Channel unavailable. Check access and the pma-voice radio bridge."</summary>

Check that the three lines from the Installation page are in `pma-voice/fxmanifest.lua`, and that `voice_enableRadios` is not set to `0`.

</details>

<details>

<summary>The client shows "ata_Radio bridge must load after pma client scripts".</summary>

The `client_script` line is not at the end of `pma-voice/fxmanifest.lua`. Move it to the bottom of the file.

</details>

<details>

<summary>I updated pma-voice and the radio stopped working.</summary>

The update replaced `pma-voice/fxmanifest.lua`. Add the three lines from the Installation page again.

</details>

<details>

<summary>The jammer prop does not show.</summary>

The prop needs game build 3095 or newer.

</details>

<details>

<summary>What happens when the jammer timer ends?</summary>

The jammer switches off, but the prop stays in the world until someone picks it up or an admin deletes it.

</details>

<details>

<summary>A vehicle is not in the Vehicles tab. Can it still have a radio?</summary>

Yes. Turn on **Radio in every vehicle** in the Settings tab and enter a frequency. Vehicles missing from the list will use it.

</details>

<details>

<summary>The vehicle radio says it needs a free HUD slot.</summary>

The player is already connected to the maximum number of channels. The vehicle radio connects as soon as they leave one.

</details>

<details>

<summary>How do I add my own talking animation?</summary>

Add a new entry to `Config.Animations` with its `label`, `dict` and `clip`, and an `image` for its card in the menu. If the animation pack is missing on the server, the radio uses the default animation instead.

</details>

<details>

<summary>Can I run my own code when a player talks on the radio?</summary>

Yes. `Editable.onTalking` is called when a player starts or stops talking. It exists in both `client/editable.lua` and `server/editable.lua`.

</details>
