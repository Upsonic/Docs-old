# Enabling Key Encryption: Fully Secure System

## Introduction

In Upsonic by the default you can encrypt your values with `encryption_key` but also you can enable the encryption for key.



## Enabling

You can enable the key encryption via `key_encryption`.

{% tabs %}
{% tab title="In Library" %}
```python
from upsonic import Upsonic_Cloud_Free

cloud = Upsonic_Cloud_Free(key_encryption=True)
```
{% endtab %}

{% tab title="In ENV Variables" %}
```
key_encyption=True
```
{% endtab %}
{% endtabs %}
