# Version Control: Set your app version to your systems and make rollbacks in seconds

## Introduction

In Upsonic you can easily make version control for you applications and you can manage the active version on your clients easily.



<img src="../../../.gitbook/assets/file.excalidraw (4).svg" alt="" class="gitbook-drawing">

## Enabling

You can enable the version control via `version` and also you can enable the `client_version` after setting and client\_id.



{% tabs %}
{% tab title="In Library" %}
```python
from upsonic import Upsonic_Cloud_Free

cloud = Upsonic_Cloud_Free(version=True)
```

```python
from upsonic import Upsonic_Cloud_Free

cloud = Upsonic_Cloud_Free(
        ..., 
        client_id="my_machine", 
        version=True, 
        client_version=True
        )
```
{% endtab %}

{% tab title="In ENV Variables" %}
```
version=True
```

```
client_id="my_machine"
version=True
client_version=True
```
{% endtab %}
{% endtabs %}





## Actions

### Tagging the Release

After version setting you should set your functions.

{% tabs %}
{% tab title="CLI" %}
<pre><code><strong>upsonic set_set_version 0.1.0
</strong></code></pre>
{% endtab %}

{% tab title="In Library" %}
<pre class="language-python"><code class="lang-python"><strong>cloud.set_set_version("0.1.0")
</strong></code></pre>
{% endtab %}
{% endtabs %}

<details>

<summary>Setting a Client Working Version Remotely</summary>

If you want you can easily update your client working version release.

{% code title="Bash" %}
```
upsonic set_set_version 0.1.0 -c = "my_developer_1"
```
{% endcode %}

or

<pre class="language-python" data-title="Python"><code class="lang-python"><strong>cloud.set_set_version("0.1.0", client_id="my_developer_1")
</strong></code></pre>

</details>

### Deploy

{% tabs %}
{% tab title="CLI" %}
```
upsonic set_get_version 0.1.0
```

Or you can update the version for an client

```
upsonic set_get_version 0.1.0 -c = "my_machine"
```
{% endtab %}

{% tab title="In Library" %}
```python
cloud.set_get_version("0.1.0")
```

Or you can update the version for an client

```python
cloud.set_get_version("0.1.0", client_id="my_machine")
```
{% endtab %}
{% endtabs %}
