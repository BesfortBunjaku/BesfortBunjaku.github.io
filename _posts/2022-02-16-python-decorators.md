---
title: "Python: Decorators"
header:
  image: assets/images/userinfomiddleware.png
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
tags:
  - table of contents
toc: true
toc_label: "Python Decorators"
toc_icon: "heart"
---
## What is a Decorator in python?
Decorator is a design pattern that allows you to modify the behavior of a function or method,without actually changing its implementation.


```python
def decorator_function(original_function):
    def wrapper_function(*args, **kwargs):
        print('wrapper executed this before {}'.format(original_function.__name__))
        return original_function(*args, **kwargs)
    return wrapper_function
```

examples of higher order functions in python are:

* [map](https://besfortbunjaku.github.io/django-validators/)
* filter
* reduce


**Costume Middleware!** We can make our owen costume middleware and include in django settings middleware list. (refer to project bello)
{: .notice}

German:

## What is a Decorator in python?

Decorator is ein designpattern, der es ermöglicht, die Funktion oder Methode zu verändern, ohne die Implementierung zu ändern.


