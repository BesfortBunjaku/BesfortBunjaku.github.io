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

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}