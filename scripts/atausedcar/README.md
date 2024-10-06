# ataUsedCar

[**Youtube Preview**](https://youtu.be/prCPsodo14U?si=mVxHEUW2h4gr5fAI)

#### Execute the following SQL code in your database:

<pre class="language-sql"><code class="lang-sql"><strong>CREATE TABLE IF NOT EXISTS `ata_carmarket` (
</strong>  `id` int(11) NOT NULL AUTO_INCREMENT,
  `ad_data` longtext DEFAULT NULL,
  `expired` int(11) NOT NULL,
  `created` int(11) NOT NULL,
  `vehicle_data` longtext DEFAULT NULL,
  `plate` varchar(12) NOT NULL,
  `owner` varchar(46) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=49 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;
</code></pre>

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
