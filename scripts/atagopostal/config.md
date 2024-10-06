---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Config

```lua
Config = {}


Config.FrameWork = 'QB' -- Only supports ESX , ESXNEW , QB

Config.Mysql = 'oxmysql'    ----- oxmysql , mysql-async , ghmattimysql

Config.Locale= 'en'

Config.NextLevelXP = 100

---- this is the default value for the next
--  level xp value example for level 2 your need 2 * 100 = 200 XP value 
--  or you can change this example 1000 that means the 
--  next level need xp value X1000 
--  (player level is 3 and need for level 4 need 4000 xp )

Config.MaxLevel = 50

Config.DiscordToken = 'TOKE IN HERE'

Config.GithubVersionCheck = true

Config.GithubName = 'ataPostal' -----!!!! DONT CHANGE PLEASEEE !!!!


Config.StartLocation = {
    pedcoords = vector4(131.44549560547,97.263343811035,82.507606506348, 170.86657714844),
    pedModel = 'a_m_y_business_01',
    ExitJobCoords = vector3(116.11511230469,99.524017333984,80.915573120117),
    markercoord = vector3(131.39198303223,96.56037902832,82.507583618164),
    vehicleSpawn = vector4(63.098510742188,122.37886810303,79.162544250488, 161.6326751709),
    markerConfig = {
        Type = 1,
        rgb = {r = 255, g = 255, b = 0}
    },
    blip = {
        color = 1 ,
        scale = 0.8,
        sprite = 478
    }
}



Config.Uniform = {   ---- just for ESX and ESX_skin
    male = {
        { "tshirt_1", 15 },
        { "tshirt_2", 0 },
        { "torso_1", 348 },
        { "torso_2", 10 },
        { "decals_1", 0 },
        { "decals_2", 0 },
        { "arms", 1 },
        { "pants_1", 10 },
        { "pants_2", 1 },
        { "shoes_1", 10 },
        { "shoes_2", 0 },
        { "helmet_1", 156 },
        { "helmet_2", 2 },
        

    },
    female = {
        { "tshirt_1", 15 },
        { "tshirt_2", 0 },
        { "torso_1", 424 },
        { "torso_2", 0 },
        { "decals_1", 136 },
        { "decals_2", 0 },
        { "arms", 11 },
        { "pants_1", 25 },
        { "pants_2", 2 },
        { "shoes_1", 3 },
        { "shoes_2", 0 },
        { "helmet_1", 176 },
        { "helmet_2", 0 },
    }




}

Config.items = {
    ['1'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116044118544617572/download.jpeg',
        Name = 'PostCard',
        description = 'A postcard is a small, decorative card often featuring a picture on one side and space for a message and address on the other. It is a popular way to send quick greetings or share vacation memories without using an envelope.',
        level = 1,
        MinIncome = 5,
        MaxIncome = 15
    },
    ['2'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116056126568530051/Easy-Graphics-What-is-Media-Mail_-01.jpg',
        Name = 'Media Mail',
        description = 'Media mail is a discounted postal service specifically designed for shipping books, CDs, DVDs, and other media-related items. It is an affordable option commonly used by individuals, libraries, and educational institutions to send educational or informational materials.',
        level = 20,
        MinIncome = 20,
        MaxIncome = 60
    },
    ['3'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116056914523066588/Difference_between_priority_and_express_mail.jpg',
        Name = 'Express Mail',
        description = 'Express mail, also known as overnight delivery, is a premium postal service that guarantees fast and time-sensitive delivery of packages and documents. It is ideal for urgent items that require immediate attention, often used in business settings or for time-critical personal correspondence.',
        level = 40,
        MinIncome = 100,
        MaxIncome = 250
    },
    ['4'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116059210183090266/092cf1e5-a459-43e6-b953-753bf28ce425.png',
        Name = 'Special Delivery',
        description = 'Special delivery is a specialized postal service offering enhanced security, tracking, and guaranteed delivery options. It is commonly used for valuable or important items, providing insurance coverage and requiring recipients to sign upon receipt to ensure secure delivery.',
        level = 45,
        MinIncome = 250,
        MaxIncome = 500
    },
    ['5'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116059226062721134/package-delivery-cybercriminals-at-your-doorstep-630x330.jpg.jpg',
        Name = 'Security Mail',
        description = 'Security mail encompasses measures to protect mail during transit, including tamper-evident envelopes, encrypted content, and specialized handling procedures. It is used for sensitive information, legal documents, financial records, or classified materials to maintain privacy and security.',
        level = 50,
        MinIncome = 600,
        MaxIncome = 1200
    },
}

Config.rutes = {
    ['1'] = {
        Image = "https://cdn.discordapp.com/attachments/1036369699006578718/1116138877292392568/Paleto-Bay-Enhancement-Modded-by-Arnored-from-GTA5-Mods.jpg",
        Name = 'Paleto Bay',
        description = 'A serene coastal town in San Andreas, known for its picturesque beauty and small-town charm.',
        level = 1,
        GiveXP = 0,
        point = {
            vector3(133.8311, 6631.011, 30.25962),
            vector3(-7.950552, 6309.009, 29.80342),
            vector3(-224.9605, 6320.064, 29.91009),
            vector3(-434.848, 6205.193, 28.24349),
            vector3(-699.6656, 5774.075, 15.90699),
            vector3(-772.2294, 5586.121, 32.05996),
            vector3(-431.378, 5967.524, 30.15599)

        }
    },
    ['2'] = {
        Image = "https://cdn.discordapp.com/attachments/1036369699006578718/1116137250930032680/68bebb56008bf2be1bb4717b8986a455.jpg",
        Name = 'Sandy Shores',
        description = 'A rugged desert town in Blaine County, home to eccentric characters and the wild spirit of the American Southwest.',
        level = 25,
        GiveXP = 5,
        point = {
            vector3(1700.766, 3581.769, 34.45777),
            vector3(2006.083, 3807.26, 31.55669),
            vector3(1839.739, 3947.031, 31.81086),
            vector3(1368.466, 3665.495, 32.19973),
            vector3(919.1879, 3593.728, 34.55741),
            vector3(436.069, 3582.669, 32.23856)
        }
    },
    ['3'] = {
        Image = "https://cdn.discordapp.com/attachments/1036369699006578718/1116135270459388055/Los-Santos-in-GTA-5.jpg",
        Name = 'Los Santos',
        description = 'A bustling metropolis on the San Andreas coast, offering diverse neighborhoods and vibrant urban experiences.',
        level = 35,
        GiveXP = 10,
        point = {
            vector3(320.9968, -802.9214, 28.14537),
            vector3(112.7914, -945.4277, 28.5437),
            vector3(-154.065, -1304.493, 30.29988),
            vector3(-335.1481, -1295.322, 30.39911),
            vector3(-952.6998, -1973.333, 12.19157),
            vector3(-267.0996, -785.361, 31.09751),
            vector3(70.23667, -277.146, 46.21249),
            vector3(-787.2025, 63.59901, 50.37799)
        }
    },
    
}

Config.vehicles = {
    ['1'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116138877648896020/6672aa31ce601ff35a86cda4872661dc.jpeg',
        Name = 'Boxville',
        carName = 'boxville2',
        Livery = 0,
        description = 'A reliable delivery truck with a spacious interior, ideal for efficiently delivering packages and parcels.',
        level = 1,
        ExtraXP = 5,
        Speed = 'Low'
    },
    ['2'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116138878093508680/guru.jpg',
        Name = 'Boxville Special',
        carName = 'boxville2',
        description = 'A sturdy and versatile delivery truck with increased cargo capacity for handling bulkier shipments and demanding routes.',
        level = 30,
        Livery = 1,
        ExtraXP = 8,
        Speed = 'Medium'
    },
    ['3'] = {
        Image = 'https://cdn.discordapp.com/attachments/1036369699006578718/1116138878659735664/pony.jpg',
        Name = 'Pony',
        carName = 'pony',
        description = 'A compact and efficient delivery van used by postal services for quick and precise package delivery.',
        level = 1,
        Livery = 1,
        ExtraXP = 10,
        Speed = 'Good'
    },
}

Config.Daily = {
    ['1'] = {
        Image = 'images/li.png',
        Name = 'Sunday Mission',
        day = 'Sunday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(-1015.367, -221.0501, 36.76381),
            vector3(-744.5985, -1502.91, 3.576021),
            vector3(489.484, -3088.315, 4.647512)
        }
    },
    ['2'] = {
        Image = 'images/fib.png',
        Name = 'Monday Mission',
        day = 'Monday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(104.6779, -700.3113, 32.12454),
            vector3(3613.522, 3740.698, 27.69009),
            vector3(-2296.255, 377.3265, 173.4666)
        }
    },
    ['3'] = {
        Image = 'images/fleeca.png',
        Name = 'Tuesday Mission',
        day = 'Tuesday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(151.9157, -1028.886, 28.23668),
            vector3(-1219.582, -318.313, 36.52538),
            vector3(-2973.811, 483.5291, 14.26483),
            vector3(1175.336, 2694.768, 36.92756)
        }
    },
    ['4'] = {
        Image = 'images/ls.png',
        Name = 'Wednesday Mission',
        day = 'Wednesday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(115.0241, 6614.685, 30.84972),
            vector3(-371.7702, -127.2304, 37.69558),
            vector3(1180.488, 2650.984, 36.81407)
        }
    },
    ['5'] = {
        Image = 'images/lspd.png',
        Name = 'Thursday Mission',
        day = 'Thursday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(402.8829, -986.1206, 28.37023),
            vector3(662.4894, -19.70947, 81.94499),
            vector3(1844.403, 3663.026, 33.19319),
            vector3(-425.1758, 6033.427, 30.26968)
        }
    },
    ['6'] = {
        Image = 'images/maze.png',
        Name = 'Friday Mission',
        day = 'Friday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(219.3543, 206.3743, 104.3963),
            vector3(-129.4344, 6443.325, 30.40006)
        }
    },
    ['7'] = {
        Image = 'images/md.png',
        Name = 'Saturday Mission',
        day = 'Saturday', --- Sunday , Monday , Tuesday , Wednesday , Thursday , Friday , Saturday
        description = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        level = 1,
        MinIncome = 200,
        MaxIncome = 300,
        GiveXP = 300,
        vehicleData = {
            carName = 'boxville2',
            Livery = 1
        },
        rutes = {
            vector3(1843.211, 3663.35, 33.10633),
            vector3(260.7616, -1428.517, 28.231),
            vector3(273.1681, -588.9316, 42.16173)
        }
    },
    
}






function helptext(str)
	SetTextComponentFormat("STRING")
	AddTextComponentString(str)
	DisplayHelpTextFromStringLabel(0, 0, 1, -1)
end


ShowNotification = function(str)
    BeginTextCommandThefeedPost("CELL_EMAIL_BCON")
    AddTextComponentSubstringPlayerName(str)
    EndTextCommandThefeedPostTicker(false, false)
end


function GetFrameWork()
    return Config.FrameWork
end
```
