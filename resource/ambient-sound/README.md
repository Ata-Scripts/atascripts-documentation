# Ambient Sound

Give any place on your map a living soundscape. Draw an area, pick a building interior / MLO or a prop directly in game, choose a sound and every player hears it with realistic 3D audio.

Inside a zone the sound is all around you. Outside it comes from the zone's edge, gets darker with distance like in real air and sounds muffled through walls. Loops are seamless, fades are smooth, and GTA's own ambience and wind are muted so only your soundscape plays. Everything is managed from an in-game editor: no coordinates, no config editing.

The package contains two resources:

* **ata\_AmbientSound**: sound zones, global sounds, the sound library and the in-game editor.
* **ata\_AmbientCreator** (optional): the backend for **Create Custom Ambient**, which mixes up to 8 sounds into one seamless loop.

The resource is standalone. It does not need a framework, a database or ox\_lib.

### Features

* **Sound zones:** draw any shape with a fly camera, or hold **SHIFT** to pick a whole interior / MLO or a prop such as a tree, fountain or bench.
* **Global Sounds:** background ambience for 16 areas of the map, blended at the borders and faded out near your own zones.
* **Sound library:** 360+ ambient sounds in 13 categories, with search and a waveform preview. Drop your own files in and they are added automatically.
* **Create Custom Ambient:** layer rain, birds, traffic and more with live preview and save them as one loop that every player can use right away.
* **Day & night:** a second sound for the night on any zone or area, crossfaded with the game clock.
* **Realistic audio:** 3D direction, air absorption, walls and interiors, smooth fades and a shared clock so loops never restart from the beginning.
* **Low memory:** sounds are streamed instead of fully decoded, so even long recordings stay light.

{% hint style="info" %}
### Versions

The Escrow version keeps `shared/config.lua` and `shared/regions.lua` editable, and `ata_AmbientCreator` is fully open. The Open Source version provides access to the complete source code of both resources.
{% endhint %}

***

note: that this software file is protected by DMCA protection and its illegal sale or distribution is prohibited.
