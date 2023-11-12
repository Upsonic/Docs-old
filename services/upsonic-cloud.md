# ☁ Upsonic Cloud

## Introduction

Upsonic Cloud is an infrastructure that provides an wide accessibility for our services. The background of Cloud is an key value database and its easily serialize any data in python and after its upload to an key in your special Database. These databases are different folders and the keys are different files. With this we can provide an stable infrastructure for your every data. With these features you can easily send you functions, classes, objects and variables easily.



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

Now you don't need to cloud.set . You just need to run these script and its will automaticaly save with <mark style="color:blue;">"my\_awesome\_function"</mark> key to cloud.

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





