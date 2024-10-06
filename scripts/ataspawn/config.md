# Config

```lua
Config = {}

Config.Framework = 'ESX' --standalone, ESX, QBCore
Config.SpawnHome = true
Config.ESX_1_9_0 = true
Config.GetSharedObject = 'esx:getSharedObject'
Config.GithubVersionCheck = true
Config.GithubName = 'ataSpawnESX' -----!!!! DONT CHANGE PLEASEEE !!!!
Config.esx_property = 'esx_property'
Config.Location = {
    {
        name = 'police',
        lock = true,
        LocationName = "Police Department",
        LocationIcon = "fa-solid fa-building-shield",
        color = "rgba(0, 0, 255,0.6)",
        image = "./img/locations/policedep.webp",
        imagePostion = "-13vw -0vw",
        imageSize = "370",
        help = false,
        TextHelp = "When You Get a Room In Motel You Can Spawn Here",
        HelpIcon = "fa-sharp fa-solid fa-question",
        coords = vector3(434.88311767578,-974.64910888672,30.713327407837),
        pedConfig = {
            pedModel = 'a_m_y_smartcaspat_01',
            pedCoords = vector3(434.88311767578,-974.64910888672,30.713327407837),
            Heading = 94.10,
            price = 340,
            pedAnimation = 'WORLD_HUMAN_CLIPBOARD',
        },
    },
    {
        name = 'airport',
        lock = true,
        LocationName = "LS AirPort",
        LocationIcon = "fa-solid fa-plane",
        color = "rgba(255, 105, 41,0.6)",
        image = "./img/locations/airport.jpg",
        imagePostion = "-36vw -0vw",
        imageSize = "370",
        help = false,
        TextHelp = "When You Get a Room In Motel You Can Spawn Here",
        HelpIcon = "fa-sharp fa-solid fa-question",
        coords = vector3(-1033.5421142578,-2739.9377441406,20.169292449951),
        pedConfig = {
            pedModel = 'a_m_y_smartcaspat_01',
            pedCoords = vector3(-1033.5421142578,-2739.9377441406,20.169292449951),
            Heading = 66.90210723877,
            price = 500,
            pedAnimation = 'WORLD_HUMAN_CLIPBOARD',
        },
    },
    {
        name = 'last', ------ this is just ID for backend no show for player WARNING : without space or special symbol esx : home , police , last etc.
        lock = false,----- DONT CHANGE !!!!!!!!!!!!!!!!!
        LocationName = "Last Postion",
        LocationIcon = "fa-sharp fa-solid fa-location-dot",
        color = "rgba(255, 0, 213,1)",
        image = "./img/locations/row.jpg",
        imagePostion = "-30vw 0vw",
        imageSize = "400",
        help = true,
        TextHelp = "You go to the last place you were in the last disconnection",
        HelpIcon = "fa-sharp fa-solid fa-question",
        coords = 'last', ----- DONT CHANGE !!!!!!!!!!!!!!!!!
        pedConfig = {
            pedModel = 'a_m_y_smartcaspat_01',
            pedCoords = vector3(275.41149902344,-598.00994873047,44.132583618164),
            Heading = 20.4,
            price = 200,
            pedAnimation = 'WORLD_HUMAN_CLIPBOARD',
        },
    },
    {
        name = 'benny',
        lock = true,
        LocationName = "Benny's Original",
        LocationIcon = "fa-solid fa-wrench",
        color = "rgba(255, 59, 41,0.6)",
        image = "./img/locations/garage.jpg",
        imagePostion = "-36vw -0vw",
        imageSize = "370",
        help = false,
        TextHelp = "When You Get a Room In Motel You Can Spawn Here",
        HelpIcon = "fa-sharp fa-solid fa-question",
        coords = vector3(-211.1427154541,-1309.4783935547,31.292879104614),
        pedConfig = {
            pedModel = 'a_m_y_smartcaspat_01',
            pedCoords = vector3(-211.1427154541,-1309.4783935547,31.292879104614),
            Heading = 10.332026481628,
            price = 200,
            pedAnimation = 'WORLD_HUMAN_CLIPBOARD',
        },
    },
    {
        name = 'meeting',
        lock = true,
        LocationName = "Legion Square",
        LocationIcon = "fa-solid fa-tree-city",
        color = "rgba(77, 255, 41,0.6)",
        image = "./img/locations/meeting.webp",
        imagePostion = "-20vw -0vw",
        imageSize = "300",
        help = false,
        TextHelp = "When You Get a Room In Motel You Can Spawn Here",
        HelpIcon = "fa-sharp fa-solid fa-question",
        coords = vector3(240.12896728516,-890.31140136719,30.492107391357),
        pedConfig = {
            pedModel = 'a_m_y_smartcaspat_01',
            pedCoords = vector3(240.12896728516,-890.31140136719,30.492107391357),
            Heading = 22.914966583252,
            price = 200,
            pedAnimation = 'WORLD_HUMAN_CLIPBOARD',
        },
    },
    {
        name = 'casino',
        lock = true,
        LocationName = "Diamon Casino",
        LocationIcon = "fa-solid fa-coins",
        color = "rgba(41, 255, 234,0.6)",
        image = "./img/locations/casino.jpg",
        imagePostion = "-25vw -0vw",
        imageSize = "340",
        help = false,
        TextHelp = "When You Get a Room In Motel You Can Spawn Here",
        HelpIcon = "fa-sharp fa-solid fa-question",
        coords = vector3(928.43975830078,56.913944244385,80.898391723633),
        pedConfig = {
            pedModel = 'a_m_y_smartcaspat_01',
            pedCoords = vector3(928.43975830078,56.913944244385,80.898391723633),
            Heading = 57.361667633057,
            price = 800,
            pedAnimation = 'WORLD_HUMAN_CLIPBOARD',
        },
    },
}



Config.jobLocation = {
    {
        job = {'police','a'},
        LocationName = "Police Special",
        LocationIcon = "fa-solid fa-handcuffs",
        coords = vector3(455.34246826172,-990.86242675781,30.68959236145),
    },
}


Config.lang = {
    buySpawn = "Congratulations, you bought this spawn location for ~g~",
    noMoney = "You don't have enough money,for buy this spawn location you need ~g~",
    haveThisLocation = "You already bought this location",
    homeUI = "Home",
    iconhomeUI = "fa-solid fa-house",
    JobUI = "Job Location",
    iconjobUI = "fa-solid fa-user-minus",
    npcDraw = "Press ~INPUT_VEH_FLY_VERTICAL_FLIGHT_MODE~ For Buy This Spawn Location "
}

------------------ NEVER EVER CHANGE -------------------------

Config.JobAndHomedefualt = {

    {
        id = 1, --- dont change
        lock = true, --- dont change
        LocationName = Config.lang.homeUI,
        LocationIcon = Config.lang.iconhomeUI,
    },
    {
        id = 2, --- dont change
        lock = true, --- dont change
        LocationName = Config.lang.JobUI,
        LocationIcon = Config.lang.iconjobUI,
    },

}
```
