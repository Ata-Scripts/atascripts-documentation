# How It Works

## real plates

with `Config.RealPlates = true` (default) the plate a player buys becomes the cars real plate

when the plate goes on the car:

* the garage table gets the new plate, also inside the `vehicle` / `mods` json
* trunk, glovebox and any table in `Config.PlateLinks` move with it
* the car keys move to the new plate, for every supported key script
* ox\_inventory trunks and gloveboxes are moved too

everything changes in one database transaction, so its all or nothing, never half done

taking the plate off with a screwdriver gives the car its old plate back

## why your garage wont break

the script never touches your garage code

your garage just reads the plate from the database like it always does, and the database already has the new one, so the car comes out with the right plate, keys work and the trunk is still there

the script also checks that no other car already uses that plate before it changes anything

## only on screen

dont want plates to change at all? set

```lua
Config.RealPlates = false
```

the plate is only drawn on the car, the real plate never changes

## sync

the plate is a real 3D prop on the car, every player sees the same plate, holder and flip

props only load near you and go away when you leave, a resource restart puts everything back for everyone

## cars with a built in plate frame

some GTA cars (police, sultan, taxi, dukes and 22 more) have a plate frame baked into the model

the script finds them and puts a thin metal cover under your plate so the old frame doesnt show, add-on cars with the same frame go in `Config.FrameCoverModels`

## owned cars without a plate

```lua
defaultPlates = false   -- owned cars show no plate until one is bought
defaultPlates = true    -- owned cars keep their normal plate
```
