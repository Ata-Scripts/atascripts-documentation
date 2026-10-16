# Admin Panel

## Admin Panel

Open the panel with `/speedbump`. If you changed `Config.Command`, use your configured command instead.

Only authorized administrators can open the panel or save and delete placements. See Installation for permissions.

Changes saved in the panel are stored in the database and synchronized with players automatically. You do not need to restart the resource after creating or editing a placement.

### Placement list

The main screen shows your saved placements, their model type, length, speed limit when enabled, and On/Off status.

* **New bump:** Start creating a placement.
* **All / Bumps / Humps / Cushions / Spikes:** Filter the list by type.
* **Search:** Find placements by name or street. The search field appears when there are more than five saved placements.
* **Placement row:** Open that placement for editing.
* **Go there pin icon:** Teleport to the placement.
* **Eye icon:** Toggle in-world admin labels.

### Create a placement

#### 1. Model

Click **New bump** and select one of the four models:

| Model            | Description                                               | Scripted slowdown enabled by default |
| ---------------- | --------------------------------------------------------- | ------------------------------------ |
| Speed Bump       | Short yellow-and-black rubber bump.                       | Yes                                  |
| Speed Hump       | Wider asphalt hump with painted stripes.                  | Yes                                  |
| UK Speed Cushion | Separate cushions with gaps between them.                 | Yes                                  |
| Tire Spikes      | One-way blades that burst tires from the wrong direction. | No                                   |

You can change the slowdown setting later, including on tire spikes.

#### 2. Place

Click **Pick points in the world**. A free camera opens above the road.

1. Move the camera to the road you want to use.
2. Left-click to set the **Start** point.
3. Move the cursor to the opposite end of the placement. The ghost preview follows your cursor.
4. Left-click to set the **End** point.
5. Press **Enter** to return to the menu with both points selected.

Draw across the road to span the traffic lanes. The two points determine the placement's direction and length; the pieces follow the road surface automatically.

| Control            | Action                              |
| ------------------ | ----------------------------------- |
| Mouse movement     | Look around.                        |
| W / A / S / D      | Move the camera.                    |
| E / Q              | Move up / down.                     |
| Left Shift         | Move faster.                        |
| Left Mouse Button  | Set the next point.                 |
| Right Mouse Button | Undo the last point.                |
| Enter              | Confirm after selecting two points. |
| Backspace          | Cancel point picking.               |

These are the default keyboard controls. The four point-picking actions can be changed in `Config.Placing`.

The menu shows the drawn distance, fitted length and piece count. Lengths snap to complete model pieces, so the fitted length can differ slightly from the distance you drew. UK cushions use separate pieces with gaps.

Use **Pick again** to change the endpoints. Toggle **Show it in the world** to show or hide the model preview while editing. Click **Next** to open Settings.

#### 3. Settings

* **Name:** Optional label, up to 40 characters. If empty, the menu uses the street name or a model-based fallback.
* **Slow cars down:** Enable or disable the scripted speed limit for this placement.
* **Speed on arrival:** Choose 10–80 km/h in steps of 5.
* **Starts slowing down:** Choose 10, 15, 25 or 40 meters before the placement.
* **Spikes face:** For Tire Spikes, choose **Normal** or **Reversed** to switch the permitted crossing direction.
* **On / Off:** Set whether the placement is active in the world.

Click **Create** to save the new placement.

Speed limits reduce the vehicle's speed cap gradually. The approach distance and global slowdown rate affect how much speed a fast vehicle loses before reaching the bump.

### Tire spike direction

Tires are safe from the spike logic when crossing in the permitted direction. Crossing the blade line from the opposite direction bursts tires.

Use the world preview's direction guide and test both directions with a regular vehicle. If the permitted direction is wrong, change **Spikes face** to **Reversed** and save.

Emergency-class vehicles are exempt by default. Turn off `Config.EmergencyIgnore`, or customize `Bridge.ignoreSpikes`, if you want different behavior.

### Edit an existing placement

Click its row in the list. Existing placements open on the **Settings** step, and you can switch to **Model** or **Place** to change the type or pick new points.

Click **Save** to apply your changes. **Cancel** discards unsaved edits.

### Temporarily disable a placement

Open the placement, set the top **On / Off** switch to **Off**, then click **Save**.

The saved record remains in the database, but its objects and driving effects are removed from the world. Turn it back **On** and save to restore it.

### Delete a placement

Open it, click the trash icon and confirm **Delete**. The placement is removed from the database and from every player's world.

Deletion cannot be undone from the panel. Use **Off** instead if you may want the placement again later.

### In-world labels

Opening the panel enables admin labels. Use the eye icon to toggle them.

After closing the panel, nearby labels show the type, ID, name or street, length and speed setting. Stand near the placement on foot and press **E** to reopen it for editing. This shortcut is separate from the E key used to raise the camera during point picking.

### Close the panel

Click the close icon on the main list or press **Escape**. While editing, Escape returns to the list first. In a delete confirmation, Escape dismisses the confirmation first.
