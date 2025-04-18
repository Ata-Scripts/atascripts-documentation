# Config File

```lua
Config = {}
Config.Framework = 'esx'
Config.Mysql = "oxmysql"

Config.Blip = {
    Enable = true,
    blipLabel = "24/7 Shop", 
    blipSprite = 52, 
    blipColor = 2,
}

Config.TargetType = "default" 

Config.InventorySystem = 'esx_inventory'

Config.npcEnable = true
Config.npcModel = "mp_m_shopkeep_01"

Config.ShopLocations ={
    vector4(24.47708, -1347.334, 29.49702, 275.1495),
    vector4(-1186.56, -458.9171, 87.39479, 38.15356),
}

Config.ShopItems = { 
    {name = 'nugget', label = 'nugget', category = 'foods', price = 64, image = 'img/items/burger-shotnuggets.png'},
    {name = 'borger', label = 'borger', category = 'foods', price = 24, image = 'img/items/burger-moneyshot.png'},
    {name = 'shotburger', label = 'shotburger', category = 'foods', price = 34, image = 'img/items/burger-shotrings.png'},
    {name = 'bread', label = 'bread', category = 'foods', price = 61, image = 'img/items/bread.png'},
    {name = 'egg', label = 'egg', category = 'foods', price = 109, image = 'img/items/farming_egg.png'},
    {name = 'colaa', label = 'softcola', category = 'drinks', price = 100, image = 'img/items/ecolalight.png'},
    {name = 'farming_applejuice', label = 'apple jiuce', category = 'drinks', price = 79, image = 'img/items/farming_applejuice.png'},
    {name = 'burger-softdrink', label = 'Cola', category = 'drinks', price = 67, image = 'img/items/burger-softdrink.png'},

} 
Config.SellItems = { 

    {name = 'diamond_necklace_silver', label = 'diamond', price = 9000, image = 'img/items/diamond_necklace_silver.png'},
    {name = 'xboxx', label = 'xBoxx', price = 11000, image = 'img/items/xboxx.png'},
    {name = 'dirtyneedle', label = 'needle', price = 360, image = 'img/items/dirtyneedle.png'},
} 

Config.UI = {
  shopname = "24/7 SHOP",
  shoplocation = "LOS SANTOS",
  playername = "Loading",
  imprtant = "IMPORTANT:",
  descimportant =
    "Lorem ipsasdasd asd asd um, dolor sit amet consectetur adipisiasdasdcing elit.Sapiente repellat architecto exercitationem inventore eos odio! Provident, deleniti accusantium vel quasi harum nisi! Asperiores repellendus vel voluptatum corporis, quisquam sed nam.",
}


function openHelpKeyboard()
    ShowHelpNotification("Press ~INPUT_TALK~ to open the shop")
    
end

function ShowHelpNotification(msg)
    BeginTextCommandDisplayHelp("STRING")
    AddTextComponentSubstringPlayerName(msg)
    EndTextCommandDisplayHelp(0, false, true, -1)
end

function invalidItem(src,itemName)
    TriggerClientEvent('ataShop:showNotification', src, 'Invalid item: ' .. itemName)
end
function Purchasesuccessful(src,totalCost)
   TriggerClientEvent('esx:showNotification', src, 'Purchase successful: $' .. totalCost)
end
function enoughmoney(src)
     TriggerClientEvent('esx:showNotification', src, 'Not enough money')
end
function enoughitem(src,itemName)
   TriggerClientEvent('esx:showNotification', src, 'You do not have enough ' .. itemName)
end

function solditem(src,totalEarnings)
     TriggerClientEvent('esx:showNotification', src, 'You sold items for $' .. totalEarnings)
end
```