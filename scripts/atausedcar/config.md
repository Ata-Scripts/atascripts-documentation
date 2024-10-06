# Config

```lua
Config = {}


Config.Mysql = "oxmysql"   --- oxmysql, ghmattimysql, mysql-async

Config.ESX_1_9_0 = true   ---- if you are using ESX version 1.9 or higher 
Config.GetSharedObject = 'esx:getSharedObject'  --- if you are using ESX version 1.8.9 or lower version ESX


Config.GithubVersionCheck = true

Config.GithubName = 'ataUsedCarMarket_ESX' -----!!!! DONT CHANGE PLEASEEE !!!!

Config.BuyWithBank = false  --- if false player need to buy with cash 
Config.Commission_Percentage = 10 ---The default amount is 10%, that is, the money that is credited to the car owner's account is reduced by 10%

Config.UsedMarket = { --- location market NPC and open market place 
    pedcoords = vector4(-56.834819793701,-1098.7476806641,25.422330856323, 25.567827224731), --- NPC coord
    pedModel = 'a_m_y_business_01', --- NPC model
    markercoord = vector3(-57.235652923584,-1097.29296875,25.422338485718),
    markerConfig = {
        Type = 1,
        rgb = {r = 255, g = 255, b = 0}
    },
    blip = {
        color = 48,
        name = 'Used Car Market',
        scale = 1.0,
        sprite = 524
    }
}

Config.Coordinates = {
    SpawnVehicleBUY = {
        coord = vector3(-10.687877655029,-1098.7456054688,26.672069549561),
        heading = 156.90705871582
    },
    SpawnTestVehicle = {
        coord = vector3(-1058.7164306641,-2902.3742675781,13.527755737305),
        heading = 169.27891540527
    },
    SpawnPreviewVehicle = {
        coord = vector3(-43.035690307617,-1098.615234375,26.422353744507),
        heading = 69.159294128418
    },


}


Config.Ui = {
    ['What does the day mean ?'] = {
        'It is your time to advertise. if your car is not sold, it will return to your garage during the day you chose'
    },
    ['Sales commission ?'] = {
        'The sales commission after the sale is 10%, which means the amount you enter will be reduced by 10% and will be deposited into your account after sale'
    },
    ['Be sure to read'] = {
        'After placing the ad, your car will be removed from the city and will be transferred to the garage of the car dealer, and after the end of the sales period, it will return to your garage. Also, your ad cant be edited or deleted, so be sure to use the ad'
    },

}


Config.Local = {
    ['1'] = 'Someone bought your vehicle and transferred $',
    ['2'] = 'Press ~INPUT_CONTEXT~ To Open ~y~Used Car Market',
}


function helptext(str)
	SetTextComponentFormat("STRING")
	AddTextComponentString(str)
	DisplayHelpTextFromStringLabel(0, 0, 1, -1)
end
  

function Notification(msg)
    exports['ataNotification']:notification(
    'far fa-check-circle text-success',
    'Used Car Market',
    "INFORMATION",
    msg,
    15000)
end
```
