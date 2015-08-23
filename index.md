---
layout: page
title: Community Versioning for Rust Content
---

Web content never expires. A blog post written in 2011 will live on in search
engine results for years.

[Rust](http://www.rust-lang.org/) has undergone a _lot_ of change over the last
few years, often in completely incompatible ways. This means the Internet is
littered with content and posts that were accurate at the time, but have since
been obsoleted.

To ensure old content gets properly flagged, with no effort needed by the
author, we've created a GitHub-driven badge service. See
[the user-friendly website](http://steveklabnik.github.io/rust-community-versions/)
for more details on the general idea.

## Updating a badge

Badges are stored as Jekyll posts. For example, the badge for this blog post:

* "Pointers in Rust: a Guide" [http://words.steveklabnik.com/pointers-in-rust-a-guide](http://words.steveklabnik.com/pointers-in-rust-a-guide)

Is stored at:

* [\_posts/2013-10-18-pointers-in-rust-a-guide.md](http://steveklabnik.github.io/rust-community-versions/_posts/2013-10-18-pointers-in-rust-a-guide.md)

Versioning informations is store in the YAML front-matter of that post:

{% highlight yaml %}
---
layout: post
url: http://words.steveklabnik.com/pointers-in-rust-a-guide
title: "Pointers in Rust: a Guide"
date: 2013-10-18
start_version: 0.8
---
{% endhighlight %}

To update the badge (as seen the blog post at words.steveklabnik.com), open a PR changing
the YAML front-matter.
