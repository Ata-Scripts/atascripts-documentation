# Config File

```lua
Config = {}

Config.DefualtGarage = 'pillboxgarage' -- name of the garage

Config.CMD = {
	['open_menu'] = 'coin',
	['set_coin'] = 'setcoin',
	['add_coin'] = 'addcoin',
	['remove_coin'] = 'removecoin',
	['see_coins'] = 'lookupcoin',
}

Config.Permission = {
	['ALL'] = { -- ALL OF THE PERMISSIONS
		'license:f8bc6aa65d475e72c5d619f893d22f384081ab79'
	},
	['SET_COIN'] = { -- SET COIN PERMISSION
		'steam:f8bc6aa65d472f384081ab79'
	},
	['ADD_COIN'] = { -- ADD COIN PERMISSION
		'steam:f8bc6aa65d47579'
	},
	['SEE_COIN'] = { -- SEE COIN PERMISSION
		'steam:f8bc6aa65d47384081ab79'
	},
}


Config.UI = {
	Header1 = "COIN SHOP",
	Header2 = "SYSTEM",
	desc = "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam sequi fugit porro provident cumque. Error tenetur, odio, perferendis quasideleniti doloribus aliquid blanditiis facere consequuntur accusantiumconsequatur rem deserunt impedit. Sequi reiciendis, assumenda.",
}

Config.MenuItems = {
	{
		count = "30000", ---- COUNT OF THE WHEN BUY
		img = "img/arc_reactor.png", ---- ITEM IMAGE
		label = "REACTOR", ---- ITEM LABEL
		price = "20", ---- PRICE of the COIN
		name = "beer", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
		information = "Lorem ipsum dolor sit amet consectetur adipisicing elit. enda.",
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/coca_cola_pop.png", ---- ITEM IMAGE
		label = "COCA DOLL", ---- ITEM LABEL
		price = "50", ---- PRICE of the COIN
		name = "coca_cola_pop", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
		
		information = "Lorem ipsum dolor sit amet consectetur adipisicing elit. enda.",
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/geoffrey_pop.png", ---- ITEM IMAGE
		label = "GEO DOLL", ---- ITEM LABEL
		price = "60", ---- PRICE of the COIN
		name = "geoffrey_pop", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "10", ---- COUNT OF THE WHEN BUY
		img = "img/screwdriverset_blue.png", ---- ITEM IMAGE
		label = "FIX BOX", ---- ITEM LABEL
		price = "10", ---- PRICE of the COIN
		name = "screwdriverset_blue", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/skull.png", ---- ITEM IMAGE
		label = "SKULL KEY", ---- ITEM LABEL
		price = "1000", ---- PRICE of the COIN
		name = "skull", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1000", ---- COUNT OF THE WHEN BUY
		img = "img/money.png", ---- ITEM IMAGE
		label = "CASH", ---- ITEM LABEL
		price = "100", ---- PRICE of the COIN
		name = "cash", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/weaponlicense.png", ---- ITEM IMAGE
		label = "FAKE ID", ---- ITEM LABEL
		price = "90", ---- PRICE of the COIN
		name = "cash", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/weapon_assaultrifle.png", ---- ITEM IMAGE
		label = "ASSAULT", ---- ITEM LABEL
		price = "200", ---- PRICE of the COIN
		name = "weapon_assaultrifle", --- name on the inventory or base
		category = "WEAPONS", ---- category : CARS , ITEMS , WEAPONS
	},

	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/weapon_dbshotgun.png", ---- ITEM IMAGE
		label = "SHOTGUN", ---- ITEM LABEL
		price = "250", ---- PRICE of the COIN
		name = "weapon_dbshotgun", --- name on the inventory or base
		category = "WEAPONS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/weapon_heavysniper.png", ---- ITEM IMAGE
		label = "SHOTGUN", ---- ITEM LABEL
		price = "300", ---- PRICE of the COIN
		name = "weapon_heavysniper", --- name on the inventory or base
		category = "WEAPONS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/meleeToolAxeT1IronFireaxe.png", ---- ITEM IMAGE
		label = "AXE", ---- ITEM LABEL
		price = "350", ---- PRICE of the COIN
		name = "axe", --- name on the inventory or base
		category = "WEAPONS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/parachute_blue.png", ---- ITEM IMAGE
		label = "PARACHUTE", ---- ITEM LABEL
		price = "100", ---- PRICE of the COIN
		name = "parachute_blue", --- name on the inventory or base
		category = "WEAPONS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "https://docs.fivem.net/vehicles/prototipo.webp", ---- ITEM IMAGE
		label = "PROTOTIPO", ---- ITEM LABEL
		price = "500", ---- PRICE of the COIN
		name = "prototipo", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
		vehicle = { type = 'car', properties = { color1 = 0, color2 = 27 } }
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "https://docs.fivem.net/vehicles/massacro2.webp", ---- ITEM IMAGE
		label = "MASSACRO", ---- ITEM LABEL
		price = "500", ---- PRICE of the COIN
		name = "massacro2", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
		vehicle = { type = 'car', properties = { color1 = 0, color2 = 27 } }
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "https://docs.fivem.net/vehicles/zentorno.webp", ---- ITEM IMAGE
		label = "ZENTORNO", ---- ITEM LABEL
		price = "600", ---- PRICE of the COIN
		name = "zentorno", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
		vehicle = { type = 'car', properties = { color1 = 0, color2 = 27 } }
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "https://docs.fivem.net/vehicles/vacca.webp", ---- ITEM IMAGE
		label = "VACCA", ---- ITEM LABEL
		price = "600", ---- PRICE of the COIN
		name = "vacca", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
		vehicle = { type = 'car', properties = { color1 = 0, color2 = 27 } }
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "https://docs.fivem.net/vehicles/entityxf.webp", ---- ITEM IMAGE
		label = "ENTITYXF", ---- ITEM LABEL
		price = "700", ---- PRICE of the COIN
		name = "entityxf", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
		vehicle = { type = 'car', properties = { color1 = 0, color2 = 27 } }
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "https://docs.fivem.net/vehicles/elegy.webp", ---- ITEM IMAGE
		label = "ELEGY", ---- ITEM LABEL
		price = "700", ---- PRICE of the COIN
		name = "elegy", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
		vehicle = { type = 'car', properties = { color1 = 0, color2 = 27 } }
	},
}

Config.coinPackages = {
	{
		count_coin = "200",
		img = "img/Package.png",
		price_coin = "$2.99",
		link = "https://ata.tebex.io",
	},
	{
		count_coin = "500",
		img = "img/Package.png",
		price_coin = "$5.99",
		link = "https://ata.tebex.io",
	},
	{
		count_coin = "1000",
		img = "img/Package.png",
		price_coin = "$8.99",
		link = "https://ata.tebex.io",
	},
	{
		count_coin = "2000",
		img = "img/Package.png",
		price_coin = "$14.99",
		link = "https://ata.tebex.io",
	},
	{
		count_coin = "5000",
		img = "img/Package.png",
		price_coin = "$24.99",
		link = "https://ata.tebex.io",
	},
	{
		count_coin = "50000",
		img = "img/Package.png",
		price_coin = "$44.99",
		link = "https://ata.tebex.io",
	},
}


Config.Locale = {
	["success_buy"] = 'You have successfully bought ',
	['coins'] = 'CP',
	['for_or'] = ' for ',
	['Webhook_buy_weapon_header'] = 'Player Buy Weapon',
	['Webhook_buy_weapon_message'] = 'Player: %s, Weapon: %s, Count: %s, Pay Coin: %s, Now Have Coin: %s',
	['Webhook_buy_vehicle_header'] = 'Player Buy Vehicle',
	['Webhook_buy_vehicle_message'] = 'Player: %s, Vehicle: %s, Count: %s, Pay Coin: %s, Now Have Coin: %s',
	['Webhook_buy_item_header'] = 'Player Buy Item',
	['Webhook_buy_item_message'] = 'Player: %s, Item: %s, Count: %s, Pay Coin: %s, Now Have Coin: %s',
	['Registered_code_header'] = 'Registered Code',
	['Registered_code_message'] = 'Transaction ID : `%s`, Amount: %s',
	['Registered_code_header_error'] = 'Error Registered Code',
	['Registered_code_message_error'] = 'Transaction ID : `%s`, Amount: %s',
	['success_set_coin'] = 'You have successfully set the coin for ',
	['no_permission'] = 'You do not have permission to use this command',
	['invalid_input'] = 'Invalid input',
	['invalid_amount'] = 'Invalid amount',
	['Webhook_admin_command_header'] = 'Admin Command',
	['Webhook_admin_command_message_remove'] = 'Admin: %s, Target: %s, Remove Coin: %s | Now Coins : %s',
	['Webhook_admin_command_message_add'] = 'Admin: %s, Target: %s, Add Coin: %s | Now Coins : %s',
	['Webhook_admin_command_message_set'] = 'Admin: %s, Target: %s, Set Coin: %s | Now Coins : %s',
	['Webhook_admin_command_message_see'] = 'Admin: %s, Target: %s, See Coin: %s',
	

}
```
