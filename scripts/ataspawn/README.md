# ataSpawn

[**Youtube Preview**](https://youtu.be/fw8cqg9HD6Q?si=pEBQEnasKlPI2xcR)



## go esx\_identity

in esx\_identity/client/main.lua

Find Here

```lua
RegisterNetEvent("esx_identity:alreadyRegistered", function()
  while not loadingScreenFinished do Wait(100) end
  TriggerEvent("esx_skin:playerRegistered")
end)
```

And Replace This

```lua
RegisterNetEvent("esx_identity:alreadyRegistered", function()
  while not loadingScreenFinished do Wait(100) end
  TriggerEvent("esx_skin:playerRegistered")
  TriggerEvent('ataSpawn:ShowSpawnLocation')
end)
```

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
