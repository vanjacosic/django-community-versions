---
layout: page
title: Community Versioning for Django Content
---

Web content never expires. A blog post written in 2011 will live on in search
engine results for years.

[Django](https://www.djangoproject.com/) has undergone a _lot_ of change over the last
few years, sometimes in backwards incompatible ways. This means the Internet is
littered with content and posts that were accurate at the time, but have since
been obsoleted.

To ensure old content gets properly flagged, with no effort needed by the
author, we've created a GitHub-driven badge service. See
[the user-friendly website](http://vanjacosic.github.io/django-community-versions/)
for more details on the general idea.

## Example

This is an example of the badge:

<iframe width="178" height="24" style="border:0px" src="http://vanjacosic.github.io/django-community-versions/2015/08/25/community-versions-for-django.html"></iframe>


## Updating a badge

Badges are stored as Jekyll posts. For example, the badge for this blog post:

* "Community versions for Django" - [http://vanjacosic.com/community-versions-for-django/](http://vanjacosic.com/community-versions-for-django/)

Is stored at:

* [\_posts/2015-08-25-community-versions-for-django.md](https://github.com/vanjacosic/django-community-versions/blob/gh-pages/_posts/2015-08-25-community-versions-for-django.md)

Versioning informations is store in the YAML front-matter of that post:

{% highlight yaml %}
---
layout: post
url: http://vanjacosic.com/community-versions-for-django/
title: "Community versions for Django"
date: 2015-08-25
start_version: 1.6
end_version: 1.8
---
{% endhighlight %}

To update the badge (as seen in the blog post), open a PR changing the YAML content.
