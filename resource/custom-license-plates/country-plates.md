# Country Plates

46 countries, each with its real shape, font, colours and format, for cars and bikes

your server picks one style, every new car gets a random plate in that format

![](../../.gitbook/assets/vp_all_countries.png)

## europe, germany

![](../../.gitbook/assets/vp_car_de.jpg)

```lua
Config.Country = 'DE'
DE = { car = 'AA AA 999', bike = 'AA AA/999' }
```

## saudi arabia

![](../../.gitbook/assets/vp_car_sa2.jpg)

arabic and latin on the same plate, both drawn from the one plate text, every arabic letter and number sits right above its latin one like the real plate

![](../../.gitbook/assets/vp_sa_close.jpg)

```lua
SA = { car = '9999|AAA', bike = '9999/AAA', letters = 'ABJDRSXTEGKLZNHUV', strict = true }
```

saudi has a long and a short plate, the player picks one in the shop

## turkey

![](../../.gitbook/assets/vp_car_tr.jpg)

```lua
TR = { car = '99 AAA 999', bike = '99 AAA/999' }
```

## how the format works

| sign | means                     |
| ---- | ------------------------- |
| `A`  | a letter                  |
| `9`  | a number                  |
| `\|` | the divider (saudi, iran) |
| `/`  | second line, for bikes    |

* `letters` only these letters are used
* `strict = true` bought plates have to follow the format too
* GTA keeps 8 characters max

## change it in game

`/plateadmin` → Settings → Default plates

pick the server style, change any countrys car and bike format and its letters, save, done, no restart

![](../../.gitbook/assets/vp_admin_country.jpg)
