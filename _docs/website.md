---
layout: docs
title: Modifying Website
permalink: /docs/website/
---

This website is made with Jekyll on Github Pages. Quite neat isn't it? The big advantage is that you can modify it using github. Either directly if you have write access to the repo, or by submitting an issue.

To modify [Webpage index](https://github.com/Shufflepuck/Gala/blob/gh-pages/index.html)

### Documentation

On each documentation page, you get a link to improve the page. Follow it to edit it.

To add a documentation page, create a `.md` in `_docs/` with the correct header:

{% highlight yaml %}
---
layout: docs
title: Modifying Website
permalink: /docs/website/
---
{% endhighlight %}

Then add the documentation to the hierarchy in [_data/docs.yml](https://github.com/Shufflepuck/Gala/blob/gh-pages/_data/docs.yml)

### Posts

Simply add a post in _posts. Use [this one](https://github.com/Shufflepuck/Gala/blob/gh-pages/_posts/2015-12-10-newsite.markdown) as an example.
