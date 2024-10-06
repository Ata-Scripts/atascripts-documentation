# Config

```lua
local QBCore = nil
local ESX = nil

Config = {}

Config.FrameWork = 'ESXNEW' -- Only supports ESX and ESXNEW and QBCORE

Config.Mysql = 'oxmysql'   ----- ghmattimysql , mysql-async , oxmysql

Config.UseDiscordAvatar = true   ---- for use discord avatar player to show in scoreboard

Config.discordToken = 'Discord Api'  ---- discord token https://atarevals.gitbook.io/docs/

Config.SteamApi = 'Steam Api'  ---- steamapi https://atarevals.gitbook.io/docs/

Config.CoolDownForNextRace = 60   -- Default value 60 min , for disable cool down for each race you can set this to 0 

Config.LevelCheckPoint = {   -- time for next lap 
    easy = 8000,   ----- 8 sec
    medium = 5000, ---- 5 sec
    hard = 2000 --- 2 sec
}

Config.GithubVersionCheck = true ------ version check


Config.GithubName = 'ataRace' -----!!!! DONT CHANGE PLEASEEE !!!!


Config.Race = {
    {
        raceLocation = vector3(1720.7114257813,3466.2697753906,38.343364715576),  ---- location for scoreboard
        raceVehicleSpawn = {
            vector4(1730.1435546875,3451.6774902344,38.528415679932,208.49067687988), ---- vehicle spawn
            vector4(1727.5966796875,3450.9165039063,38.530387878418,208.49067687988), ---- vehicle spawn
        },
        raceName = 'Sandy Shores', ---- Race name (Sandy Shores,pillbox)
        level = 'easy', --- Config.LevelCheckPoint for next checkpoint time
        raceImage = 'https://preview.redd.it/35yxksg5ezgz.jpg?auto=webp&s=30f4967951abd4fa15206b946889eb63d6ab5ff3',  ---- race image
        laps = {
            vector3(1784.8057861328,3354.1469726563,40.136344909668), -- lap
            vector3(1828.5816650391,3280.9831542969,43.217342376709), -- lap
            vector3(1900.4619140625,3188.3620605469,45.678142547607),-- lap
            vector3(1975.4272460938,3123.5456542969,46.620094299316),-- lap
            vector3(2111.7082519531,3048.3359375,45.151973724365),-- lap
            vector3(2223.2810058594,3014.5288085938,44.794319152832),-- lap
            vector3(2315.7416992188,2986.0737304688,47.02131652832),-- lap
            --- you can add more laps
            },
        illegal = false,  -- Race is illegal or not
        availableVehicle = { ---Can be left empty here to allow all cars
            -- 't20',
            -- 'sultanrs'
        }, 
        blip = { --- blip setting
            haveBlip = true,
            blipCode = 315,
            blipSize = 1.0,
            BlipColor =0,
            BlipName = 'Race'
        },
    },
    -- {
    --     raceLocation = vector3(3690.4001464844,4463.1259765625,23.133003234863),
    --     raceVehicleSpawn = {
    --         vector4(1730.1435546875,3451.6774902344,38.528415679932,208.49067687988),
    --         vector4(1727.5966796875,3450.9165039063,38.530387878418,208.49067687988),
    --     },
    --     raceName = 'Boat Garage',
    --     level = 'hard',
    --     raceImage = 'https://cdn.discordapp.com/attachments/1068377936383709257/1078524362417778799/image.png',
    --     laps = {
    --         vector3(1784.8057861328,3354.1469726563,40.136344909668),
    --         vector3(1828.5816650391,3280.9831542969,43.217342376709),
    --         vector3(1900.4619140625,3188.3620605469,45.678142547607),
    --         vector3(1975.4272460938,3123.5456542969,46.620094299316),
    --         vector3(2111.7082519531,3048.3359375,45.151973724365),
    --         vector3(2223.2810058594,3014.5288085938,44.794319152832),
    --         vector3(2315.7416992188,2986.0737304688,47.02131652832),
    --         },
    --     illegal = true,
    --     availableVehicle = {},
    --     blip = {
    --         haveBlip = true,
    --         blipCode = 315,
    --         blipSize = 1.0,
    --         BlipColor =0,
    --         BlipName = 'Race'
    --     },
    -- },
}



function GetFrameWork()
    return Config.FrameWork
end

if GetFrameWork() == 'ESX' then
    Citizen.CreateThread(function()
        while ESX == nil do
            TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)
            Citizen.Wait(0)
        end
    end)
elseif GetFrameWork() == 'QBCORE' then
    
    QBCore = exports['qb-core']:GetCoreObject()
elseif GetFrameWork() == 'ESXNEW' then
    ESX = exports["es_extended"]:getSharedObject()
end


function Notify(message)
    if GetFrameWork() == 'ESX' then
        ESX.ShowNotification(message, false, false, w)
    elseif GetFrameWork() == 'QBCORE' then
        QBCore.Functions.Notify(message, "primary")
    end
end
```
