# Admin Panel

## Admin Panel

Open the editor with `/soundadmin`. Only admins can open it (see Installation). From the server console you can open it for a player with `soundadmin <player ID>`.

Everything saved in the editor is synchronized with all players automatically. You do not need to restart anything after creating or editing a zone.

### Main screen

* **Create Zone:** start a new sound zone. The fly camera opens right away.
* **Global Sounds:** background sounds for whole areas of the map.
* **✨ button:** Create Custom Ambient (needs `ata_AmbientCreator`).
* **Find a zone:** search your zones by name.
* **Zone cards:** each zone shows a small map, its name, its sound and whether it is On or Off. **Edit** opens it, **Go** teleports you to it.
* **Bug button:** shows the debug view in the world: zone walls, your listening point and a line to every sound you hear, with its distance and volume.

### Create a zone

Click **Create Zone**. A fly camera opens above you.

#### Draw an area

1. Fly to the place you want.
2. Left-click the corners of the area. The walls appear live as you add corners.
3. Press **Enter** when you are done.

#### Pick an interior / MLO

Hold **SHIFT** and point at a building. When an interior or MLO is detected it is highlighted in blue with its number of rooms. Left-click while holding SHIFT to use the whole interior: the sound plays in every room and floor, and is heard muffled from outside.

You can also stand inside the building and use **Use the interior I'm standing in** on the Area tab.

#### Pick a prop

Hold **SHIFT** and point at a prop, such as a tree, a fountain, a street light or a bench. A blue box shows the size of the zone. Left-click while holding SHIFT to create a zone around it. The zone is a box the size of the prop's model plus `Placing.propPadding` (1.5 m by default). Only its coordinates are saved; the prop itself is not tracked, so it costs no performance.

| Control                             | Action                                       |
| ----------------------------------- | -------------------------------------------- |
| Mouse movement                      | Look around.                                 |
| W / A / S / D                       | Fly.                                         |
| E / Q                               | Up / down.                                   |
| Left Ctrl                           | Fly faster.                                  |
| Left Mouse Button                   | Add a corner.                                |
| Right Mouse Button                  | Undo the last corner.                        |
| Hold Left Shift + Left Mouse Button | Pick the highlighted interior / MLO or prop. |
| Enter                               | Finish.                                      |
| Backspace                           | Cancel.                                      |

The keys can be changed in `Placing` in the config.

### Sound tab

* **Zone name:** optional. If you leave it empty, the zone is named after its street and area, for example `Elgin Ave, Legion Square`.
* **Sound:** press **Browse** to open the sound library.
* **Moon button:** turns on day & night. A second sound card appears for the night. The two sounds crossfade at the night hours set in `Night` (20:00 to 06:00 by default, game time).
* **Volume:** 1% to 100%. 100% equals `MaxVolume` of full volume.
* **Heard from outside:** 5 to 200 m. How far outside the zone the sound can still be heard. It gets quieter and darker with distance.
* **Show walls and play sound:** see the zone and hear it live while you edit.

### Area tab

Shows the zone on the map with its corners or interior.

* **Draw area or pick interior / Edit corners in the world:** opens the fly camera again.
* **My spot:** adds a corner where you stand.
* **Undo / Eraser:** remove the last corner or all corners.

Click **Save** to save the zone. To delete a zone, open it and use the trash button, then confirm. Deleting cannot be undone; switch the zone **Off** instead if you may need it again.

### Sound library

The library contains every sound file of the resource, plus your custom mixes.

* **Search:** by name or file name.
* **Category icons:** filter by category. Hover an icon to see its name.
* **Click a sound** to play it. The waveform shows the whole sound; click anywhere on it to jump there.
* **Use this sound:** puts it on the zone or area.
* **Own link:** use a direct `.mp3` / `.ogg` link from another website instead. The website must allow CORS.
* **Custom mixes** have a trash button to delete them for good. A mix that is still used by a zone or area cannot be deleted.

### Global Sounds

Click **Global Sounds** to see the whole GTA map split into 16 areas. Areas without a sound are grey with a "no sound" icon. Hover or click an area to see its name and sound.

1. Click an area on the map.
2. Click **Give it a sound**, pick a sound and set its volume. The moon button adds a night sound here too.
3. Click **Save**.

The global sound plays everywhere in that area, blends into the next area at the border, and fades out as you get close to one of your own zones, so a zone always replaces the background instead of playing on top of it.

### Create Custom Ambient

Click the **✨** button next to Global Sounds. It needs `ata_AmbientCreator`; the button is grey when it is not running.

1. Search or pick a category, then click sounds to add them. They start playing right away.
2. Set each sound's own volume with its slider. Up to 8 sounds per mix.
3. Enter a name and choose the loop length: 1, 3 or 5 minutes.
4. Click **Save**.

After a few seconds the mix is in the sound library under **Custom mixes**, ready for any zone or area, for every player, without a restart.
