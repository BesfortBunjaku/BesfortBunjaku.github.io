---
title: "Django: Django validators"
header:
  image: assets/images/git.png
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
tags:
  - table of contents
toc: true
toc_label: "Git Tutorial"
toc_icon: "heart"
---
## Built-in Validation?
As per the Django documentation, there are some built-in validators:
```python
  from django.core.validators import validate_slug, validate_email
  from django.db import models

  SlugField = models.CharField(validators=[validate_slug])
  EmailField = models.CharField(validators=[validate_email])

  
```
## The Reusable Method?
Writing custom validators is often the best way to have uniform validation throughout your project. So let's create our own validators using the above example.
```python
  # yourapp.validators.py

  from django.core.exceptions import ValidationError

  def validate_domainonly_email(value):
      """
      Let's validate the email passed is in the domain "yourdomain.com"
      """
      if not "yourdomain.com" in value:
          raise ValidationError(_"Sorry, the email submitted is invalid. All emails have to be registered on this domain only.", status='invalid')



```
Now we're talking. This new method validate_domainonly_email is perfect to be used anywhere on our project. It will accomplish field-level validation wherever we use it.
The nice thing is we can reuse this validator in any field including Model fields, Form fields, and even DRF serializers.

```python
#anotherapp.models.py 
from django.db import models
from yourapp.validators import validate_domainonly_email


class NewProjectSubmission(models.Model):
    email = models.EmailField(validators=[validate_domainonly_email])


```
Or in a Django Rest Framework serializer:

```python
#anotherapp.serializers.py 

from rest_framework import serializers
from yourapp.validators import validate_domainonly_email

class CommentSerializer(serializers.Serializer): # or serializers.ModelSerializer
    email = serializers.EmailField(validators=[validate_domainonly_email])
    content = serializers.CharField(max_length=200)
    created = serializers.DateTimeField()



```

## Even further... a custom Field!
To maximize reusability, you might consider even creating a custom Django Field, specifically for this validator. It's all going to depend on your project and what you need to validate.

```python
from django.core.validators import validate_slug, validate_email
from django.db import models

from yourapp.validators import validate_domainonly_email


class DomainEmailField(models.CharField):
    description = "An email field specific to our domain."

    def __init__(self, *args, **kwargs):
        kwargs['max_length'] = 120
        kwargs['validators'] = [validate_email, validate_domainonly_email]
        super(DomainEmailField, self).__init__(*args, **kwargs)
```
## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}