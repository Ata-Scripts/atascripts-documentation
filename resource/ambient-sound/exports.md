# Exports

## Exports

`ata_AmbientSound` works from its editor and does not need exports. `ata_AmbientCreator` provides the exports below. They are used by `ata_AmbientSound`; you only need them if you build your own integration.

{% hint style="info" %}
`Render` and `Delete` only accept calls from `ata_AmbientSound`, because they write into its sound folder.
{% endhint %}

### Server exports

#### GetCatalog

Returns the available sounds and the saved custom mixes.

```lua
exports['ata_AmbientCreator']:GetCatalog(function(result)
    if result.ok then
        print(#result.data.sounds, #result.data.saved)
    end
end)
```

#### Render

Mixes 1 to 8 sounds into one seamless loop of 30 to 300 seconds.

```lua
exports['ata_AmbientCreator']:Render({
    name = 'Rainy harbor',
    duration = 60,
    layers = {
        { id = 'rain-light-rain.mp3', volume = 0.6 },
        { id = 'animals-seagulls.mp3', volume = 0.3 },
    }
}, function(result)
    -- result.ok, result.data = { id = 'creator-YYYYMMDD-xxxx.ogg', name, duration, layers, bytes, sha256, created }
end)
```

#### Delete

Deletes a saved mix (audio file and recipe).

```lua
exports['ata_AmbientCreator']:Delete('creator-YYYYMMDD-xxxx.ogg', function(result) end)
```

#### GetPeaks

Returns the waveform of a sound file as 90 values between 0 and 1. Used by the sound library for long files.

```lua
exports['ata_AmbientCreator']:GetPeaks('forest.mp3', function(result) end)
```

### Client export

#### FetchAudio

Downloads a saved mix. A mix saved after the server started is not on the resource's file server yet, so it is sent to players this way.

```lua
exports['ata_AmbientCreator']:FetchAudio('creator-YYYYMMDD-xxxx.ogg', function(result)
    -- result.ok, result.data = { mime = 'audio/ogg', base64, sha256 }
end)
```

Every callback receives `{ ok = true, data = ... }` or `{ ok = false, error = '...' }`.
