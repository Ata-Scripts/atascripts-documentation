# FAQ

### the plate is in the wrong spot on an add-on car

stand next to it and use `/platefix`, its saved for that model

### the old plate frame shows under the new plate

add the model name to `Config.FrameCoverModels`

### players cant put a plate on their car

by default only the owner can, set `Config.Bridge.keyHolders = true` to let key holders do it too, or change `Hooks.canUseVehicle` in `bridge/editable_server.lua`

### my garage shows the old plate

your garage keeps the plate in a table the script doesnt know, add it to `Config.PlateLinks` or `Config.VehicleTable`, see [Editable Files](editable-files.md)

### can i restart the script on a live server

yes, plates, holders and flips come back for everyone

### i changed config.lua but nothing changed in game

settings saved in `/plateadmin` win over the config, press **Reset to config.lua** in that section

### the shop doesnt open

check `Hooks.canOpenShop` in `bridge/editable_client.lua`, and that you didnt set `Config.Shop.command = ''`

### support

ask us in our [discord](https://discord.gg/vZvCU7cSst)
