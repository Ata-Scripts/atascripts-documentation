# ataCoinShop

[**Youtube Preview**](https://youtu.be/M3DEKzjt\_6Q)

#### Execute the following SQL code in your database (sql):

```sql
ALTER TABLE `users` 
ADD COLUMN `coinVIP` int(11) DEFAULT 0;

CREATE TABLE IF NOT EXISTS `ata_coin_code` (
  `code` varchar(50) NOT NULL,
  `amount` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;
```

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
