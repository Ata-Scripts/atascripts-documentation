# Config

```lua
Config = {}

------------------------------------------------------------------------------------

Config.Mysql = "oxmysql"

Config.FrameWork = 'ESXNEW' -- Only supports ESX and ESXNEW

Config.GithubName = 'EntrySystem' ---- !! DO NOT CHANGE THIS

Config.GithubVersionCheck = true ---- !! DO NOT CHANGE THIS

Config.LegalWhiteListWithMenu = false ---- if you want to disable admin white list false value in here and for open question menu open true here

Config.ilLegalWhiteListWithMenu = true ---- if you want to disable admin white list false value in here and for open question menu open true here

Config.dropmessage = " [EINREIS SYSTEM] You did the test wrong, I kicked you for a warning so you understand the seriousness of the situation, you can enter again"

Config.AdminChangeClothes = true -- Only supports esx_skin and skinchanger - also you can config in shared/client.lua

Config.VehicleDrugDeliver = 'guardian'

Config.DeveloperMode = false --- Only Developer Mode

Config.AutoOpenQuestionMenu = true --- Automatic Question Menu Open When Admin is 0 (you can change in Config.MinimumAdminForWaiting for set minimum)

Config.MinimumAdminForWaiting = 1 ---- if 1 admin is online player get waiting for admin else question menu open automaticly


Config.AdminCmd = {
    args = 'eduty',
    legal = 'legal', ----- for duty admin in legal location
    illegal = 'illegal', ----- for duty admin in illegal location
}

Config.AdminAcceptWhiteListCmd = 'accept'
Config.AdminDeclineWhiteListCmd = 'decline'
Config.AdminResetEntry = 'entryreset'

Config.allowed =
{ 
    'superadmin',
    'admin'
}


Config.DrugDeliverLocation = {
        vector3(1946.1857910156,2685.1633300781,42.357814788818),
        vector3(2315.7751464844,2595.7900390625,46.49291229248),
        vector3(1216.5206298828,1845.0688476563,78.736549377441),
        vector3(-104.04707336426,851.25152587891,235.41526794434),
}


Config.AdminCall = {
    title = 'Waiting WhiteList',
    subject = 'My ID : ',
    msg = 'Hello i Waiting For You In '

}

Config.npc = "a_m_y_busicas_01"

Config.admincall = {
    npc = vector3(-1085.6, -2829.6, 26.7087), 
    npcH = 141.95,
    npctitle = "~y~Hello Welcome~w~ How can I help you?",
    npcquestion = "~y~[E]~w~ Call an admin to take care of you",
    npccalled = "~y~Okay, I've called an admin for you, please wait."
}

Config.admincallswindler = {
    npc = vector3(-2165.7, 5197.73, 15.8803), 
    npcH = 106.65,
    npctitle = "~y~Hello Welcome~w~ How can I help you?",
    npcquestion = "~y~[E]~w~ Call an admin to take care of you",
    npccalled = "~y~Okay, I've called an admin for you, please wait."
}

Config.coord = {
    legal = vector3(-1084.8931884766,-2840.3842773438,27.708745956421),
    illegal = vector3(-2168.2, 5192.34, 16.4841),
    legal_finish = vector3(-1035.9, -2735.5, 20.1692), ---- airport
    illegal_finish = vector3(-99.128, -1049.3, 27.4486) --- land
}


Config.EconomyTax = {
    ['low'] = 10000,
    ['medium'] = 100000,
    ['high'] = 500000,    
    ['ultra'] = 1000000,
    ['extreme'] = 2000000,
}

Config.EconomyTaxPercentage = {
    ['low'] = 0.1,
    ['medium'] = 0.5,
    ['high'] = 0.6,    
    ['ultra'] = 0.8,
    ['extreme'] = 1,
}


Config.PlayerTax = true
Config.CarTax = true

Config.EconomyTaxInterval = 120 -- in minutes (2 hrs)

Config.CarTaxRate = 100 -- $100 per car
Config.CarTaxInterval = 180 -- in minutes (3hrs)


Config.PoliceMenuCmd = 'visamenu'


Config.JobAndGrade = {
    ['police'] = 3 ,
    ['sheriff'] = 3 ,
    ['fbi'] = 6
}


Config.lang = {
    no = "You failed the test, I'm kicking you out so you don't repeat it, and you can retest when you come back!",
    yes = "You have successfully completed the test, welcome to our server",
    AdminOffDuty = "Now You Are Off Duty You Can Again On Duty With This Cmd : \n",
    AdminOffDutyHelp = "You Can Off Duty With This Cmd : \n",
    PlayerKicked = "You kicked because cant answer test",
    PlayerResetEntry = "reseted entry infomration",
    CheckVisa = "Check Player Visa",
    NowHaveVisa = "Now Have Visa",
    DontHaveVisa = "Dont Have Visa",
    GiveVisaForYou = "Gived Visa For You , Welcome",
    HaveVisa = "Have Visa",
    GivePlayerVisa = "Give Player Visa",
    PlayerNotFound = "Player not found or is not online!"
}



function GetFrameWork()
    return Config.FrameWork
end



Config.TriggerEvents = {
    CheckPlayer = 'ataEntry:CheckPlayer',
}
```
