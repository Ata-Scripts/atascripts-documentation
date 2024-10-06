# ataUIPack

[**Youtube Preview**](https://youtu.be/rF4MX9HEWOw?si=Xn2uYgCP0\_t2H-PG)



## Request Send

### Server Side

```lua
TriggerClientEvent('ataUI:Request', source, {
        title = 'Test Request',
        msg = 'This is a test request.',
        serverORclient = 'client',
        TriggerEvent = 'test:Response',
        CountParameter = 1,
        Parameter = { 'test' }
})
```

### Client Side

```lua
TriggerEvent('ataUI:Request', PlayerID, {
        title = 'Test Request',
        msg = 'This is a test request.',
        serverORclient = 'client',
        TriggerEvent = 'test:Response',
        CountParameter = 1,
        Parameter = { 'test' }
    })
```

***

## Open TEXT with Key

JUST WORK IN CLIENT SIDE

## for Open

```lua
lua exports["ataUI"]:openText('e','OPEN DOOR','dark','#fff','#000')
```

## for Close

```lua
exports["ataUI"]:closeText()
```

***

## Notification

### client Side

```lua
TriggerEvent('ataUI:not',{Theme = 'dark',Type = 'warn',title = 'TITLE HERE',msg = 'MSG HERE',time = '2000', icon = 'fas fa-question-circle' })
```

### server Side

```lua
TriggerClientEvent('ataUI:not',source,{Theme = 'dark',Type = 'warn',title ='TITLE HERE',msg = 'MSG HERE',time = '2000', icon = 'fas fa-question- circle'})
```

***

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
