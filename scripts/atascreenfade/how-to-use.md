# How To Use ?

## Defualt  (Settings Your Choose Theme)

{% tabs %}
{% tab title="Native" %}
<pre class="language-lua"><code class="lang-lua"><strong>DoScreenFadeOut(1000)
</strong><strong>
</strong>--- For Hide 
<strong>
</strong><strong>DoScreenFadeIn(1000)
</strong></code></pre>
{% endtab %}

{% tab title="Second Tab" %}
```lua
exports['ataScreenFade']:DisplayLoad(1000)


--- For Hide 

exports['ataScreenFade']:HideLoad(1000)
```
{% endtab %}
{% endtabs %}

## Customization Fade

{% tabs %}
{% tab title="Native" %}
```lua
DoScreenFadeOut(1000, {
    logo = 'img/ata2.svg',               -- Path to the logo image.
    animation_logo = 'slide-animation',  -- Type of animation for the logo.
    color1 = '#fff',                     -- Primary color used in the fade effect.
    color2 = '#ddf222',                  -- Secondary color used in the fade effect.
    spinner = true,                      -- Enable spinner during the fade-out.
    loadingText = 'Welcome To Police Department ...',  -- Custom text displayed during loading.
    colorSpinner = '#0f0f'               -- Color of the spinner.
})


--- For Hide 

DoScreenFadeIn(1000)
```
{% endtab %}

{% tab title="Export Function" %}
```lua
exports['ataScreenFade']:DisplayLoad(1000, {
    logo = 'img/ata2.svg',               -- Path to the logo image.
    animation_logo = 'slide-animation',  -- Type of animation for the logo.
    color1 = '#fff',                     -- Primary color used in the fade effect.
    color2 = '#ddf222',                  -- Secondary color used in the fade effect.
    spinner = true,                      -- Enable spinner during the fade-out.
    loadingText = 'Loading',             -- Custom text displayed during loading.
    colorSpinner = '#0f0f'               -- Color of the spinner.
})


--- For Hide 
exports['ataScreenFade']:HideLoad(1000)
```
{% endtab %}
{% endtabs %}

* **logo**: Specify the path to the logo image you wish to display during the fade-out.
* **animation\_logo**: Choose an animation style for the logo to enhance visual appeal.
* **color1** and **color2**: Define the colors background used in the fade effect to match your server's theme.
* **spinner**: Enable a loading spinner to indicate activity during the screen transition.
* **loadingText**: Set a custom message to greet players or provide information during the loading phase.
* **colorSpinner**: Customize the spinner color to complement the overall design.





{% hint style="info" %}
you can just send 1 config to change :) also this is not save in config so you can add more customizion for any script with anythig you want
{% endhint %}





***
