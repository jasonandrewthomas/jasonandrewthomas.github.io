---
layout: post
title: "Diabetic Retinopathy AI"
date: 2018-04-30
comments: true
categories:
---

The FDA has just approved an AI diagnosis for Diabetic Retinopathy.

{% highlight python %}
from __future__ import absolute_import

import os

from celery import Celery
from django.conf import settings  # noqa

app = Celery('DumpGood')

# Using a string here means the worker will not have to
# pickle the object when using Windows.
app.config_from_object('django.conf:settings')
app.autodiscover_tasks(lambda: settings.INSTALLED_APPS)
{% endhighlight %}


