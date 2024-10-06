# ataGarage

[**Youtube Preview**](https://youtu.be/Etw\_R0gLpL8)

#### Execute the following SQL code in your database:

```sql
ALTER TABLE owned_vehicles ADD COLUMN IF NOT EXISTS stored tinyint(1) NOT NULL DEFAULT 1;
ALTER TABLE owned_vehicles ADD COLUMN IF NOT EXISTS damage  longtext NULL DEFAULT NULL;
ALTER TABLE owned_vehicles ADD COLUMN IF NOT EXISTS body_damage varchar(50) NOT NULL DEFAULT '1000';
ALTER TABLE owned_vehicles ADD COLUMN IF NOT EXISTS parking varchar(50) NULL DEFAULT NULL;
ALTER TABLE owned_vehicles ADD COLUMN IF NOT EXISTS engine_damage varchar(50) DEFAULT '1000';
ALTER TABLE owned_vehicles ADD COLUMN IF NOT EXISTS job varchar(50) NOT NULL DEFAULT 'civ';;
```

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
