# ataNotify V2

[**Youtube Preview**](https://youtu.be/Uwj77Pp3woM?si=aQz0jbmPt5J-usJD)



Examples:

```lua
 exports["ataNotify2"]:Notify(
 		"TITLE HERE",
 		"MASSAGE HERE",
 		10000, ---TIME (IS MS)
 		"success", --@type 'success' | 'error' | 'info' | 'warn'
 		"IMAGE LINK" --IMAGE LINK OR LOCATION --- Not requirement
 	)
```

```lua
exports["ataNotify2"]:Notify(
		"Garage",
		"You can take own vehicle from this area ",
		5000,
		"info",
		"https://cdn.discordapp.com/attachments/1032691691666288710/1245106076634845204/parking.png?ex=66578ae5&is=66563965&hm=f9f54a31291bf86974048b695f5e7b78fc7cc63c637f6afcfa958b7cdc088ab8&"
	)
```

```lua
exports["ataNotify2"]:Notify(
		"Server Owner",
		"Mauris nec fringilla tellus, et ultrices dolor. Mauris pellentesque quam id purus ultricies, quis feugiat neque cursus. Aenean non luctus est, ut mattis tortor. In id nisi ut sem auctor posuere id vel tortor. Morbi porta porta tellus in porta.",
		7000,
		"info",
		"https://cdn.discordapp.com/attachments/1138288504548368425/1245107421760852120/ssa.png?ex=66578c26&is=66563aa6&hm=eec9a5550d5230d3292f1c32378dd491cecf5fd66417c04bd11d4bfa085165f4&"
	)

```

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
