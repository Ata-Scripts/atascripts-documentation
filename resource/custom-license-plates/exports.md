# Exports

## server

```lua
-- for MDT, radar and police scripts: what is known about a plate (shown or real)
local info = exports.ata_VehiclePlate:LookupPlate('B AT 2026')
-- { plate, realPlate, bought, kind, country, design, installed, owner, ownerName, model }

local owner, name = exports.ata_VehiclePlate:GetVehicleOwner(vehicle)
local vehicle = exports.ata_VehiclePlate:GetVehicleByPlate('B AT 2026')
local hidden = exports.ata_VehiclePlate:IsPlateHidden(vehicle)        -- flipped or no plate
local shown, real = exports.ata_VehiclePlate:GetVehiclePlate(vehicle)

exports.ata_VehiclePlate:GetPlateOwner(text)
exports.ata_VehiclePlate:GetPlateData(text)
exports.ata_VehiclePlate:GetPlayerPlates(source)
exports.ata_VehiclePlate:HasPlate(source, text)
exports.ata_VehiclePlate:IsPlateAvailable(text)

exports.ata_VehiclePlate:GivePlate(source, text, data)
exports.ata_VehiclePlate:RemovePlate(text)
exports.ata_VehiclePlate:InstallPlate(text, vehicle)
exports.ata_VehiclePlate:UninstallPlate(text)
exports.ata_VehiclePlate:TransferPlate(text, source)
exports.ata_VehiclePlate:SetVehiclePlate(vehicle, text)
exports.ata_VehiclePlate:RefreshVehiclePlate(vehicle)                 -- after your script changed the real plate

exports.ata_VehiclePlate:SetVehiclePlateHolder(vehicle, style, finish) -- nil style removes it
```

## client

```lua
local info = exports.ata_VehiclePlate:GetPlateInfo(vehicle)
-- { plate, realPlate, country, design, hidden, holder }

exports.ata_VehiclePlate:GetVehiclePlate(vehicle)
exports.ata_VehiclePlate:IsPlateHidden(vehicle)
exports.ata_VehiclePlate:OpenPlateShop()
exports.ata_VehiclePlate:OpenPlateDesigner(text)
```

## tebex

package command

```
purchase_plate {"transid":"{transaction}","type":"len1"}
```

use `len2` or `custom` for the other packages
