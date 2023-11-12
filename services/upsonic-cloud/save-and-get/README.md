# ⬆ Save & Get

## Before Start

With Upsonic Cloud you will be save anything in python to Cloud, but we are developing our systems and please inform us in any error situations via dashboard help section.





## Save

The whole save system are working with <mark style="color:blue;">`cloud.save`</mark> method and you can use in any type with key and value (Any definition in python). But we have a special method for class and function saving via Python Decorations and its <mark style="color:blue;">`@cloud.active`</mark> . Also you can easily use Encryption with this commands. Lastly we have some other decorators for improving your situations.

### Function

```python
# Connection Code Above

@cloud.active
def my_awesome_function():
    print("Hello world")

```

It's Equal to <mark style="color:purple;">`cloud.set("my_awesome_function", my_awesome_function)`</mark>. After these implementations you should run the code and its will automatically upload to Upsonic Cloud with the function name or your special name (Just via cloud.set uses).

