# update.py: All is your need



## Introduction

This is an generic updating culture file for your applications. With this you can easily manage your applications CD in one file. General idea is defining the sending type to cloud and using Upsonic Update interface.

{% code title="File Tree" %}
```
- My_App
    - src
        - __init__.py
        - algorithms.py
    .env
    - update.py
```
{% endcode %}

{% tabs %}
{% tab title="src/algorithms.py" %}
```python
def my_algorithm():
    return 1+2

```
{% endtab %}

{% tab title="src/__init__.py" %}
```python
from .algorithms import *

```
{% endtab %}
{% endtabs %}

## Saving All Modules - Suggested

{% code title="update.py" %}
```python
from upsonic import Upsonic_Cloud_Free
cloud = Upsonic_Cloud_Free(cache=False)
from upsonic_update import Upsonic_Update
update = Upsonic_Update(cloud, pre_update_all=True, clear_olds=True)
# --------- DONT CONFIGURE ABOVE THIS LINE ---------


import src

cloud.active_module(src)


# --------- DONT CONFIGURE BELOW THIS LINE ---------
update.update()
```
{% endcode %}

#### Result

{% code title="console" %}
```
[18:46:09] [DB_De*] Upsonic Cloud initializing...
           [DB_De*] Upsonic Cloud active                    
           ---------------------------------------------
[18:46:11]                                                                 
            Update Started
                                                   
            Updating: ['src.algorithms.my_algorithm']
            ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[18:46:12]  Update took 1s              
              
            Updating Complated Without any Error
        
```
{% endcode %}

Now you can access your function via&#x20;

{% code title="anywhere.py" %}
```python
cloud.get("src.algorithms.my_algorithm")
```
{% endcode %}

##

***



## Saving Just Some Function

In this way you can easily set some functions to your cloud and get by the full module names. With this you dont need to break your systems.

{% code title="update.py" %}
```python
from upsonic import Upsonic_Cloud_Free
cloud = Upsonic_Cloud_Free(cache=False)
from upsonic_update import Upsonic_Update
update = Upsonic_Update(cloud, pre_update_all=True, clear_olds=True)
# --------- DONT CONFIGURE ABOVE THIS LINE ---------


import src

cloud.active(src.algorithms.my_algorithm)


# --------- DONT CONFIGURE BELOW THIS LINE ---------
update.update()
```
{% endcode %}

#### Result

{% code title="console" %}
```
[18:46:09] [DB_De*] Upsonic Cloud initializing...
           [DB_De*] Upsonic Cloud active                    
           ---------------------------------------------
[18:46:11]                                                                 
            Update Started
                                                   
            Updating: ['src.algorithms.my_algorithm']
            ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[18:46:12]  Update took 1s              
              
            Updating Complated Without any Error
        
```
{% endcode %}

Now you can access your function via&#x20;

{% code title="" %}
```python
cloud.get("src.algorithms.my_algorithm")
```
{% endcode %}

##
