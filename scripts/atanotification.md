# ataNotification

[**Youtube Preview**](https://youtu.be/XSKP5F\_-CKE?si=nmML7tyVmuuQIhhj)



## Server Side&#x20;

```lua
TriggerClientEvent('ataNotification:show', source, {
    sound = 'not1',
    icon = 'fas fa-exclamation-circle text-danger',
    title = 'Nastala chyba',
    message = 'hi world',
    time = 7000,
    appname = 'Server'
})
```

## Client Side

```lua
TriggerEvent('ataNotification:show',{
    sound = 'not1',
    icon = 'fas fa-exclamation-circle text-danger',
    title = 'Nastala chyba',
    message = 'hi world',
    time = 7000,
    appname = 'Server'
})

```

## Test All Notify And Style



```lua
RegisterCommand('long', function()
	exports['ataNotification']:notification('far fa-keyboard text-primary','Long text test',"This is long text test", "Lorem, ipsum dolor sit amet consectetur adipisicing elit. odio harum explicabo eligendi quibusdam pariatur temporibus ducimus, ea iste! Fugit temporibus aliquam tempore sint ipsum? Beatae, sed. Perspiciatis mollitia voluptatum aperiam est!		", 15000,'not1')
end)

RegisterCommand('gmail', function()
	exports['ataNotification']:notification('far fa-envelope-open text-danger','GMAIL',"", "You have been accepted to Harvard University. Click on the link below to see more information", 15000)
end)

RegisterCommand('error', function()
	exports['ataNotification']:notification('fas fa-exclamation-circle text-danger','Server',"ERROR", "You do not have permission to do this", 15000)
end)
RegisterCommand('whatsapp', function()
	exports['ataNotification']:notification('fab fa-whatsapp text-success','WHATSAPP',"Carl Johnson", "Hello Where Are You ??", 15000,'not2')
end)


RegisterCommand('visa', function()
	exports['ataNotification']:notification('fab fa-cc-visa text-info','Visa',"Transfer Money", "You Have Sent 300$ To Ata!", 15000,"not1")
end)

RegisterCommand('test', function()
	exports['ataNotification']:notification('far fa-check-circle text-success','Your Server Name',"SUCCESS", "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia.", 15000)
end)

```
