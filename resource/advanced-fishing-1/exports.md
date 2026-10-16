# Exports

### Client Exports

#### openRadio

Opens the handheld radio.

```lua
exports.ata_Radio:openRadio()
```

The same thing is available as a client event, so you can also open it from the server:

```lua
TriggerClientEvent('ata_Radio:open', source)
```

#### useRadio

Item export for the `radio` item. It opens the handheld radio.

```lua
client = { export = 'ata_Radio.useRadio' }
```

#### useEarpiece

Item export for the `earpiece` item. It opens the earpiece.

```lua
client = { export = 'ata_Radio.useEarpiece' }
```

#### useJammer

Item export for the `radio_jammer` item. It starts the jammer placement.

```lua
client = { export = 'ata_Radio.useJammer' }
```

### Server Exports

#### hasRadio

Returns `true` when the player is connected to at least one radio channel.

```lua
local connected = exports.ata_Radio:hasRadio(source)
```

| Parameter | Type   | Description          |
| --------- | ------ | -------------------- |
| `source`  | number | The player server id |
