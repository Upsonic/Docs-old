# ✨ Connect

{% hint style="info" %}
**For connecting you must get your Database and Cloud Access Key from** [**here**](https://app.upsonic.co/cloud)**.**
{% endhint %}



### Requirements

* Database Key
* Cloud Access Key

### Connection Code

{% tabs %}
{% tab title="Free" %}
```python
from upsonic import Upsonic_Cloud_Free
cloud = Upsonic_Cloud_Free("YOUR_DATABASE_KEY", "YOUR_CLOUD_ACCESS_KEY")

# Other codes
```
{% endtab %}

{% tab title="Pro" %}
```python
from upsonic import Upsonic_Cloud_Pro
cloud = Upsonic_Cloud_Pro("YOUR_DATABASE_KEY", "YOUR_CLOUD_ACCESS_KEY")

# Other codes
```
{% endtab %}

{% tab title="Premium" %}
```python
from upsonic import Upsonic_Cloud_Premium
cloud = Upsonic_Cloud_Premium("YOUR_DATABASE_KEY", "YOUR_CLOUD_ACCESS_KEY")

# Other codes
```
{% endtab %}
{% endtabs %}
