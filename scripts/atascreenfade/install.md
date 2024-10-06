# install

### Installation Guide for Screen Fade&#x20;

Our script offers two methods for integration into your FiveM server, ensuring flexibility based on your server setup preferences.

## Method 1: Automatic Installation

This method automatically updates the `fxmanifest.lua` for all resources on your server.

**Steps for Automatic Installation:**

1.  Ensure automatic manifest replacement is enabled in your configuration:

    ```lua
    Config.AutoReplaceManifest = true
    ```
2.  Execute the following command in your server console to install:

    ```
    ata_screenfade install
    ```
3.  For additional commands and help, use:

    ```bash
    ata_screenfade help
    ```
4.  To revert all changes made by the script to your resource manifests, use:

    ```
    ata_screenfade uninstall
    ```

{% hint style="info" %}
**Note:** Using this installation method will insert specific codes into the `fxmanifest.lua` and `__resource.lua` files across your resources. If you prefer a manual setup, see Method 2.
{% endhint %}

## Method 2: Manual Installation

in this method you can call screen fade native with exports (JUST CLIENT SIDES)

### ScreenFadeOut

```lua
exports['ataScreenFade']:DisplayLoad(1000)
```

### ScreenFadeIn

```lua
 exports['ataScreenFade']:HideLoad(1000)
```

