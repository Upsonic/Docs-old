# CLI - New

You can use some commands from CLI for Upsonic. CLI is integrated with `.env` variables and directly giving keys.



### Connection

{% tabs %}
{% tab title="ENV Variables" %}
<pre data-title=".env"><code><strong>type="free"
</strong><strong>client_id=""
</strong><strong>
</strong><strong>database_Free="DB_database_***"
</strong>access_key_Free="ACK_***"
</code></pre>

```bash
upsonic --help
```
{% endtab %}

{% tab title="Directly with Args" %}
```bash
upsonic --client_id "" --type free --database_name "DB_database_***" --access_key "ACK_***"
```
{% endtab %}
{% endtabs %}

###

### Commands

| Usage         | Explanation           |
| ------------- | --------------------- |
| lock \<key>   | For locking the key   |
| unlock \<key> | For unlocking the key |

