# Replace esx\_TextUI

## es\_extended/client/functions.lua

***

**ESX.TextUI:**

```lua
function ESX.TextUI(message, type)
    if type == 'info' or type == 'error' then
        theme = 'dark'
    elseif type == 'success' then
        theme = 'light'
    end

    if GetResourceState('ataUI') ~= 'missing' then
        exports["ataUI"]:openText('E', message, theme,'#ffffff','#000000')
    else
        print('[^1ERROR^7] ^5ataUI^7 is Missing!')
    end
end
```

**ESX.HideUI:**

```lua
function ESX.HideUI()
    if GetResourceState("ataUI") ~= "missing" then
        exports["ataUI"]:closeText()
    else 
        print("[^1ERROR^7] ^5ataUI^7 is Missing!")
    end
end
```

You can also change the colors as you like it after `theme`. For now i set it to **white** _(#ffffff)_ & **black** _(#000000)_\

