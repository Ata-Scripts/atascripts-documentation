# ataEinreise

#### [YouTube Preview](https://youtu.be/HHfDjquF7zc?si=zdxIf0GtfuS3WblD)

#### Execute the following SQL code in your database:

```sql
ALTER TABLE `users` ADD COLUMN
(
  `entry_type` varchar(50) DEFAULT NULL,
  `entry_test` tinyint(1) DEFAULT 0
    
) 
```

## if you are using default esx\_skin

in esx\_skin/client/main.lua

add

```lua
local aNew = false 
```

And Find This Code&#x20;

```lua
function OpenSaveableMenu(submitCb, cancelCb, restrict)
    TriggerEvent('skinchanger:getSkin', function(skin) lastSkin = skin end)

    OpenMenu(function(data, menu)
        menu.close()
        DeleteSkinCam()

        TriggerEvent('skinchanger:getSkin', function(skin)
            TriggerServerEvent('esx_skin:save', skin)

            if submitCb ~= nil then
                submitCb(data, menu)
            end
        end)
    end, cancelCb, restrict)
end
```

And Replace This

```lua
function OpenSaveableMenu(submitCb, cancelCb, restrict)
    TriggerEvent('skinchanger:getSkin', function(skin) lastSkin = skin end)

    OpenMenu(function(data, menu)
        menu.close()
        DeleteSkinCam()

        TriggerEvent('skinchanger:getSkin', function(skin)
            TriggerServerEvent('esx_skin:save', skin)

            if aNew then
                TriggerServerEvent('ataEntry:CheckPlayer')
                aNew = false
            end

            if submitCb ~= nil then
                submitCb(data, menu)
            end
        end)

    end, cancelCb, restrict)
end
```

And Find This&#x20;

```lua
AddEventHandler('esx_skin:playerRegistered', function()
    CreateThread(function()
        while not ESX.PlayerLoaded do
            Wait(100)
        end

        if firstSpawn then
            ESX.TriggerServerCallback('esx_skin:getPlayerSkin', function(skin)
                if skin == nil then
                    TriggerEvent('skinchanger:loadSkin', { sex = 0 }, OpenSaveableMenu)
                    Wait(100)
                else
                    TriggerEvent('skinchanger:loadSkin', skin)
                    Wait(100)
                end
            end)

            firstSpawn = false
        end
    end)
end)
```

And Replace This&#x20;

```lua
AddEventHandler('esx_skin:playerRegistered', function()
    CreateThread(function()
        while not ESX.PlayerLoaded do
            Wait(100)
        end

        if firstSpawn then
            ESX.TriggerServerCallback('esx_skin:getPlayerSkin', function(skin, jobSkin)
                if skin == nil then
                    aNew = true
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

## If You Are Using ataCharCreator

in ataCharCreator/config/client.lua

```lua
RegisterNetEvent('ataCharCreator:PlayerSuccessSpawn')
AddEventHandler('ataCharCreator:PlayerSuccessSpawn', function()
    TriggerServerEvent('ataEntry:CheckPlayer')
end)
```

## In esx\_identity

go esx\_identity/client/main.lua

```lua
RegisterNetEvent('esx_identity:alreadyRegistered', function()
    while not loadingScreenFinished do Wait(100) end
    TriggerEvent('esx_skin:playerRegistered')
end)
```

and replace this&#x20;

```lua
RegisterNetEvent('esx_identity:alreadyRegistered', function()
    while not loadingScreenFinished do Wait(100) end
    TriggerEvent('esx_skin:playerRegistered')
    TriggerServerEvent('ataEntry:CheckPlayer')
end)
```

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)

Enjoy
