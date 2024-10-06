# Config

```lua

Config = {}

Config.newESX = true

Config.MenuCommand = "coin"

Config.setCoinAdmin = "setcoin"

Config.giveCoinAdmin = "givecoin"

Config.GithubVersionCheck = true

Config.GithubName = "ataCoinShop" -----!!!! DONT CHANGE PLEASEEE !!!!

Config.DiscordLog =
	"YOUR WEBHOOK"

Config.AdminGroup = {
	"admin",
	"superadmin",
}

Config.UI = {
	Header1 = "COIN SHOP",
	Header2 = "SYSTEM",
	desc = "Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam sequi fugit porro provident cumque. Error tenetur, odio, perferendis quasideleniti doloribus aliquid blanditiis facere consequuntur accusantiumconsequatur rem deserunt impedit. Sequi reiciendis, assumenda.",
}

Config.MenuItems = {
	{
		count = "2", ---- COUNT OF THE WHEN BUY
		img = "img/arc_reactor.png", ---- ITEM IMAGE
		label = "REACTOR", ---- ITEM LABEL
		price = "20", ---- PRICE of the COIN
		name = "arc_reactor", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/coca_cola_pop.png", ---- ITEM IMAGE
		label = "COCA DOLL", ---- ITEM LABEL
		price = "50", ---- PRICE of the COIN
		name = "coca_cola_pop", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
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
		name = "money", --- name on the inventory or base
		category = "ITEMS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/weaponlicense.png", ---- ITEM IMAGE
		label = "FAKE ID", ---- ITEM LABEL
		price = "90", ---- PRICE of the COIN
		name = "money", --- name on the inventory or base
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
		img = "img/prototipo.png", ---- ITEM IMAGE
		label = "PROTOTIPO", ---- ITEM LABEL
		price = "500", ---- PRICE of the COIN
		name = "prototipo", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/massacro2.png", ---- ITEM IMAGE
		label = "MASSACRO", ---- ITEM LABEL
		price = "500", ---- PRICE of the COIN
		name = "massacro2", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/zentorno.png", ---- ITEM IMAGE
		label = "ZENTORNO", ---- ITEM LABEL
		price = "600", ---- PRICE of the COIN
		name = "axe", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/vacca.png", ---- ITEM IMAGE
		label = "VACCA", ---- ITEM LABEL
		price = "600", ---- PRICE of the COIN
		name = "vacca", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/entityxf.png", ---- ITEM IMAGE
		label = "ENTITYXF", ---- ITEM LABEL
		price = "700", ---- PRICE of the COIN
		name = "entityxf", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
	},
	{
		count = "1", ---- COUNT OF THE WHEN BUY
		img = "img/elegy.png", ---- ITEM IMAGE
		label = "ELEGY", ---- ITEM LABEL
		price = "700", ---- PRICE of the COIN
		name = "elegy", --- name on the inventory or base
		category = "CARS", ---- category : CARS , ITEMS , WEAPONS
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

```
