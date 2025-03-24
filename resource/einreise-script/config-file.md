# Config File

```lua
Config = {}
Question = {}
Config.Debug = false -- true , false

Config.InteractionWithTarget = false -- true , false [if false then it will use TextUI for interaction]
Config.AskQuestionIfMethodAdmin = true -- true , false (( Check if the method is no online admin is online then ask question ))
Config.AllowedGroup = {'god','admin','mod'}  --- group that can use admin command and get notification when player request verify
Config.QuestionCurrectAnswer = 80 -- 80% correct answer to join the server
Config.CoolDown = 10000 -- 10 seconds for send notification to all staff for player NPC call
Config.RandomizeQuestions = true -- true , false [if true then it will randomize the questions]

Config.ChangeSettings = { --- Allowed to change settings for player that have this steam or license
    'steam:1234567890',
    'license:123456789',
}

Config.AdminCommand = {
    ['main'] = 'einreise',
    ['legal'] = 'legal',
    ['illegal'] = 'illegal',
    ['back'] = 'back',
    ['notificationType'] = 'defualt', -- defualt , ata-core << you can adjust in client/main.lua >>
    ['admin_menu'] = 'einreise_menu'
}

 
Config.Legal = {
    ['VerifyMethod'] = 'question', --- free , admin , question , lock
    ['NPCLocation'] = vector3(-1034.53, -2732.5, 19.17),  ---- NPC Coords (For Contact Staff and Question Menu)
    ['NPCHeading'] = 146.82, ---- NPC Heading (For Contact Staff and Question Menu)
    ['NPCModel'] = 'ig_solomon', ---- NPC Model (For Contact Staff and Question Menu)
    ['NPCTextUI'] = 'talk with airport staff', ---- NPC Text UI Config.InteractionWithTarget (For Contact Staff and Question Menu)
    ['AdminJoinCoords'] = vector4(-1033.25, -2739.77, 20.17, 75.27), ---- Admin spawn point !! This is Vector 4 (X,Y,Z,W)
    ['PlayerWaitingCoords'] = vector4(-1037.82, -2737.67, 19.17,76.51), ---- Player waiting list coords !! This is Vector 4 (X,Y,Z,W)   
    ['PlayerWaitingCoordsRadius'] = 30, ---- Player waiting list radius to teleport back
    ['PlayerCoordsAfterVerify'] = vector4(-966.02, -2609.3, 13.98, 330.44) ---- Player coords after verify
}

Config.Illegal = {
    ['VerifyMethod'] = 'admin', --- free , admin , question , lock
    ['NPCLocation'] = vector3(1304.84, 4232.41, 32.91),  ---- NPC Coords (For Contact Staff and Question Menu)
    ['NPCHeading'] = 259.2, ---- NPC Heading (For Contact Staff and Question Menu)
    ['NPCModel'] = 'u_m_m_streetart_01', ---- NPC Model (For Contact Staff and Question Menu)
    ['NPCTextUI'] = 'for talk with illegal staff',  ---- NPC Text UI Config.InteractionWithTarget (For Contact Staff and Question Menu)
    ['AdminJoinCoords'] = vector4(1302.63, 4229.33, 33.91, 285.86) , ---- Admin spawn point !! This is Vector 4 (X,Y,Z,W)
    ['PlayerWaitingCoords'] = vector4(1316.15, 4230.0, 33.92, 76.51), ---- Player waiting list coords !! This is Vector 4 (X,Y,Z,W) 
    ['PlayerWaitingCoordsRadius'] = 30, ---- Player waiting list radius to teleport back
    ['PlayerCoordsAfterVerify'] = vector4(1314.46, 4307.15, 37.95, 358.52) ---- Player coords after verify
}


Config.Locale = {
    ['joined_illegal'] = 'joined the illegal', -- if you are using normal notification not defualt script UI NOTIFICATION ADMIN
    ['joined_legal'] = 'joined the legal', -- if you are using normal notification not defualt script UI NOTIFICATION ADMIN
    ['accept_player'] = "You have accepted id: ",
    ['free_verify_success'] = 'Welcome To Server',
    ['dont_have_permission'] = 'You dont have permission to use this command',
    ['dont_have_permission_settings'] = 'You dont have permission to change settings',
    ['settings_updated'] = 'Settings updated',
    ['deny_player'] = "You have denied id: ",
    ['kick_reason'] = 'You are not allowed to join',
    ['cool_down'] = 'You are on cool down',
    ['back_to_last_location'] = 'You can back to last location with /'..Config.AdminCommand.back ,
    ['called_to_all_staff'] = 'i called to all online staff',

    ['question_verify_success'] = 'You have verified by system your answer is correct',
    ['question_verify_failed'] = 'You have not verified by system your answer is incorrect',

    ['admin_command_missing_argument'] = 'Missing argument. /' .. Config.AdminCommand.main .. ' ' .. Config.AdminCommand.legal .. ' or /'..Config.AdminCommand.main .. ' ' .. Config.AdminCommand.illegal,
    ['admin_command_invalid_argument'] = 'Invalid argument: ' .. Config.AdminCommand.main .. ' ' .. Config.AdminCommand.legal .. ' or /'..Config.AdminCommand.main .. ' ' .. Config.AdminCommand.illegal,
    
    ['Webhook_admin_call_illegal'] = 'Want To Join : `Illegal`', 
    ['Webhook_admin_call_legal'] = 'Want To Join : `Legal`',
    ['Webhook_admin_call_illegal_header'] = 'Player in waiting list:',
    ['Webhook_admin_call_legal_header'] = 'Player in waiting list:', 

    ['Webhook_verified_illegal'] = 'verified by: [ADMIN]', 
    ['Webhook_verified_legal'] = 'verified by: [ADMIN]',
    ['Webhook_verified_illegal_header'] = 'Player verified Illegal :',
    ['Webhook_verified_legal_header'] = 'Player verified Legal :', 

    ['Webhook_question_verify_success'] = 'verified by: [Question Verify System]',
    ['Webhook_question_verify_success_header'] = 'Player verified Illegal :',
    ['Webhook_question_verify_failed'] = 'not verified by: [Question Verify System]',
    ['Webhook_question_verify_failed_header'] = 'Player verified Illegal :',

    ['Webhook_settings_updated'] = 'Settings updated By ',
    ['Webhook_settings_updated_illegal'] = 'Now **Illegal** Verify Method is : ',
    ['Webhook_settings_updated_legal'] = 'Now **Legal** Verify Method is : ',

    ['Webhook_free_verify_illegal_success'] = 'verified by: [Free Verify System]',
    ['Webhook_free_verify_illegal_header'] = 'Player verified Illegal :',

    ['Webhook_free_verify_legal_success'] = 'verified by: [Free Verify System]',
    ['Webhook_free_verify_legal_header'] = 'Player verified Legal :',
}
 


function Debug(text)
    if Config.Debug then
        print('[ATA-Einreise] '..text)
    end
end
```

