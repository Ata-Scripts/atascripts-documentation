# ataGoPostal

#### Execute the following SQL code in your database:

{% tabs %}
{% tab title="ESX" %}
```sql
ALTER TABLE `users` ADD COLUMN `ataPostal` LONGTEXT NULL;
```
{% endtab %}

{% tab title="QB" %}
```sql
ALTER TABLE `players` ADD COLUMN `ataPostal` LONGTEXT NUL
```
{% endtab %}
{% endtabs %}

### Also You Can Translate All Ui And All Texts&#x20;

```lua
Locales['en'] = {
    -- Name
    ['name'] = 'go Postal',
    ['Open_Menu'] = 'open menu with ~INPUT_CONTEXT~.',
    ['Change_Cloth'] = 'change cloth ~INPUT_CONTEXT~ .',
    ['Exit_job'] = 'for exit job ~INPUT_CONTEXT~ .',
}
```

###

### Server artifacts

Make sure your server artifacts version is above the **5181**.

* Windows: [https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/](https://runtime.fivem.net/artifacts/fivem/build\_server\_windows/master/)
* Linux: [https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/](https://runtime.fivem.net/artifacts/fivem/build\_proot\_linux/master/)
