---
title: "Django: Django Middleware"
header:
  image: assets/images/userinfomiddleware.png
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
tags:
  - table of contents
toc: true
toc_label: "Django Middleware"
toc_icon: "heart"
---
## What is a Middleware?
Middleware is code (usually a class) that is executed during request response circle.
Django commes with predefined Middleware (default) list, some of them are:

  ![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/settingsmiddleware.png)
{: .image-left}

* SecurityMiddleware
* SessionMiddleware
* AuthenticationMiddleware
* CsrfViewMiddleware

**Costume Middleware!** We can make our owen costume middleware and include in django settings middleware list. (refer to project bello)
{: .notice}

## What is the use of Middlewares?
Middlewares are used to:

* `Filter or Gathering Data`:
  Ex. filtering user data.."describe the project bello"

* `Securety`:
  Middleware can respond directly without hitting the view.This type of future makes django very powerfully,because we protect our system from any malision request that can harm our system.
  
  ![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/middleware2.png)
{: .image-left}

* `Logging`:
  

## How to create a costume Middleware?

`Step1 :`

  ![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/middlemod.png)
{: .image-left}

First we create a python file inside any app called `middleware.py`,this could be called anything.

`Step2 :`

We create a class inside `middleware.py` module.
Tow methods are required from django to be included inside this class:

```python
class UserInfoMiddleware:
    def __init__(self, get_response):
        self.get_response = get_response
        # One-time configuration and initialization.

    def __call__(self, request):
        # Code to be executed for each request before the view (and later middleware) are called.
        print("Hi..")

        response = self.get_response(request)

        # Code to be executed for each request/response after the view is called.

        return response
```

* `__init__(self, get_response)`
* `__call__(self, request)-> response`

other methods are optional.
There are five optional methods that we can include in middleware class:

Those tow methods are called during request process, before getting to the view.

* `process_request(self, request)`
* `process_view(self, request, view_func, view_args, view_kwargs)`



`Step3 :` 

We include or register our costume middleware in django settings middleware section.


**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}