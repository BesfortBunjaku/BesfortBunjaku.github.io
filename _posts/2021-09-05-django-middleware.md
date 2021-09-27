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
Middleware is code (usually class) that is executed during request response circle.
Django commes with predefined Middleware list, some of them are:

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

* `Filter Data`:
  Ex. filtering user data.."describe the project bello"

* `Securety`:
  ![Smithsonian Image]({{ site.url }}{{ site.baseurl }}/assets/images/middleware2.png)
{: .image-left}

* `Logging`:
  

## How to create an costume Middleware?

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}