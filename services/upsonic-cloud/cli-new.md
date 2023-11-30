# CLI - New

You can use some commands from CLI for Upsonic. CLI is integrated with `.env` variables and directly giving keys.



### Connection

{% tabs %}
{% tab title="ENV Variables" %}
{% code title=".env" %}
```
database_Free="DB_database_***"
access_key_Free="ACK_***"
```
{% endcode %}

```bash
upsonic --type free
```
{% endtab %}

{% tab title="Directly with Args" %}
```bash
upsonic --type free --database_name "DB_database_***" --access_key "ACK_***"
```
{% endtab %}
{% endtabs %}

###

### Commands

| Usage         | Explanation           |
| ------------- | --------------------- |
| lock \<key>   | For locking the key   |
| unlock \<key> | For unlocking the key |

