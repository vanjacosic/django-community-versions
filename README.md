# Community versions for Django

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

A screenshot of how the badge looks:

<img src="https://cldup.com/BNws4708xH.png" title="Example of the Django version badge" width="183" height="27"> 


## Updating a badge

Badges are stored as Jekyll posts. For example, the badge for this blog post:

* "Community versions for Django" [http://vanjacosic.com/community-versions-for-django/](http://vanjacosic.com/community-versions-for-django/)

Is stored at:

* [\_posts/2015-08-25-community-versions-for-django.md](https://github.com/vanjacosic/django-community-versions/blob/gh-pages/_posts/2015-08-25-community-versions-for-django.md)

Versioning informations is store in the YAML front-matter of that post:

```
---
layout: post
url: http://vanjacosic.com/community-versions-for-django/
title: "Community versions for Django"
date: 2015-08-25
start_version: 1.6
end_version: 1.8
---
```

To update the badge (as seen in the blog post), open a PR changing the YAML content.

## Creating a badge

To create and embed a badge, first author a Jekyll post with the version
information as exists. Most badges are likely to be for current content, and
thus may only have a `start_version` property.

To embed your badge, use the filename to determine the badge URL. For example
this filename:

```
_posts/2015-08-25-community-versions-for-django.md
```

Is used as a badge with the following markup:

```html
<iframe
  width="178" height="24" style="border:0px"
  src="http://vanjacosic.github.io/django-community-versions/2015/08/25/community-versions-for-django.html">
</iframe>
```

Please help ensure your own blog posts are correctly flagged by add a badge
when you publish.

Linking to a URL that does not exist, such as before your
PR with the new badge is merged, will simply result in a blank space. As
soon as the PR is merged and GitHub pages updates, the badge will appear.
