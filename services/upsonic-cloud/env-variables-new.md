# ENV Variables - New

You can easily set your database and access key via environment variables that placed on `.env` file.

{% code title="my_app/.env" %}
```
database_Free="DB_database_***"
access_key_Free="ACK_***"

database_Pro="DB_database_***"
access_key_Pro="ACK_***"

database_Premium="DB_database_***"
access_key_Premium="ACK_***"


database_Startup="DB_database_***"
access_key_Startup="ACK_***"

locking=False

```
{% endcode %}



After these settings you can use just interfaces via;

{% code title="my_app/main.py" %}
```python
from upsonic import Upconic_Cloud_Free
cloud = Upconic_Cloud_Free()
```
{% endcode %}
