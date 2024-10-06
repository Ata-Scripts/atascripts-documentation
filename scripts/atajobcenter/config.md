# Config

{% tabs %}
{% tab title="ESX" %}
```lua
Config = {}


Config.Mysql = "mysql-async"


Config.NewQB = true
Config.GetSharedObject = 'QBCore:GetObject'

Config.TebexLink = 'https://ata.tebex.io/package/5820174'


Config.GithubVersionCheck = true

Config.GithubName = 'ataJobCenter_QB' -----!!!! DONT CHANGE PLEASEEE !!!!


Config.StartLocation = {
  pedcoords = vector4(-269.81802368164,-960.033203125,30.22313117981, 301.3229675293),
  pedModel = 'a_m_y_business_01',
  markercoord = vector3(-269.27758789063,-959.7373046875,30.22313117981),
  markerConfig = {
      Type = 1,
      rgb = {r = 255, g = 255, b = 0}
  },
  blip = {
      color = 5 ,
      name = 'Job Center' ,
      scale = 1.0,
      sprite = 407
  }
}



Config.NeedXP = {
  ['2'] = 1000,
  ['3'] = 1500,
  ['4'] = 2000,
  ['5'] = 3300,
  ['6'] = 3000,
  ['7'] = 3500,
  ['8'] = 4000,
  ['9'] = 4500,
  ['10'] = 5000
}




Config.Jobs = {
    {
      jobname = "LOS SANTOS MEDICAL DEPARTMENT",
      desc = "The Los Santos Medical Department: Leading healthcare in the heart of the city. Top-notch care, cutting-edge technology, and a dedicated team of professionals committed to your well-being.",
      level = 3,
      image = "./imgs/ambulance_bg.jpg", --- you can use image from local or URL
      logo = "./imgs/SMD_Logo.png", --- you can use image from local or URL
      whitelist = true,
      webhook = 'you Channel Webhook',
      setJobConfig = {
        name = 'ambualnce',
        grade = 0
      },
      questions = {
        "Why join the Medical Department?",
        "What previous medical experience do you have?",
        "How would you handle a medical emergency?",
        "Describe your experience working in a medical team.",
        "How do you ensure patient comfort and care during transportation?",
        "What medical certifications or training do you possess?",
        "How would you handle a situation where a patient is uncooperative or panicked?",
    },
    },
    {
      jobname = "LOS SANTOS POLICE DEPARTMENT",
      desc = "The Los Santos Police Department: Safeguarding the city with honor and diligence. Our brave officers uphold the law, maintain peace, and protect the community from harm. Committed to serving and ensuring a safe environment for all residents.",
      level = 5,
      image = "./imgs/police_bg.png",
      logo = "./imgs/R_29.webp",
      whitelist = true,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'police',
        grade = 0
      },
      questions = {
        "Why become a Police Officer?",
        "What motivates you to serve the community?",
        "How would you handle a high-stress law enforcement situation?",
        "Describe a time when you successfully de-escalated a tense situation.",
        "How do you balance enforcing the law with empathy towards individuals?",
        "How do you keep yourself updated on relevant laws and regulations?",
        "What steps would you take if you witness police misconduct within the department?",
    },
    },
    {
      jobname = "Maze Bank",
      desc = "Maze Bank: Your path to financial success. Trusted, innovative, and personalized banking services for a secure future.",
      level = 2,
      image = "./imgs/bank_bg.jpg",
      logo = "./imgs/maze_logo.jpg",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'banker',
        grade = 0
      },
      questions = {
        "What draws you to a career in banking at Maze Bank?",
        "Describe your experience in financial transactions and account management.",
        "How do you prioritize client confidentiality and data security?",
        "How would you handle a dissatisfied client with complex banking issues?",
        "What sets Maze Bank apart from other financial institutions?",
        "How do you stay informed about the latest banking regulations and trends?",
        "How do you handle ethical dilemmas that may arise in the banking industry?",
    },
    },
    {
      jobname = "Weazel News",
      desc = "Weazel News: Your 24/7 source for breaking stories and in-depth coverage. Keeping Los Santos informed with unbiased reporting and journalistic integrity. Stay connected and stay ahead with Weazel News.",
      level = 1,
      image = "./imgs/weazel_bg.jpg",
      logo = "./imgs/weazel.webp",
      whitelist = true,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'reporter',
        grade = 0
      },
      questions = {
        "What motivates you to work as a reporter in Los Santos?",
        "How do you ensure fair and unbiased reporting?",
        "Describe your experience in conducting investigative journalism.",
        "How do you handle sensitive stories with potential legal implications?",
        "What steps do you take to verify the credibility of your news sources?",
        "How do you approach interviewing individuals from diverse backgrounds?",
        "How do you handle criticism or feedback on your reporting?",
    },
    },
    {
      jobname = "Los Santos Taxi",
      desc = "Taxi Services: Your reliable ride at your fingertips. Fast, convenient, and safe transportation all around Los Santos. Experienced drivers ready to take you where you need to go, whenever you need it. Sit back, relax, and enjoy the journey with our top-notch taxi service.",
      level = 1,
      image = "./imgs/taxi_bg.webp",
      logo = "./imgs/taxi.jpg",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'taxi',
        grade = 0
      },
      questions = {
        "Why do you want to work as a taxi driver in Los Santos?",
        "How do you prioritize passenger safety and a comfortable ride experience?",
        "Describe your knowledge of the city's roads and popular destinations.",
        "How do you handle a situation where a passenger is intoxicated and disruptive?",
        "What measures do you take to maintain your vehicle for taxi services?",
        "How do you handle fare disputes and ensure fair pricing for customers?",
        "What do you do if you encounter an emergency situation during a taxi ride?",
    },
    },
    {
      jobname = "LS Custom",
      desc = "LS Custom: Your one-stop auto shop in Los Santos. Transform your ride into a personalized masterpiece. Skilled mechanics and a vast selection of upgrades to enhance performance and style. From flashy aesthetics to powerful engines, we make your automotive dreams a reality at LS Custom.",
      level = 3,
      image = "./imgs/mechanic.jpg",
      logo = "./imgs/ls.webp",
      whitelist = true,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'mechanic',
        grade = 0
      },
      questions = {
        "Why did you decide to pursue a career as a mechanic at LS Custom?",
        "Describe your experience in automotive repair and customization.",
        "How do you prioritize and manage multiple repair jobs efficiently?",
        "How would you handle a complex repair project with limited resources?",
        "What steps do you take to ensure customer satisfaction with your work?",
        "How do you keep up with advancements in automotive technology and trends?",
        "How do you handle unexpected challenges that may arise during repairs?",
    },
    },
    {
      jobname = "Fisherman",
      desc = "The Fisherman: Reel in the adventure. Discover serene fishing spots and hook your perfect catch in Los Santos. Beginner-friendly tours and top-notch equipment for an unforgettable experience.",
      level = 1,
      image = "./imgs/fisher_bg.jpeg",
      logo = "./imgs/fish.png",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'fisherman',
        grade = 0
      },
      questions = {
        "What draws you to the life of a fisherman in Los Santos?",
        "Describe your fishing experience and the types of fish you've caught.",
        "How do you ensure sustainable fishing practices to protect marine life?",
        "What safety measures do you follow while out at sea?",
        "How do you handle unexpected weather changes during fishing trips?",
        "What do you do if you encounter illegal fishing activities?",
        "How do you ensure the quality and freshness of your catches for sale?",
    },
    },
    {
      jobname = "Lumberjack",
      desc = "The Lumberjack: Conquer the wilderness. Become a skilled woodcutter in Los Santos, harvesting timber and embracing nature's beauty.",
      level = 1,
      image = "./imgs/lumberjack_bg.jpg",
      logo = "./imgs/fish.png",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'lumberjack',
        grade = 0
      },
      questions = {
        "Why did you choose to work as a lumberjack in Los Santos?",
        "Describe your experience in felling trees and handling timber.",
        "How do you ensure safety while operating logging machinery?",
        "What steps do you take to minimize environmental impact during logging activities?",
        "How do you handle emergencies such as accidents or injuries in the wilderness?",
        "What safety protocols do you follow to prevent forest fires during logging?",
        "How do you ensure compliance with regulations and permits for logging operations?",
    },
    },
}


Config.Local = {
  ['jobsetit'] = 'Welcome To : ',
  ['jobWhitelistSend'] = 'Your Whitelist Sended To : ',
  ['buyLevel'] = 'thank you for purchase you get a level in job center menu. enjoy',
  ['OpenMenu'] = 'Press ~INPUT_CONTEXT~ To Open ~y~Job Center',
  ['getXP'] = '[JOB CENTER] You Recive : ',
  ['getLevel'] = '[JOB CENTER] Your Level Upgrade To : ',
}


Config.discordWebhookimage = 'https://cdn.discordapp.com/attachments/692339336343191586/1133482013182136361/8c344128fdac705708d68ad3ae923680.png'

function Notification(msg)
        TriggerEvent('QBCore:Notify',msg)
end

function helptext(str)
	SetTextComponentFormat("STRING")
	AddTextComponentString(str)
	DisplayHelpTextFromStringLabel(0, 0, 1, -1)
end
```
{% endtab %}

{% tab title="QB" %}
```lua
Config = {}


Config.Mysql = "mysql-async"


Config.ESX_1_9_0 = true
Config.GetSharedObject = 'esx:getSharedObject'

Config.TebexLink = 'https://ata.tebex.io/package/5820174'


Config.GithubVersionCheck = true

Config.GithubName = 'ataJobCenter_ESX' -----!!!! DONT CHANGE PLEASEEE !!!!


Config.StartLocation = {
  pedcoords = vector4(-269.81802368164,-960.033203125,30.22313117981, 301.3229675293),
  pedModel = 'a_m_y_business_01',
  markercoord = vector3(-269.27758789063,-959.7373046875,30.22313117981),
  markerConfig = {
      Type = 1,
      rgb = {r = 255, g = 255, b = 0}
  },
  blip = {
      color = 5 ,
      name = 'Job Center' ,
      scale = 1.0,
      sprite = 407
  }
}



Config.NeedXP = {
  ['2'] = 1000,
  ['3'] = 1500,
  ['4'] = 2000,
  ['5'] = 3300,
  ['6'] = 3000,
  ['7'] = 3500,
  ['8'] = 4000,
  ['9'] = 4500,
  ['10'] = 5000
}




Config.Jobs = {
    {
      jobname = "LOS SANTOS MEDICAL DEPARTMENT",
      desc = "The Los Santos Medical Department: Leading healthcare in the heart of the city. Top-notch care, cutting-edge technology, and a dedicated team of professionals committed to your well-being.",
      level = 3,
      image = "./imgs/ambulance_bg.jpg", --- you can use image from local or URL
      logo = "./imgs/SMD_Logo.png", --- you can use image from local or URL
      whitelist = true,
      webhook = 'you Channel Webhook',
      setJobConfig = {
        name = 'ambualnce',
        grade = 0
      },
      questions = {
        "Why join the Medical Department?",
        "What previous medical experience do you have?",
        "How would you handle a medical emergency?",
        "Describe your experience working in a medical team.",
        "How do you ensure patient comfort and care during transportation?",
        "What medical certifications or training do you possess?",
        "How would you handle a situation where a patient is uncooperative or panicked?",
    },
    },
    {
      jobname = "LOS SANTOS POLICE DEPARTMENT",
      desc = "The Los Santos Police Department: Safeguarding the city with honor and diligence. Our brave officers uphold the law, maintain peace, and protect the community from harm. Committed to serving and ensuring a safe environment for all residents.",
      level = 5,
      image = "./imgs/police_bg.png",
      logo = "./imgs/R_29.webp",
      whitelist = true,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'police',
        grade = 0
      },
      questions = {
        "Why become a Police Officer?",
        "What motivates you to serve the community?",
        "How would you handle a high-stress law enforcement situation?",
        "Describe a time when you successfully de-escalated a tense situation.",
        "How do you balance enforcing the law with empathy towards individuals?",
        "How do you keep yourself updated on relevant laws and regulations?",
        "What steps would you take if you witness police misconduct within the department?",
    },
    },
    {
      jobname = "Maze Bank",
      desc = "Maze Bank: Your path to financial success. Trusted, innovative, and personalized banking services for a secure future.",
      level = 2,
      image = "./imgs/bank_bg.jpg",
      logo = "./imgs/maze_logo.jpg",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'banker',
        grade = 0
      },
      questions = {
        "What draws you to a career in banking at Maze Bank?",
        "Describe your experience in financial transactions and account management.",
        "How do you prioritize client confidentiality and data security?",
        "How would you handle a dissatisfied client with complex banking issues?",
        "What sets Maze Bank apart from other financial institutions?",
        "How do you stay informed about the latest banking regulations and trends?",
        "How do you handle ethical dilemmas that may arise in the banking industry?",
    },
    },
    {
      jobname = "Weazel News",
      desc = "Weazel News: Your 24/7 source for breaking stories and in-depth coverage. Keeping Los Santos informed with unbiased reporting and journalistic integrity. Stay connected and stay ahead with Weazel News.",
      level = 1,
      image = "./imgs/weazel_bg.jpg",
      logo = "./imgs/weazel.webp",
      whitelist = true,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'reporter',
        grade = 0
      },
      questions = {
        "What motivates you to work as a reporter in Los Santos?",
        "How do you ensure fair and unbiased reporting?",
        "Describe your experience in conducting investigative journalism.",
        "How do you handle sensitive stories with potential legal implications?",
        "What steps do you take to verify the credibility of your news sources?",
        "How do you approach interviewing individuals from diverse backgrounds?",
        "How do you handle criticism or feedback on your reporting?",
    },
    },
    {
      jobname = "Los Santos Taxi",
      desc = "Taxi Services: Your reliable ride at your fingertips. Fast, convenient, and safe transportation all around Los Santos. Experienced drivers ready to take you where you need to go, whenever you need it. Sit back, relax, and enjoy the journey with our top-notch taxi service.",
      level = 1,
      image = "./imgs/taxi_bg.webp",
      logo = "./imgs/taxi.jpg",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'taxi',
        grade = 0
      },
      questions = {
        "Why do you want to work as a taxi driver in Los Santos?",
        "How do you prioritize passenger safety and a comfortable ride experience?",
        "Describe your knowledge of the city's roads and popular destinations.",
        "How do you handle a situation where a passenger is intoxicated and disruptive?",
        "What measures do you take to maintain your vehicle for taxi services?",
        "How do you handle fare disputes and ensure fair pricing for customers?",
        "What do you do if you encounter an emergency situation during a taxi ride?",
    },
    },
    {
      jobname = "LS Custom",
      desc = "LS Custom: Your one-stop auto shop in Los Santos. Transform your ride into a personalized masterpiece. Skilled mechanics and a vast selection of upgrades to enhance performance and style. From flashy aesthetics to powerful engines, we make your automotive dreams a reality at LS Custom.",
      level = 3,
      image = "./imgs/mechanic.jpg",
      logo = "./imgs/ls.webp",
      whitelist = true,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'mechanic',
        grade = 0
      },
      questions = {
        "Why did you decide to pursue a career as a mechanic at LS Custom?",
        "Describe your experience in automotive repair and customization.",
        "How do you prioritize and manage multiple repair jobs efficiently?",
        "How would you handle a complex repair project with limited resources?",
        "What steps do you take to ensure customer satisfaction with your work?",
        "How do you keep up with advancements in automotive technology and trends?",
        "How do you handle unexpected challenges that may arise during repairs?",
    },
    },
    {
      jobname = "Fisherman",
      desc = "The Fisherman: Reel in the adventure. Discover serene fishing spots and hook your perfect catch in Los Santos. Beginner-friendly tours and top-notch equipment for an unforgettable experience.",
      level = 1,
      image = "./imgs/fisher_bg.jpeg",
      logo = "./imgs/fish.png",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'fisherman',
        grade = 0
      },
      questions = {
        "What draws you to the life of a fisherman in Los Santos?",
        "Describe your fishing experience and the types of fish you've caught.",
        "How do you ensure sustainable fishing practices to protect marine life?",
        "What safety measures do you follow while out at sea?",
        "How do you handle unexpected weather changes during fishing trips?",
        "What do you do if you encounter illegal fishing activities?",
        "How do you ensure the quality and freshness of your catches for sale?",
    },
    },
    {
      jobname = "Lumberjack",
      desc = "The Lumberjack: Conquer the wilderness. Become a skilled woodcutter in Los Santos, harvesting timber and embracing nature's beauty.",
      level = 1,
      image = "./imgs/lumberjack_bg.jpg",
      logo = "./imgs/fish.png",
      whitelist = false,
      webhook = 'https://discord.com/api/webhooks/1133469268411957329/fwdrfMAgzzVcYaKOYzpxVl45grFf6O3lqncajUNTkvjfo79vA9xvYUe2gF_60tv7M-kG',
      setJobConfig = {
        name = 'lumberjack',
        grade = 0
      },
      questions = {
        "Why did you choose to work as a lumberjack in Los Santos?",
        "Describe your experience in felling trees and handling timber.",
        "How do you ensure safety while operating logging machinery?",
        "What steps do you take to minimize environmental impact during logging activities?",
        "How do you handle emergencies such as accidents or injuries in the wilderness?",
        "What safety protocols do you follow to prevent forest fires during logging?",
        "How do you ensure compliance with regulations and permits for logging operations?",
    },
    },
}


Config.Local = {
  ['jobsetit'] = 'Welcome To : ',
  ['jobWhitelistSend'] = 'Your Whitelist Sended To : ',
  ['buyLevel'] = 'thank you for purchase you get a level in job center menu. enjoy',
  ['OpenMenu'] = 'Press ~INPUT_CONTEXT~ To Open ~y~Job Center',
  ['getXP'] = '[JOB CENTER] You Recive : ',
  ['getLevel'] = '[JOB CENTER] Your Level Upgrade To : ',
}


Config.discordWebhookimage = 'https://cdn.discordapp.com/attachments/692339336343191586/1133482013182136361/8c344128fdac705708d68ad3ae923680.png'

function Notification(msg)
        ESX.ShowNotification(msg)
end

function helptext(str)
	SetTextComponentFormat("STRING")
	AddTextComponentString(str)
	DisplayHelpTextFromStringLabel(0, 0, 1, -1)
end
```
{% endtab %}
{% endtabs %}
