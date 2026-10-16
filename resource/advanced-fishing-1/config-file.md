# Config File

{% code title="config.lua" lineNumbers="true" %}
```lua
Config = {}
Config.MaxChannels = 4
Config.ShareGps = true
Config.ShowMemberStatus = true
Config.DefaultVolume = 50
Config.CarRadioDefault = false
Config.CarSpeaker = true
Config.CarSpeakerRange = 10.0


Config.Jammer = {
    item = 'radio_jammer',
    model = 'm23_2_prop_m32_jammer_01a',
    radii = { 50, 100, 150 },
    duration = 5 * 60, s
    maxWhitelist = 5
}


Config.Animations = {
    handheld = {
        { label = 'Handheld', dict = 'cellphone@', clip = 'cellphone_text_read_base',
            prop = true, bone = 57005, placement = { 0.14, 0.01, -0.02, 110.0, 120.0, -15.0 }, image= 'assets/animations/handheld-1.gif' },
        { label = 'Shoulder', dict = 'random@arrests', clip = 'generic_radio_enter' , image= 'assets/animations/handheld-4.gif' },
        { label = 'Radio pose', dict = 'anim@radio_pose_3', clip = 'radio_holding_gun',
            prop = true, bone = 60309, placement = { 0.075, 0.047, 0.011, -97.9442, 3.7058, -23.2367 }, image= 'assets/animations/handheld-3.gif' },

    },
    earpiece = {
        { label = 'Hand at ear', dict = 'cellphone@', clip = 'cellphone_call_listen_base', image= 'assets/animations/handheld-2.gif' },
        { label = 'Shoulder press', dict = 'random@arrests', clip = 'generic_radio_chatter', image= 'assets/animations/handheld-4.gif' }
    }
}

Config.RadioAnimationSettings = {
    handheld = { default = 1, disabled = false, playerChoice = true },
    earpiece = { default = 1, disabled = false, playerChoice = true },
}

Config.Sos = { hudSeconds = 15, blipSeconds = 60, radius = 60.0 }


Config.CarRadios = {
    ["ambulance"] = { frequency = "10.00", name = "Ambulance", jobs = { "ambulance" }, speaker = true, active = true },
    ["firetruk"] = { frequency = "40.00", name = "Fire Department", jobs = {  }, speaker = true, active = true },
    ["police"] = { frequency = "1.00", name = "Police", jobs = { "police" }, speaker = true, active = true },
    ["police2"] = { frequency = "20.00", name = "Police", jobs = { "police" }, speaker = true, active = true },
    ["police3"] = { frequency = "20.00", name = "Police", jobs = { "police" }, speaker = true, active = true },
    ["sheriff"] = { frequency = "30.00", name = "Sheriff", jobs = { "police" }, speaker = true, active = true },
    ["sheriff2"] = { frequency = "30.00", name = "Sheriff", jobs = { "police" }, speaker = true, active = true },
    ["taxi"] = { frequency = "50.00", name = "Taxi", jobs = {  }, speaker = false, active = true },
    ["towtruck2"] = { frequency = "2.61", name = "TOWTRUCK2", jobs = { "mechanic" }, speaker = true, active = true },
}

Config.AdminGroups = { 'admin', 'superadmin' }


Config.JobChannels = {
    { id = 1, label = "LSPD-1", freq = "1.00", jobs = { "police" }, password = "", hidden = false, active = true },
    { id = 3, label = "LSPD-PW", freq = "3.00", jobs = { "police" }, password = "1380", hidden = false, active = true },
    { id = 4, label = "SWAT-1", freq = "1.01", jobs = { "police" }, password = "", hidden = false, active = true },
    { id = 6, label = "COM-PW", freq = "5.11", jobs = { "ambulance", "police" }, password = "", hidden = false, active = true },
    { id = 7, label = "Mechanic", freq = "5.15", jobs = { "mechanic", "lumberjack" }, password = "1234", hidden = false, active = true },
    { id = 8, label = "Mechanic-2", freq = "4.00", jobs = { "mechanic" }, password = "", hidden = false, active = true },
}
```
{% endcode %}
