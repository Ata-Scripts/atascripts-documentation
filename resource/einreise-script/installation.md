# Installation

### Installation

1. Drop the `ata_einreise` folder into your server's resources directory
2. Add `ensure ata_einreise` to your server.cfg

* First you need `ata_core` to ensure like this

```cfg
ensure ata_core
ensure ata_einreise
```

3. Configure the `config.lua` file to match your server's needs
4. Set up your Discord webhooks in `server/discord.lua`
5. Restart your server
