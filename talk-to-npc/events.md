# Events

#### Client Events

| Event                        | Description                |
| ---------------------------- | -------------------------- |
| `ata_talktonpc:addChat`      | Add message to chat        |
| `ata_talktonpc:buyItems`     | Open buy menu              |
| `ata_talktonpc:sellItems`    | Open sell menu             |
| `ata_talktonpc:interact`     | Start interaction with NPC |
| `ata_talktonpc:closeUI`      | Close dialogue UI          |
| `ata_talktonpc:notification` | Display notification       |

#### Server Events

| Event               | Description                 |
| ------------------- | --------------------------- |
| `buyitemsCash`      | Buy items with cash         |
| `buyitemsBank`      | Buy items with bank money   |
| `sellitemsCash`     | Sell items for cash         |
| `sellitemsBank`     | Sell items for bank deposit |
| `getInventoryItems` | Get player inventory list   |

### Custom Events

You can create custom events to extend functionality:

```lua
RegisterNetEvent('custom:event')
AddEventHandler('custom:event', function()
    TriggerEvent('ata_talktonpc:addChat', "text", 'Message text')
    Wait(1000)
    -- Custom code
    TriggerEvent('ata_talktonpc:closeUI')
end)
```
