# ☁ Upsonic Cloud

## Introduction

Upsonic Cloud is an infrastructure that provides an wide accessibility for our services. The background of Cloud is an key value database and its easily serialize any data in python and after its upload to an key in your special Database. These databases are different folders and the keys are different files. With this we can provide an stable infrastructure for your every data. With these features you can easily send you functions, classes, objects and variables easily.



<img src="../../.gitbook/assets/file.excalidraw (2).svg" alt="" class="gitbook-drawing">

## Before Start

With Upsonic Cloud you will be save anything in python to Cloud, but we are developing our systems and please inform us in any error situations via dashboard help section.



## Save

The whole save system are working with <mark style="color:blue;">`cloud.save`</mark> method and you can use in any type with key and value (Any definition in python). But we have a special method for class and function saving via Python Decorations and its <mark style="color:blue;">`@cloud.active`</mark> . Also you can easily use Encryption with this commands. Lastly we have some other decorators for improving your situations.

### Function

```python

def my_awesome_function():
    print("Hello world")


cloud.set("my_awesome_function", my_awesome_function)

```

After this implementations you should run the code and its will upload to Upsonic Cloud with the "my\_awesome\_function" key.

#### Decorators

<details>

<summary><mark style="color:blue;"><code>@cloud.active</code></mark> Fast cloud.set that automaticaly retrive the name of function</summary>

With this decorator you don't need to use `cloud.set` its an shortcut for saving functions to cloud.



<pre class="language-python"><code class="lang-python"><strong>
</strong>@cloud.active
def my_awesome_function():
    print("Hello world")

</code></pre>

Now you don't need to cloud.set . You just need to run this script and its will automaticaly save with <mark style="color:blue;">"my\_awesome\_function"</mark> key to cloud.

</details>

***

<details>

<summary><mark style="color:purple;"><code>@requires("flask")</code></mark> Add an requirement and install automaticaly</summary>

It's automaticaly check the flask installation and if its not exist the system its automaticaly install via pip when the function calls.

```python
from upsonic import requires

@cloud.active
@requires("flask")
@requires("django==4.2.6")
def my_awesome_function():
    import flask
    import django
    print("Hello world")

```

</details>

<details>

<summary><mark style="color:purple;"><code>@no_exception</code></mark> Add an barrier to prevent exception</summary>

It's add an barrier to your function that runs before the main code. Its add an try-except and with this your runtime never get down.

```python
from upsonic import no_exception

@cloud.active
@no_exception
def my_awesome_function():
    raise Exception()

```

</details>



### Class

```python

class my_class:
    def __init__(self, age):
        self.age = age
        
cloud.set("my_class", my_class)

```

With this code you can easily set `my_class` to <mark style="color:blue;">"my\_class"</mark> key.

#### Decorators

<details>

<summary><mark style="color:blue;"><code>@cloud.active</code></mark> Fast cloud.set that automaticaly retrive the name of class</summary>

With this decorator you don't need to use `cloud.set` its an shortcut for saving functions to cloud.



<pre class="language-python"><code class="lang-python"><strong>
</strong>@cloud.active
class my_class:
    def __init__(self, age):
        self.age = age

</code></pre>

Now you don't need to cloud.set . You just need to run this script and its will automaticaly save with <mark style="color:blue;">"my\_class"</mark> key to cloud.

</details>

***

<details>

<summary><mark style="color:purple;"><code>@requires("flask")</code></mark> Add an requirement and install automaticaly</summary>

It's automaticaly check the flask installation and if its not exist the system its automaticaly install via pip when the class calls.

```python
from upsonic import requires

@cloud.active
@requires("flask")
@requires("django==4.2.6")
class my_class:
    def __init__(self, age):
        import flask
        import django
        self.age = age
```

</details>



### Object

```python

class my_class:
    def __init__(self, age):
        self.age = age
  
my_object = my_class(15) 
        
cloud.set("my_object", my_object)

```

With this code you can easily set `my_object` to <mark style="color:blue;">"my\_object"</mark> key.

### Variable

```python
my_string = "Hello"
my_integer = 13412
my_float = 1234.15

my_dictionary {"hello":"world"}
my_list = [my_string, mr_integer, my_float, my_dictionary]
my_tuple = (my_dictionary, my_list)


cloud.set("my_tuple", my_tuple)

```

With this code you can easily set `my_tuple` to <mark style="color:blue;">"my\_tuple"</mark> key.



### Module

```python
import random

cloud.active_module(random)

cloud. Get("random.Random")().random() # == random.random()

```

With this way you can easily make accessible your modules in Upsonic Cloud. Example of the set keys is <mark style="color:blue;">"random.Random"</mark> .

## Get

In getting we have a <mark style="color:blue;">`cloud.get`</mark> function and you can retrive anything in the cloud with this.

```python
cloud.get("my_awesome_function")()
cloud.get("my_class")(15)
cloud.get("my_tuple")
```





## Encryption

You can easily encrypt your datas before to send Upsonic Cloud. With this way no body will able to read your datas. for this you should use an <mark style="color:purple;">string</mark> via <mark style="color:blue;">`encryption_key`</mark> parameter in `cloud.set` and `cloud.get` and `cloud.active`.

```python
cloud.set("key", "value", encryption_key="YOUR_ENCRYPTION_KEY")

cloud.get("key", encryption_key="YOUR_ENCRYPTION_KEY")

@cloud.active(encryption_key="YOUR_ENCRYPTION_KEY")
def a_function():
    pass
```
