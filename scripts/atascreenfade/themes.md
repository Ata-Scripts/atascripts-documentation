# Themes

### we added more 10+ themes in client/themes so you can easy yo use and make better for you server

### **`Logo Setting:`**

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### Customizing the Loading Screen for Dynamic Screen Fade Control

Configure the appearance of your loading screen with precision using our script's flexible settings. You can customize everything from the logo to the background and loading spinner.

#### Logo Settings

* **Logo**: Place your custom logo within the `html/img` directory for easy access. Recommended format is SVG,PNG for optimal clarity. Example: `img/ata2.svg`. or URL
* **Shadow**: Add a subtle shadow to the logo for enhanced visual depth. This feature can be disabled by setting `shadow` to `false`.
* **Animation Logo**: Assign a predefined animation to your logo to make it dynamic and engaging. Select from the list of available animations below.  [#list-of-animation-classes](themes.md#list-of-animation-classes "mention")

#### List of Animation Classes

* **`fill-up-animation`**: Reveals the logo from the bottom upwards.
* **`fill-bottom-animation`**: Unveils the logo from the top downwards.
* **`fill-right-animation`**: Shows the logo from left to right.
* **`fill-left-animation`**: Displays the logo from right to left.
* **`bounce-animation`**: Makes the logo bounce vertically.
* **`fade-animation`**: Fades the logo in and out smoothly.
* **`shake-animation`**: Adds a shaking effect to the logo.
* **`zoom-animation`**: Zooms the logo in and out.
* **`rotate-scale-animation`**: Rotates and scales the logo alternately.
* **`slide-animation`**: Slides the logo from the top.
* **`rotate-animation`**: Continuously rotates the logo.
* **`flip-animation`**: Flips the logo around the center axis.
* **`scale-animation`**: Scales the logo up and down.
* **`scale-animation-x2`**: Doubles the scaling effect on the logo.
* **`invert-animation`**: Inverts the colors of the logo.

### **`Background Setting:`**

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Customize the background with colors that match your server’s theme.

* **Color 1**: Primary background color, such as `#1D1045`.
* **Color 2**: Secondary background color, which can be set to create a gradient effect, such as `#000000`.

### **`Spinner Setting:`**

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>



Manage how the loading spinner and text appear during the screen transitions.

* **Spinner Visibility**: Control whether a spinner is shown by setting `spinnerIsOn` to `true` or `false`.
* **Spinner Settings**:
  * **Size**: Set the size of the spinner as a percentage, like `90`.
  * **Position**: Specify the position of the spinner relative to the logo, such as `belowLogo`.
  * **Style**: Choose the spinner animation style from predefined styles (e.g., `load8`).
  * **Default Text**: Customize the text displayed during loading, such as `"LOADING..."`.
  * **Color**: Set the color for both the spinner and the loading text, like `#EC83BC`.

## example themes :thumbsup:

{% code title="themes/ataThemes.lua" %}
```lua
return {
    logoSettings = {
        logo = "img/ata2.svg", --- your defualt logo 
        shadow = false, -- logo have animation in background ?
        animation_logo = "fill-right-animation", -- your logo animation
    },
    background = {
        color1 = '#1D1045', -- background  color 1
        color2= '#000000', --- background color 2
    },
    loadingScreen = {
        spinnerIsOn = false, -- defualt have spinner ?
        spinnerSettings = {
            size = 90, --- spinner size 0% - 100%
            position = "belowLogo", -- spinner position
            style = 'load8', --- spinner Style
            defaultText = "LOADING...", -- defualt spinner text
            color = "#EC83BC"  --- spinner and text color
        },
    }
}
```
{% endcode %}
