# ✨ Connect

{% hint style="info" %}
**For connecting you must get your Database and Cloud Access Key from** [**here**](https://app.upsonic.co/cloud)**.**
{% endhint %}

## Install

You can easily install the Upsonic with [PyPI](https://pypi.org/project/upsonic/).

<details>

<summary>Requirements</summary>

* Python >= 3.5
* pip3
* Any Modern OS
  * Linux
  * MacOS
  * Windows
  * Android
  * iOS

</details>

### Installation Command

It's the cross-platform and stable download command for every system.

<pre data-title="Console" data-full-width="false"><code><strong>pip3 install Upsonic
</strong></code></pre>

## Connect

<details>

<summary>Requirements</summary>

* Database Key
* Cloud Access Key

</details>

### Connection Code

{% tabs %}
{% tab title="Free" %}
{% code title="Python" %}
```python
from upsonic import Upsonic_Cloud_Free
cloud = Upsonic_Cloud_Free("YOUR_DATABASE_KEY", "YOUR_CLOUD_ACCESS_KEY")

# Other codes
```
{% endcode %}
{% endtab %}

{% tab title="Pro" %}
{% code title="Python" %}
```python
from upsonic import Upsonic_Cloud_Pro
cloud = Upsonic_Cloud_Pro("YOUR_DATABASE_KEY", "YOUR_CLOUD_ACCESS_KEY")

# Other codes
```
{% endcode %}
{% endtab %}

{% tab title="Premium" %}
{% code title="Python" %}
```python
from upsonic import Upsonic_Cloud_Premium
cloud = Upsonic_Cloud_Premium("YOUR_DATABASE_KEY", "YOUR_CLOUD_ACCESS_KEY")

# Other codes
```
{% endcode %}
{% endtab %}
{% endtabs %}
