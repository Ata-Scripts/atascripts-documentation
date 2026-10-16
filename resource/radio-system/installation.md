# Installation

{% hint style="warning" %}
The resource folders must be named exactly `ata_Radio` and `pma-voice`.
{% endhint %}

### 1. Add the resource

Put the `ata_Radio` folder in your resources folder.

### 2. Set up pma-voice

Only one file needs to change: `pma-voice/fxmanifest.lua`. Nothing else in pma-voice is edited.

Add this line directly **before** the `server_scripts {` block:

{% code title="pma-voice/fxmanifest.lua" %}
```lua
server_script '@ata_Radio/integrations/pma-server.lua'

server_scripts {
    -- pma's original entries, untouched
}
```
{% endcode %}

Add these two lines at the **bottom** of the file:

{% code title="pma-voice/fxmanifest.lua" %}
```lua
dependency 'ata_Radio'
client_script '@ata_Radio/integrations/pma-client.lua'
```
{% endcode %}

### 3. Start order

`ata_Radio` must start before `pma-voice`.

{% code title="server.cfg" %}
```
ensure ata_Radio
ensure pma-voice
```
{% endcode %}

### 4. Add the items

The script uses three items: `radio`, `earpiece` and `radio_jammer`.

{% tabs %}
{% tab title="ox_inventory" %}
Add these to `ox_inventory/data/items.lua`:

```lua
['radio'] = {
    label = 'Radio', weight = 1000, stack = false, allowArmed = true, close = true, consume = 0,
    client = { export = 'ata_Radio.useRadio' }
},
['earpiece'] = {
    label = 'Earpiece', weight = 100, stack = false, close = true, consume = 0,
    client = { export = 'ata_Radio.useEarpiece', image = 'https://cfx-nui-ata_Radio/html/assets/earpiece.png' }
},
['radio_jammer'] = {
    label = 'Radio Jammer', weight = 3000, stack = false, close = true, consume = 0,
    client = { export = 'ata_Radio.useJammer' }
},
```
{% endtab %}

{% tab title="ESX inventory / qb-inventory" %}
Add the `radio`, `earpiece` and `radio_jammer` items to your items list. The script makes them usable automatically.
{% endtab %}
{% endtabs %}

### 5. Restart the server

Check that the bridge is loaded:

* Server console: `[ata_Radio] pma server bridge loaded; stock radio dispatch is filtered.`
* Client F8 console: `[ata_Radio] pma client bridge loaded; exports registered.`

{% hint style="info" %}
The database table `ata_radio_player` is created automatically on the first start.
{% endhint %}
