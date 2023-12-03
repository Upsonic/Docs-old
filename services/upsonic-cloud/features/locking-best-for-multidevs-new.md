# Locking: Best for Multidevs - New

## Introduction

In Upsonic Cloud by the principle we are setting the latest one of the requests but you can add an barrier for disabling settings from others in client side.



<img src="../../../.gitbook/assets/file.excalidraw (1).svg" alt="" class="gitbook-drawing">

## Enabling

You can enable the locking via  `locking` usage in env and directly from library. The people in your team should enable the locking for preventing any **overwrite** situation.

{% tabs %}
{% tab title="In Library" %}
```python
from upsonic import Upsonic_Cloud_Free

cloud = Upsonic_Cloud_Free(locking=True)
```
{% endtab %}

{% tab title="In ENV Variables" %}
```
locking = True
```
{% endtab %}
{% endtabs %}



## Actions

### Locking and Unlocking

{% tabs %}
{% tab title="CLI" %}
```bash
upsonic --type free lock my_function
```
{% endtab %}

{% tab title="In Library" %}
```python
cloud.lock("my_function
```
{% endtab %}
{% endtabs %}

### Unlocking

{% tabs %}
{% tab title="CLI" %}
```
upsonic --type free unlock my_function
```
{% endtab %}

{% tab title="In Library" %}
```
cloud.unlock("my_function")
```
{% endtab %}
{% endtabs %}

## Result

When you locked the systems the other users will see an error when they want to set the key. Locking uses 1 more key for each key.  So you should care about this.
