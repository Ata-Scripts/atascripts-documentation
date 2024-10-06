# Config

```````lua

Config = {}

Config.ESX_1_9_0 = true

Config.GetSharedObject = 'esx:getSharedObject' --- share object ESX 

Config.deletevehiclewhenfundinworld = true --[[
  when player spawn a vehicle server has check it
  vehicle on all map if you true this value when found vehicle on map server deleted vehicle
  if you want you can change this value to false just send a notification to player (This Vehicle is still in the city)
]]--


Config.GithubVersionCheck = true

Config.GithubName = 'ataGarageESX' -----!!!! DONT CHANGE PLEASEEE !!!!

Config.pedname = GetHashKey('mp_m_exarmy_01')

Config.SpecialGarage = false   ---- The player can only get vehicle from the garage where parked the vehicle (false to disable this option)

Config.allvehiclegogarage = true  --- when server has restarted all vehicle stored on garage

Config.EnableBlips = true  -- for enable garage blips

Config.priceimpound = 200 -- impound price

Config.paymethod = 'cash' -- impound remove money methid (cash or bank)

Config.UseLegacyFuel = false -- if you are use Legacyfuel true this 

Config.LegacyFuelExport = 'LegacyFuel' -- if you are use Legacyfuel just put resource name default (LegacyFuel) 

Config.ataNotification = false   --- if you used ata notify true this or false for dafualt notfiction (https://forum.cfx.re/t/atanotify-paid-standalone/4806801)

Config.defaultgarageCAR = 'Garage MeetingPoint' -- dafualt garage for CARS

Config.defaultgarageBOAT = 'Garage Boat 1' -- dafualt garage for Boat

Config.defaultgarageAIR = 'Airport Garage 1' -- dafualt garage for Aircraft

Config.DefualtJobName = 'civ'  --- defualt vehicle job (you need config on esx_vehicleshop when player buy a car set table on owned_vehicles in job )

---------------------- BLIP 
 Config.BlipSetting = {
    car = {
        sprite = 357,
        color = 32,
        scale = 0.8
    },
    boat = {
        sprite = 357,
        color = 30,
        scale = 0.8
    },
    aircraft = {
        sprite = 357,
        color = 47,
        scale = 0.8
    },
    jobCar = {
        sprite = 267,
        color = 32,
        scale = 1.2
    },
    jobBoat = {
        sprite = 267,
        color = 30,
        scale = 1.2
    },
    jobAircraft = {
        sprite = 267,
        color = 47,
        scale = 1.2
    },

}

------- Locals 

Locales = {
    ['openGarage'] = 'Press ~INPUT_CONTEXT~ to Open ~b~',
    ['putgarage'] = '~INPUT_CONTEXT~ to Store Vehicle in~b~ ',
    ['cannot_store'] = 'You can not store this Vehicle on here!',
    ['blips_name_car'] = 'Car Garage',
    ['blips_name_boat'] = 'Boat Garage',
    ['blips_name_aircraft'] = 'AirCraft Garage',
    ['job_blips_name_car'] = 'Parking Car',
    ['job_blips_name_boat'] = 'Parking Boat',
    ['job_blips_name_aircraft'] = 'Parking AirCraft',
    ['vehicle_in_city'] = 'This Vehicle is still in the city',
    ['No_Money'] = 'No Enough Money',
    ['no_car'] = 'You do not have car in this garage',
    ['Vehicle_take_out'] = 'Vehicle was successfully take out the parking',
    ['spawn_loction_busy'] = 'There is no space to take out the car',
    ['Vehicle_Loading'] = 'Loading Vehicle...',
    ['puted_garage'] = 'Your Parked Vehicle ',
    ['Car_Not_Found_Model'] = 'Some of your vehicle will be removed from the server',
    ['force_put_not_type_vehicle'] = 'This car is not for this parking lot',
    ['driver_seat'] = 'Must be in Driver Seat to Store Vehicle!',
    ['not_for_you'] = 'This Vehicle Not For You',
    ['This_car_for_job'] = 'This Car Not For You Job and you cant park this vehicle on here',
    ['for_another_job'] = 'this garage for another job and you dont have permission for open',
}



------- Garages 

Config.Garages = {

    ["Garage MeetingPoint"] = {  ------ Garage Name
    fortype = 'car', ------- boat,aircraft
    job = 'police',
    putvehicle = vector3(222.89686584473,-768.55389404297,29.819), ---- Coord for put vehicle to garage
    openGarage = { 
    pedcoords = vector3(213.9903717041,-808.43347167969,31.014892578125) ,
    handling = 164.32424926758 ,
    } ,  ------- Coord for open garage
    vehicle = {spawn = vector3(232.7941, -805.47, 29.94101),heading = 68.64 } ---- vehicle postion on NUI
    }, 

    ["Garage Ammunation"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(132.52978515625,-1058.3092041016,29.192367553711), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(101.25100708008,-1073.5465087891,29.374118804932) ,
        handling = 70.31566619873 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(122.47484588623,-1066.2039794922,29.192367553711),heading = 92.331748962402 } ---- vehicle postion on NUI
    },

    ["Garage Lake Vinewood"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(204.70176696777,1231.7833251953,225.46000671387), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(189.10824584961,1240.0161132813,225.5948638916) ,
        handling = 292.2243347168 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(184.53756713867,1201.2281494141,225.59535217285),heading = 25.013040542603 } ---- vehicle postion on NUI
    },

    ["Garage Towing Yard"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(380.31115722656,-1628.1184082031,28.896547317505), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(371.53823852539,-1612.5786132813,29.291933059692) ,
        handling = 334.6123046875 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(372.38265991211,-1622.7026367188,29.29195022583),heading = 316.74816894531 } ---- vehicle postion on NUI
    },  

    ["Garage Sandy Shores"] =  {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(2394.0927734375,3112.1306152344,48.13090133667), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(2396.294921875, 3122.7512207031, 48.153861999512) ,
        handling = 159.77008056641 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(2418.3581542969, 3076.1823730469, 49.646366119385), heading = 7.1623997688293 } ---- vehicle postion on NUI
    },

    ["Garage Airport"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-898.11419677734,-2329.4318847656,6.7090339660645), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-905.70788574219, -2338.2431640625, 6.7094860076904) ,
        handling = 331.28952026367 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-942.62329101563, -2321.0380859375, 6.709089756012), heading = 244.78674316406 } ---- vehicle postion on NUI
    }, 

    ["Garage Diamond Casino"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(965.33453369141,-8.3803033828735,80.704391479492), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(978.02935791016, 12.26170539856, 81.040977478027) ,
        handling =  147.9542388916 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(1001.4100341797, 6.4374265670776, 81.862548828125), heading = 150.52450561523 } ---- vehicle postion on NUI
    },

    ["Garage Lifeinvader"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-1480.9979248047,-505.73709106445,32.806880950928), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-1477.9783935547, -519.24041748047, 34.73673248291) ,
        handling =  32.55126953125 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-1521.4340820313, -555.63677978516, 33.238788604736), heading = 304.54635620117} ---- vehicle postion on NUI
    },

    ["Garage University"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-1704.0686035156, 57.58362197876, 65.500610351563), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-1709.1881103516, 75.202728271484, 65.799949645996),
        handling = 219.90576171875
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-1680.2362060547, 62.420425415039, 63.996715545654), heading = 43.933570861816} ---- vehicle postion on NUI
    },  

    ["Garage Arena"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-87.749320983887, -2018.1204833984, 18.016967773438), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-73.37230682373, -2004.9880371094, 18.275281906128),
        handling = 349.07455444336
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-113.1358795166, -2042.6868896484, 17.732028961182), heading = 9.1761684417725} ---- vehicle postion on NUI
    },



    ["Garage Sawmill"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-769.22357177734, 5592.2841796875, 33.48571395874), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-773.18859863281, 5597.9067382813, 33.605308532715),
        handling = 175.76968383789
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-756.01470947266, 5541.35546875, 33.48571395874), heading = 105.471534729} ---- vehicle postion on NUI
    },   
 

    ["Garage Paleto Bay"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(120.78108978271, 6616.0458984375, 31.846189498901), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(112.19958496094, 6619.80078125, 31.814376831055),
        handling = 224.00424194336
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(143.25419616699, 6642.1948242188, 31.55711555481), heading = 133.67115783691} ---- vehicle postion on NUI
    },   

    ["Garage Strand"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-2022.4906005859, -464.76733398438, 11.506952285767), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-2029.9643554688, -465.89868164063, 11.603978157043),
        handling = 52.891563415527
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-2047.7723388672, -476.57836914063, 11.6463098526), heading = 227.36676025391} ---- vehicle postion on NUI
    },   


    ["Garage Boat 1"] = {
        fortype = 'boat', ------- car,aircraft
        job = '',
        putvehicle = vector3(-778.423828125, -1431.4781494141, -0.47479113936424), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-778.30059814453, -1436.4464111328, 1.5952203273773),
        handling = 235.92755126953
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-812.08612060547, -1437.1982421875, 1.47431707382202), heading = 129.31367492676} ---- vehicle postion on NUI
    },   


    ["Airport Garage 1"] = {
        fortype = 'aircraft', ------- car,boat
        job = '',
        putvehicle = vector3(-1648.7729492188, -3136.9482421875, 13.992227554321), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-1685.0911865234, -3150.2141113281, 13.99084854126),
        handling = 237.11123657227
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-1576.2501220703, -3004.9892578125, 13.944757461548), heading = 60.391708374023} ---- vehicle postion on NUI
    },  
    
}

----- Parking Postion for spawn vehicle

Config.ParkingSpots = {

    ["Garage MeetingPoint"] = {
        { coords = vector3(231.3424, -778.7856, 30.44159), heading = 246.25 },
        { coords = vector3(220.8888, -806.535, 30.41988), heading = 247.6 },
        { coords = vector3(230.5119, -810.1128, 30.18728), heading = 66.84 },
        { coords = vector3(222.6113, -801.5812, 30.40527), heading = 247.6 },
        { coords = vector3(233.3575, -805.4659, 30.17599), heading = 67.52 },
        { coords = vector3(225.304, -796.8502, 30.39073), heading = 248.64 },
        { coords = vector3(234.9362, -800.3376, 30.20797), heading = 70.67 },
        { coords = vector3(226.4475, -791.4465, 30.4132), heading = 251.02 },
        { coords = vector3(237.0649, -795.1746, 30.23324), heading = 69.83 },
        { coords = vector3(228.0065, -786.3903, 30.43746), heading = 249.89 },
        { coords = vector3(239.0561, -790.4228, 30.25794), heading = 67.72 },
        { coords = vector3(230.3553, -781.5231, 30.43418), heading = 248.91 },
        { coords = vector3(242.7698, -780.0054, 30.35404), heading = 70.66 },
        { coords = vector3(232.0546, -776.3297, 30.46051), heading = 248.42 },
        { coords = vector3(244.251, -775.119, 30.41724), heading = 67.21 },
        { coords = vector3(218.4489, -768.4896, 30.56911), heading = 248.43 },
        { coords = vector3(227.4739, -771.9465, 30.51531), heading = 66.66 },
        { coords = vector3(215.7119, -773.3503, 30.59915), heading = 251.82 },
        { coords = vector3(224.1316, -781.9398, 30.49026), heading = 67.77 },
        { coords = vector3(212.5763, -783.4927, 30.62998), heading = 250.96 },
        { coords = vector3(221.9631, -786.8163, 30.5016), heading = 67.69 },
        { coords = vector3(210.6994, -788.7374, 30.65435), heading = 248.31 },
        { coords = vector3(220.0236, -791.6862, 30.49321), heading = 70.24 },
        { coords = vector3(208.9232, -793.5826, 30.68486), heading = 250.44 },
        { coords = vector3(218.3866, -796.7542, 30.50086), heading = 70.28 },
        { coords = vector3(264.8602, -759.6733, 34.37768), heading = 68.03 },
        { coords = vector3(251.3972, -760.5433, 34.3763), heading = 340.99 },
        { coords = vector3(241.8033, -755.6668, 34.37081), heading = 342.41 },
        { coords = vector3(253.1028, -746.4533, 34.37242), heading = 161.82 },
        { coords = vector3(246.5718, -743.6817, 34.36513), heading = 162.23 },
        { coords = vector3(240.0531, -741.3574, 34.34895), heading = 162.87 },
        { coords = vector3(225.1537, -751.7924, 34.36911), heading = 340.86 },
        },


        ["Garage Ammunation"] = {
            { coords = vector3(117.2824, -1081.693, 28.67972), heading = 1.91 },
            { coords = vector3(121.2401, -1081.427, 28.67954),  heading = 359.21 },
            { coords = vector3(125.0198, -1080.944, 28.67923), heading = 358.8 },
            { coords = vector3(128.4002, -1080.588, 28.68507), heading = 3.76 },
            { coords = vector3(132.4021, -1080.99, 28.68003), heading = 3.56},
            { coords = vector3(135.8009, -1080.835, 28.68082), heading = 1.8 },
            { coords = vector3(139.382, -1081.091, 28.67981), heading = 359.33 },
            { coords = vector3(143.4466, -1080.838, 28.67924), heading = 359.68 },
        },

        ["Garage Lake Vinewood"] = {
            { coords = vector3(209.0826, 1237.935, 224.9463), heading =103.19 },
            { coords = vector3(208.1008, 1241.53, 224.9463),  heading = 102.33 },
            { coords = vector3(209.7728, 1234.545, 224.9461), heading = 101.86 },
            { coords = vector3(210.3904, 1231.424, 224.9469), heading = 101.61 },
            { coords = vector3(211.402, 1228.216, 224.9462), heading = 102.12},
        },
        ["Garage Abschlepphof"] = {
            { coords = vector3(420.1821, -1635.958, 28.77895), heading = 89.98 },
            { coords = vector3(419.9895, -1638.851, 28.77918), heading = 88.73 },
            { coords = vector3(419.973, -1641.943, 28.77791), heading = 89.2},
        },
        ["Garage Sandy Shores"] = {
            { coords = vector3(2427.97, 3131.909, 47.73763), heading = 84.99 },
            { coords = vector3(2428.147, 3129.082, 47.74551), heading = 91.21 },
            { coords = vector3(2428.259, 3125.273, 47.74416), heading = 53.54},
        },

        ["Garage Airport"] = {
            { coords = vector3(-894.2426, -2332.148, 6.194956), heading = 58.55 },
            { coords = vector3(-897.4691, -2337.982, 6.195388), heading = 61.31 },
            { coords = vector3(-905.8764, -2333.281, 6.19511), heading = 238.09},
            { coords = vector3(-901.0616, -2323.87, 6.195228), heading = 240.47},
            { coords = vector3(-897.5806, -2318.291, 6.195082), heading = 239.45},
        },

        ["Garage Diamond Casino"] = {
            { coords = vector3(940.3263, -33.29683, 78.3399), heading = 147.29 },
            { coords = vector3(937.6256, -30.9432, 78.33926), heading = 148.06 },
            { coords = vector3(934.3148, -29.5231, 78.3399), heading = 149.04},
            { coords = vector3(931.641, -27.50686, 78.3398), heading = 147.55},
        }, 

        ["Garage Lifeinvader"] = {
            { coords = vector3(-1474.919, -492.9715, 32.29266), heading = 216.75 },
            { coords = vector3(-1479.994, -496.0269, 32.29388), heading = 211.64},
            { coords = vector3(-1471.842, -508.1354, 32.29374), heading = 34.62},
        },

        ["Garage University"] = {
            { coords = vector3(-1706.622, 52.34721, 65.32575), heading = 290.24 },
            { coords =vector3(-1699.539, 62.07898, 64.56644), heading = 163.25},
            { coords = vector3(-1699.639, 44.63554, 64.76392), heading = 292.77},
            { coords = vector3(-1682.668, 47.14423, 63.33105), heading = 162.29},
        },
        
        ["Garage Arena"] = {
            { coords = vector3(-73.36166, -2011.271, 17.66566), heading = 200.33 },
            { coords = vector3(-70.20872, -2010.242, 17.66543), heading = 200.01},
            { coords = vector3(-67.27823, -2009.095, 17.66498), heading = 200.43},
            { coords = vector3(-64.11967, -2007.895, 17.66542), heading = 200.74},
        },

        ["Garage Fort Zancudo"] = {
            { coords = vector3(-2318.024, 3359.394, 32.33652), heading = 150.6 },
            { coords = vector3(-2328.225, 3364.968, 32.31561), heading = 153.32},
            { coords = vector3(-2338.471, 3368.845, 32.31243), heading = 152.53},
            { coords = vector3(-2347.382, 3375.894, 32.3191), heading = 150.33},
            { coords = vector3(-2355.875, 3379.408, 32.31982), heading = 148.05},
        },

        ["Garage Sawmill"] = {
            { coords = vector3(-763.1837, 5547.319, 32.97276), heading = 179.23 },
            { coords = vector3(-759.2617, 5548.167, 32.97184), heading = 177.83},
            { coords = vector3(-755.5919, 5548.017, 32.97201), heading = 179.96},
            { coords = vector3(-752.2121, 5548.506, 32.9741), heading = 176.16},
            { coords = vector3(-746.7042, 5535.05, 32.97205), heading = 32.6},
        },

        ["Garage Paleto Bay"] = {
            { coords = vector3(118.6931, 6599.357, 31.66381), heading = 271.37},
            { coords = vector3(124.2623, 6594.765, 31.62819), heading = 267.79},
            { coords = vector3(128.5387, 6590.112, 31.58277), heading = 269.37},
            { coords = vector3(133.8651, 6585.312, 31.60717), heading = 268.71},
        },

        ["Garage Strand"] = {
            { coords = vector3(-2033.201, -480.0014, 11.18028), heading = 320.42},
            { coords = vector3(-2030.866, -481.6261, 11.1763), heading = 319.55},
            { coords = vector3(-2028.944, -483.6024, 11.19185), heading = 320.03},
            { coords = vector3(-2023.907, -471.9026, 10.8962), heading = 139.16},
            { coords = vector3(-2021.958, -473.7846, 10.89293), heading = 138.63},
        },

        ["Devis Abschlepphof"] = {
            { coords = vector3(394.48, -1625.619, 28.77805), heading = 51.32},
            { coords = vector3(396.8207, -1623.42, 28.77847), heading = 49.24},
            { coords = vector3(400.7062, -1618.789, 28.7784), heading = 50.7},
            { coords = vector3(385.1242, -1634.277, 28.77862), heading = 137.91},
            { coords = vector3(387.48, -1636.322, 28.77965), heading = 142.26},
        },
        
        ["Garage Towing Yard"] = {
            { coords = vector3(402.84921264648, -1616.4978027344, 29.291940689087), heading = 231.88035583496},
            { coords = vector3(401.21780395508, -1619.2060546875, 29.291940689087), heading = 238.05874633789},
            { coords = vector3(388.59014892578, -1612.5645751953, 29.291940689087), heading = 49.598037719727},
            { coords = vector3(390.59307861328, -1610.2729492188, 29.291940689087), heading = 50.550159454346},
            { coords = vector3(392.41836547852, -1608.1228027344, 29.291940689087), heading = 52.912658691406},
        },
        ["Garage Boat 1"] = {
            { coords = vector3(-797.06298828125,-1413.0871582031,0.35248219966888), heading = 50.45},
            { coords = vector3(-791.98718261719,-1405.9442138672,0.36012238264084), heading = 50.45},
            { coords = vector3(-786.43493652344,-1399.5565185547,0.3554439842701), heading = 50.45},
        },
        ["Airport Garage 1"] = {
            { coords = vector3(-1664.9295654297,-3145.6000976563,13.991494178772), heading = 328.48},
        },
}
``````lua
Config = {}

Config.ESX_1_9_0 = true

Config.GetSharedObject = 'esx:getSharedObject' --- share object ESX 

Config.deletevehiclewhenfundinworld = true --[[
  when player spawn a vehicle server has check it
  vehicle on all map if you true this value when found vehicle on map server deleted vehicle
  if you want you can change this value to false just send a notification to player (This Vehicle is still in the city)
]]--


Config.GithubVersionCheck = true

Config.GithubName = 'ataGarageESX' -----!!!! DONT CHANGE PLEASEEE !!!!

Config.pedname = GetHashKey('mp_m_exarmy_01')

Config.SpecialGarage = false   ---- The player can only get vehicle from the garage where parked the vehicle (false to disable this option)

Config.allvehiclegogarage = true  --- when server has restarted all vehicle stored on garage

Config.EnableBlips = true  -- for enable garage blips

Config.priceimpound = 200 -- impound price

Config.paymethod = 'cash' -- impound remove money methid (cash or bank)

Config.UseLegacyFuel = false -- if you are use Legacyfuel true this 

Config.LegacyFuelExport = 'LegacyFuel' -- if you are use Legacyfuel just put resource name default (LegacyFuel) 

Config.ataNotification = false   --- if you used ata notify true this or false for dafualt notfiction (https://forum.cfx.re/t/atanotify-paid-standalone/4806801)

Config.defaultgarageCAR = 'Garage MeetingPoint' -- dafualt garage for CARS

Config.defaultgarageBOAT = 'Garage Boat 1' -- dafualt garage for Boat

Config.defaultgarageAIR = 'Airport Garage 1' -- dafualt garage for Aircraft

Config.DefualtJobName = 'civ'  --- defualt vehicle job (you need config on esx_vehicleshop when player buy a car set table on owned_vehicles in job )

---------------------- BLIP 
 Config.BlipSetting = {
    car = {
        sprite = 357,
        color = 32,
        scale = 0.8
    },
    boat = {
        sprite = 357,
        color = 30,
        scale = 0.8
    },
    aircraft = {
        sprite = 357,
        color = 47,
        scale = 0.8
    },
    jobCar = {
        sprite = 267,
        color = 32,
        scale = 1.2
    },
    jobBoat = {
        sprite = 267,
        color = 30,
        scale = 1.2
    },
    jobAircraft = {
        sprite = 267,
        color = 47,
        scale = 1.2
    },

}

------- Locals 

Locales = {
    ['openGarage'] = 'Press ~INPUT_CONTEXT~ to Open ~b~',
    ['putgarage'] = '~INPUT_CONTEXT~ to Store Vehicle in~b~ ',
    ['cannot_store'] = 'You can not store this Vehicle on here!',
    ['blips_name_car'] = 'Car Garage',
    ['blips_name_boat'] = 'Boat Garage',
    ['blips_name_aircraft'] = 'AirCraft Garage',
    ['job_blips_name_car'] = 'Parking Car',
    ['job_blips_name_boat'] = 'Parking Boat',
    ['job_blips_name_aircraft'] = 'Parking AirCraft',
    ['vehicle_in_city'] = 'This Vehicle is still in the city',
    ['No_Money'] = 'No Enough Money',
    ['no_car'] = 'You do not have car in this garage',
    ['Vehicle_take_out'] = 'Vehicle was successfully take out the parking',
    ['spawn_loction_busy'] = 'There is no space to take out the car',
    ['Vehicle_Loading'] = 'Loading Vehicle...',
    ['puted_garage'] = 'Your Parked Vehicle ',
    ['Car_Not_Found_Model'] = 'Some of your vehicle will be removed from the server',
    ['force_put_not_type_vehicle'] = 'This car is not for this parking lot',
    ['driver_seat'] = 'Must be in Driver Seat to Store Vehicle!',
    ['not_for_you'] = 'This Vehicle Not For You',
    ['This_car_for_job'] = 'This Car Not For You Job and you cant park this vehicle on here',
    ['for_another_job'] = 'this garage for another job and you dont have permission for open',
}



------- Garages 

Config.Garages = {

    ["Garage MeetingPoint"] = {  ------ Garage Name
    fortype = 'car', ------- boat,aircraft
    job = 'police',
    putvehicle = vector3(222.89686584473,-768.55389404297,29.819), ---- Coord for put vehicle to garage
    openGarage = { 
    pedcoords = vector3(213.9903717041,-808.43347167969,31.014892578125) ,
    handling = 164.32424926758 ,
    } ,  ------- Coord for open garage
    vehicle = {spawn = vector3(232.7941, -805.47, 29.94101),heading = 68.64 } ---- vehicle postion on NUI
    }, 

    ["Garage Ammunation"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(132.52978515625,-1058.3092041016,29.192367553711), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(101.25100708008,-1073.5465087891,29.374118804932) ,
        handling = 70.31566619873 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(122.47484588623,-1066.2039794922,29.192367553711),heading = 92.331748962402 } ---- vehicle postion on NUI
    },

    ["Garage Lake Vinewood"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(204.70176696777,1231.7833251953,225.46000671387), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(189.10824584961,1240.0161132813,225.5948638916) ,
        handling = 292.2243347168 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(184.53756713867,1201.2281494141,225.59535217285),heading = 25.013040542603 } ---- vehicle postion on NUI
    },

    ["Garage Towing Yard"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(380.31115722656,-1628.1184082031,28.896547317505), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(371.53823852539,-1612.5786132813,29.291933059692) ,
        handling = 334.6123046875 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(372.38265991211,-1622.7026367188,29.29195022583),heading = 316.74816894531 } ---- vehicle postion on NUI
    },  

    ["Garage Sandy Shores"] =  {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(2394.0927734375,3112.1306152344,48.13090133667), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(2396.294921875, 3122.7512207031, 48.153861999512) ,
        handling = 159.77008056641 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(2418.3581542969, 3076.1823730469, 49.646366119385), heading = 7.1623997688293 } ---- vehicle postion on NUI
    },

    ["Garage Airport"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-898.11419677734,-2329.4318847656,6.7090339660645), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-905.70788574219, -2338.2431640625, 6.7094860076904) ,
        handling = 331.28952026367 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-942.62329101563, -2321.0380859375, 6.709089756012), heading = 244.78674316406 } ---- vehicle postion on NUI
    }, 

    ["Garage Diamond Casino"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(965.33453369141,-8.3803033828735,80.704391479492), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(978.02935791016, 12.26170539856, 81.040977478027) ,
        handling =  147.9542388916 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(1001.4100341797, 6.4374265670776, 81.862548828125), heading = 150.52450561523 } ---- vehicle postion on NUI
    },

    ["Garage Lifeinvader"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-1480.9979248047,-505.73709106445,32.806880950928), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-1477.9783935547, -519.24041748047, 34.73673248291) ,
        handling =  32.55126953125 ,
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-1521.4340820313, -555.63677978516, 33.238788604736), heading = 304.54635620117} ---- vehicle postion on NUI
    },

    ["Garage University"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-1704.0686035156, 57.58362197876, 65.500610351563), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-1709.1881103516, 75.202728271484, 65.799949645996),
        handling = 219.90576171875
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-1680.2362060547, 62.420425415039, 63.996715545654), heading = 43.933570861816} ---- vehicle postion on NUI
    },  

    ["Garage Arena"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-87.749320983887, -2018.1204833984, 18.016967773438), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-73.37230682373, -2004.9880371094, 18.275281906128),
        handling = 349.07455444336
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-113.1358795166, -2042.6868896484, 17.732028961182), heading = 9.1761684417725} ---- vehicle postion on NUI
    },



    ["Garage Sawmill"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-769.22357177734, 5592.2841796875, 33.48571395874), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-773.18859863281, 5597.9067382813, 33.605308532715),
        handling = 175.76968383789
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-756.01470947266, 5541.35546875, 33.48571395874), heading = 105.471534729} ---- vehicle postion on NUI
    },   
 

    ["Garage Paleto Bay"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(120.78108978271, 6616.0458984375, 31.846189498901), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(112.19958496094, 6619.80078125, 31.814376831055),
        handling = 224.00424194336
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(143.25419616699, 6642.1948242188, 31.55711555481), heading = 133.67115783691} ---- vehicle postion on NUI
    },   

    ["Garage Strand"] = {
        fortype = 'car', ------- boat,aircraft
        job = '',
        putvehicle = vector3(-2022.4906005859, -464.76733398438, 11.506952285767), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-2029.9643554688, -465.89868164063, 11.603978157043),
        handling = 52.891563415527
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-2047.7723388672, -476.57836914063, 11.6463098526), heading = 227.36676025391} ---- vehicle postion on NUI
    },   


    ["Garage Boat 1"] = {
        fortype = 'boat', ------- car,aircraft
        job = '',
        putvehicle = vector3(-778.423828125, -1431.4781494141, -0.47479113936424), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-778.30059814453, -1436.4464111328, 1.5952203273773),
        handling = 235.92755126953
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-812.08612060547, -1437.1982421875, 1.47431707382202), heading = 129.31367492676} ---- vehicle postion on NUI
    },   


    ["Airport Garage 1"] = {
        fortype = 'aircraft', ------- car,boat
        job = '',
        putvehicle = vector3(-1648.7729492188, -3136.9482421875, 13.992227554321), ---- Coord for put vehicle to garage
        openGarage = { 
        pedcoords = vector3(-1685.0911865234, -3150.2141113281, 13.99084854126),
        handling = 237.11123657227
        } ,  ------- Coord for open garage
        vehicle = {spawn = vector3(-1576.2501220703, -3004.9892578125, 13.944757461548), heading = 60.391708374023} ---- vehicle postion on NUI
    },  
    
}

----- Parking Postion for spawn vehicle

Config.ParkingSpots = {

    ["Garage MeetingPoint"] = {
        { coords = vector3(231.3424, -778.7856, 30.44159), heading = 246.25 },
        { coords = vector3(220.8888, -806.535, 30.41988), heading = 247.6 },
        { coords = vector3(230.5119, -810.1128, 30.18728), heading = 66.84 },
        { coords = vector3(222.6113, -801.5812, 30.40527), heading = 247.6 },
        { coords = vector3(233.3575, -805.4659, 30.17599), heading = 67.52 },
        { coords = vector3(225.304, -796.8502, 30.39073), heading = 248.64 },
        { coords = vector3(234.9362, -800.3376, 30.20797), heading = 70.67 },
        { coords = vector3(226.4475, -791.4465, 30.4132), heading = 251.02 },
        { coords = vector3(237.0649, -795.1746, 30.23324), heading = 69.83 },
        { coords = vector3(228.0065, -786.3903, 30.43746), heading = 249.89 },
        { coords = vector3(239.0561, -790.4228, 30.25794), heading = 67.72 },
        { coords = vector3(230.3553, -781.5231, 30.43418), heading = 248.91 },
        { coords = vector3(242.7698, -780.0054, 30.35404), heading = 70.66 },
        { coords = vector3(232.0546, -776.3297, 30.46051), heading = 248.42 },
        { coords = vector3(244.251, -775.119, 30.41724), heading = 67.21 },
        { coords = vector3(218.4489, -768.4896, 30.56911), heading = 248.43 },
        { coords = vector3(227.4739, -771.9465, 30.51531), heading = 66.66 },
        { coords = vector3(215.7119, -773.3503, 30.59915), heading = 251.82 },
        { coords = vector3(224.1316, -781.9398, 30.49026), heading = 67.77 },
        { coords = vector3(212.5763, -783.4927, 30.62998), heading = 250.96 },
        { coords = vector3(221.9631, -786.8163, 30.5016), heading = 67.69 },
        { coords = vector3(210.6994, -788.7374, 30.65435), heading = 248.31 },
        { coords = vector3(220.0236, -791.6862, 30.49321), heading = 70.24 },
        { coords = vector3(208.9232, -793.5826, 30.68486), heading = 250.44 },
        { coords = vector3(218.3866, -796.7542, 30.50086), heading = 70.28 },
        { coords = vector3(264.8602, -759.6733, 34.37768), heading = 68.03 },
        { coords = vector3(251.3972, -760.5433, 34.3763), heading = 340.99 },
        { coords = vector3(241.8033, -755.6668, 34.37081), heading = 342.41 },
        { coords = vector3(253.1028, -746.4533, 34.37242), heading = 161.82 },
        { coords = vector3(246.5718, -743.6817, 34.36513), heading = 162.23 },
        { coords = vector3(240.0531, -741.3574, 34.34895), heading = 162.87 },
        { coords = vector3(225.1537, -751.7924, 34.36911), heading = 340.86 },
        },


        ["Garage Ammunation"] = {
            { coords = vector3(117.2824, -1081.693, 28.67972), heading = 1.91 },
            { coords = vector3(121.2401, -1081.427, 28.67954),  heading = 359.21 },
            { coords = vector3(125.0198, -1080.944, 28.67923), heading = 358.8 },
            { coords = vector3(128.4002, -1080.588, 28.68507), heading = 3.76 },
            { coords = vector3(132.4021, -1080.99, 28.68003), heading = 3.56},
            { coords = vector3(135.8009, -1080.835, 28.68082), heading = 1.8 },
            { coords = vector3(139.382, -1081.091, 28.67981), heading = 359.33 },
            { coords = vector3(143.4466, -1080.838, 28.67924), heading = 359.68 },
        },

        ["Garage Lake Vinewood"] = {
            { coords = vector3(209.0826, 1237.935, 224.9463), heading =103.19 },
            { coords = vector3(208.1008, 1241.53, 224.9463),  heading = 102.33 },
            { coords = vector3(209.7728, 1234.545, 224.9461), heading = 101.86 },
            { coords = vector3(210.3904, 1231.424, 224.9469), heading = 101.61 },
            { coords = vector3(211.402, 1228.216, 224.9462), heading = 102.12},
        },
        ["Garage Abschlepphof"] = {
            { coords = vector3(420.1821, -1635.958, 28.77895), heading = 89.98 },
            { coords = vector3(419.9895, -1638.851, 28.77918), heading = 88.73 },
            { coords = vector3(419.973, -1641.943, 28.77791), heading = 89.2},
        },
        ["Garage Sandy Shores"] = {
            { coords = vector3(2427.97, 3131.909, 47.73763), heading = 84.99 },
            { coords = vector3(2428.147, 3129.082, 47.74551), heading = 91.21 },
            { coords = vector3(2428.259, 3125.273, 47.74416), heading = 53.54},
        },

        ["Garage Airport"] = {
            { coords = vector3(-894.2426, -2332.148, 6.194956), heading = 58.55 },
            { coords = vector3(-897.4691, -2337.982, 6.195388), heading = 61.31 },
            { coords = vector3(-905.8764, -2333.281, 6.19511), heading = 238.09},
            { coords = vector3(-901.0616, -2323.87, 6.195228), heading = 240.47},
            { coords = vector3(-897.5806, -2318.291, 6.195082), heading = 239.45},
        },

        ["Garage Diamond Casino"] = {
            { coords = vector3(940.3263, -33.29683, 78.3399), heading = 147.29 },
            { coords = vector3(937.6256, -30.9432, 78.33926), heading = 148.06 },
            { coords = vector3(934.3148, -29.5231, 78.3399), heading = 149.04},
            { coords = vector3(931.641, -27.50686, 78.3398), heading = 147.55},
        }, 

        ["Garage Lifeinvader"] = {
            { coords = vector3(-1474.919, -492.9715, 32.29266), heading = 216.75 },
            { coords = vector3(-1479.994, -496.0269, 32.29388), heading = 211.64},
            { coords = vector3(-1471.842, -508.1354, 32.29374), heading = 34.62},
        },

        ["Garage University"] = {
            { coords = vector3(-1706.622, 52.34721, 65.32575), heading = 290.24 },
            { coords =vector3(-1699.539, 62.07898, 64.56644), heading = 163.25},
            { coords = vector3(-1699.639, 44.63554, 64.76392), heading = 292.77},
            { coords = vector3(-1682.668, 47.14423, 63.33105), heading = 162.29},
        },
        
        ["Garage Arena"] = {
            { coords = vector3(-73.36166, -2011.271, 17.66566), heading = 200.33 },
            { coords = vector3(-70.20872, -2010.242, 17.66543), heading = 200.01},
            { coords = vector3(-67.27823, -2009.095, 17.66498), heading = 200.43},
            { coords = vector3(-64.11967, -2007.895, 17.66542), heading = 200.74},
        },

        ["Garage Fort Zancudo"] = {
            { coords = vector3(-2318.024, 3359.394, 32.33652), heading = 150.6 },
            { coords = vector3(-2328.225, 3364.968, 32.31561), heading = 153.32},
            { coords = vector3(-2338.471, 3368.845, 32.31243), heading = 152.53},
            { coords = vector3(-2347.382, 3375.894, 32.3191), heading = 150.33},
            { coords = vector3(-2355.875, 3379.408, 32.31982), heading = 148.05},
        },

        ["Garage Sawmill"] = {
            { coords = vector3(-763.1837, 5547.319, 32.97276), heading = 179.23 },
            { coords = vector3(-759.2617, 5548.167, 32.97184), heading = 177.83},
            { coords = vector3(-755.5919, 5548.017, 32.97201), heading = 179.96},
            { coords = vector3(-752.2121, 5548.506, 32.9741), heading = 176.16},
            { coords = vector3(-746.7042, 5535.05, 32.97205), heading = 32.6},
        },

        ["Garage Paleto Bay"] = {
            { coords = vector3(118.6931, 6599.357, 31.66381), heading = 271.37},
            { coords = vector3(124.2623, 6594.765, 31.62819), heading = 267.79},
            { coords = vector3(128.5387, 6590.112, 31.58277), heading = 269.37},
            { coords = vector3(133.8651, 6585.312, 31.60717), heading = 268.71},
        },

        ["Garage Strand"] = {
            { coords = vector3(-2033.201, -480.0014, 11.18028), heading = 320.42},
            { coords = vector3(-2030.866, -481.6261, 11.1763), heading = 319.55},
            { coords = vector3(-2028.944, -483.6024, 11.19185), heading = 320.03},
            { coords = vector3(-2023.907, -471.9026, 10.8962), heading = 139.16},
            { coords = vector3(-2021.958, -473.7846, 10.89293), heading = 138.63},
        },

        ["Devis Abschlepphof"] = {
            { coords = vector3(394.48, -1625.619, 28.77805), heading = 51.32},
            { coords = vector3(396.8207, -1623.42, 28.77847), heading = 49.24},
            { coords = vector3(400.7062, -1618.789, 28.7784), heading = 50.7},
            { coords = vector3(385.1242, -1634.277, 28.77862), heading = 137.91},
            { coords = vector3(387.48, -1636.322, 28.77965), heading = 142.26},
        },
        
        ["Garage Towing Yard"] = {
            { coords = vector3(402.84921264648, -1616.4978027344, 29.291940689087), heading = 231.88035583496},
            { coords = vector3(401.21780395508, -1619.2060546875, 29.291940689087), heading = 238.05874633789},
            { coords = vector3(388.59014892578, -1612.5645751953, 29.291940689087), heading = 49.598037719727},
            { coords = vector3(390.59307861328, -1610.2729492188, 29.291940689087), heading = 50.550159454346},
            { coords = vector3(392.41836547852, -1608.1228027344, 29.291940689087), heading = 52.912658691406},
        },
        ["Garage Boat 1"] = {
            { coords = vector3(-797.06298828125,-1413.0871582031,0.35248219966888), heading = 50.45},
            { coords = vector3(-791.98718261719,-1405.9442138672,0.36012238264084), heading = 50.45},
            { coords = vector3(-786.43493652344,-1399.5565185547,0.3554439842701), heading = 50.45},
        },
        ["Airport Garage 1"] = {
            { coords = vector3(-1664.9295654297,-3145.6000976563,13.991494178772), heading = 328.48},
        },
}

```````
