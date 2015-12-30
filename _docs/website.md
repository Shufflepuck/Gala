---
layout: docs
title: Modifying Website
permalink: /docs/website/
---

This website is made with Jekyll on Github Pages. Quite neat isn't it? The big advantage is that you can modify it using Github. Either directly if you have write access to the repo, or by submitting a pull request.

All pages are hosted on our repository, in the [gh-pages branch](https://github.com/Shufflepuck/Gala/tree/gh-pages).
For example, to modify the webpage index you would modify the following file: [webpage index](https://github.com/Shufflepuck/Gala/blob/gh-pages/index.html).

### Documentation

On each documentation page, you get a link to improve the page. Follow it to edit it.

To add a documentation page, create a new file ending with the `.md` file extension in `_docs/`. Make sure and add the correct yaml header (shown below):

{% highlight yaml %}
---
layout: docs
title: Modifying Website
permalink: /docs/website/
---
{% endhighlight %}

Then add the documentation to the hierarchy in [_data/docs.yml](https://github.com/Shufflepuck/Gala/blob/gh-pages/_data/docs.yml)

### Posts

Simply add a post in `_posts`. Use [this one](https://github.com/Shufflepuck/Gala/blob/gh-pages/_posts/2015-12-10-newsite.markdown) as an example.
