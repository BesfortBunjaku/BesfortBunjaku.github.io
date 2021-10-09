---
title: "Functions: Higher Order Functions"
header:
  image: assets/images/userinfomiddleware.png
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
tags:
  - table of contents
toc: true
toc_label: "Higher Order Functions"
toc_icon: "heart"
---
## What is a Higher Order Functions?
Higher Order Functions is a function that accepts another function as argument. The function that passed as argument is called `callback function`.


```python
def callback_function(x):
    y = x + 2
    return y

def higher_order_function(lst , callback_function):
    return [callback_function(item) for item in lst]
```

examples of higher order functions in python are:

* map
* filter
* reduce


**Costume Middleware!** We can make our owen costume middleware and include in django settings middleware list. (refer to project bello)
{: .notice}


