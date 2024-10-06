# ataCharCreator

[YouTube Preview](https://youtu.be/FSygYRjfGso)

## **Installation Guide**

in esx\_skin/client/main.lua

find here&#x20;

```lua
AddEventHandler('esx_skin:playerRegistered', function()
    CreateThread(function()
        while not ESX.PlayerLoaded do
            Wait(100)
        end

        if firstSpawn then
            ESX.TriggerServerCallback('esx_skin:getPlayerSkin', function(skin, jobSkin)
                if skin == nil then
                    TriggerEvent('skinchanger:loadSkin', {sex = 0}, OpenSaveableMenu)
                    Wait(100)
                    skinLoaded = true
                else
                    TriggerEvent('skinchanger:loadSkin', skin)
                    Wait(100)
                    skinLoaded = true
                end
            end)

            firstSpawn = false
        end
    end)
end)

```

and replace this

```lua
AddEventHandler('esx_skin:playerRegistered', function()
    CreateThread(function()
        while not ESX.PlayerLoaded do
            Wait(100)
        end

        if firstSpawn then
            ESX.TriggerServerCallback('esx_skin:getPlayerSkin', function(skin, jobSkin)
                if skin == nil then
                    Wait(100)
                    skinLoaded = true
                else
                    TriggerEvent('skinchanger:loadSkin', skin)
                    Wait(100)
                    skinLoaded = true
                end
            end)

            firstSpawn = false
        end
    end)
end)

```

## if you dont use multicharacter   &#x20;

And Go esx\_identity/client/main.lua

```lua
ESX.TriggerServerCallback('esx_identity:registerIdentity', function(callback)
            if not callback then
                return
            end

            ESX.ShowNotification(TranslateCap('thank_you_for_registering'))
            setGuiState(false)

            if not ESX.GetConfig().Multichar then
                TriggerEvent('esx_skin:playerRegistered')
            end
end, data)
```

and replace this

```lua
ESX.TriggerServerCallback('esx_identity:registerIdentity', function(callback)
            if not callback then
                return
            end

            ESX.ShowNotification(TranslateCap('thank_you_for_registering'))
            setGuiState(false)

            if not ESX.GetConfig().Multichar then
                TriggerServerEvent('ataCharCreator:RequestMenuChar')
            end
end, data)
```

## For Multicharacter&#x20;

go esx\_multicharacter/client/main.lua

```lua
	RegisterNetEvent('esx:playerLoaded')
	AddEventHandler('esx:playerLoaded', function(playerData, isNew, skin)
		local spawn = playerData.coords or Config.Spawn
		if isNew or not skin or #skin == 1 then
			local finished = false
			skin = Config.Default[playerData.sex]
			skin.sex = playerData.sex == "m" and 0 or 1
			local model = skin.sex == 0 and mp_m_freemode_01 or mp_f_freemode_01
			RequestModel(model)
			while not HasModelLoaded(model) do
				RequestModel(model)
				Wait(0)
			end
			SetPlayerModel(PlayerId(), model)
			SetModelAsNoLongerNeeded(model)
			TriggerEvent('skinchanger:loadSkin', skin, function()
				local playerPed = PlayerPedId()
				SetPedAoBlobRendering(playerPed, true)
				ResetEntityAlpha(playerPed)
				TriggerEvent('esx_skin:openSaveableMenu', function()
					finished = true
				end, function()
					finished = true
				end)
			end)
			repeat Wait(200) until finished
		end

        DoScreenFadeOut(750)
		Wait(750)

		SetCamActive(cam, false)
		RenderScriptCams(false, false, 0, true, true)
		cam = nil
		local playerPed = PlayerPedId()
		FreezeEntityPosition(playerPed, true)
		SetEntityCoordsNoOffset(playerPed, spawn.x, spawn.y, spawn.z, false, false, false, true)
		SetEntityHeading(playerPed, spawn.heading)
		if not isNew then TriggerEvent('skinchanger:loadSkin', skin or Characters[spawned].skin) end
        Wait(500)

		DoScreenFadeIn(750)
		Wait(750)

		repeat Wait(200) until not IsScreenFadedOut()
		TriggerServerEvent('esx:onPlayerSpawn')
		TriggerEvent('esx:onPlayerSpawn')
		TriggerEvent('playerSpawned')
		TriggerEvent('esx:restoreLoadout')
		Characters, hidePlayers = {}, false
	end)

```

and replace this&#x20;

```lua
RegisterNetEvent('esx:playerLoaded')
AddEventHandler('esx:playerLoaded', function(playerData, isNew, skin)
	local spawn = playerData.coords or Config.Spawn
	if isNew or not skin or #skin == 1 then
		local finished = false
		skin = Config.Default[playerData.sex]
		skin.sex = playerData.sex == "m" and 0 or 1
		local model = skin.sex == 0 and mp_m_freemode_01 or mp_f_freemode_01
		RequestModel(model)
		while not HasModelLoaded(model) do
			RequestModel(model)
			Wait(0)
		end
		SetPlayerModel(PlayerId(), model)
		SetModelAsNoLongerNeeded(model)
		TriggerServerEvent('ataCharCreator:RequestMenuChar')
	end

    DoScreenFadeOut(750)
	Wait(750)

	SetCamActive(cam, false)
	RenderScriptCams(false, false, 0, true, true)
	cam = nil
	local playerPed = PlayerPedId()
	FreezeEntityPosition(playerPed, true)
	SetEntityCoordsNoOffset(playerPed, spawn.x, spawn.y, spawn.z, false, false, false, true)
	SetEntityHeading(playerPed, spawn.heading)
	if not isNew then TriggerEvent('skinchanger:loadSkin', skin or Characters[spawned].skin) end
    Wait(500)

	DoScreenFadeIn(750)
	Wait(750)

	repeat Wait(200) until not IsScreenFadedOut()
	TriggerServerEvent('esx:onPlayerSpawn')
	TriggerEvent('esx:onPlayerSpawn')
	TriggerEvent('playerSpawned')
	TriggerEvent('esx:restoreLoadout')
	Characters, hidePlayers = {}, false
end)
```

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)

**Enjoy**
