---
layout: post
title:  "Changing an existing linux symlink"
date:   2015-03-25 21:42:10
categories: jekyll update
---

I already had ruby version 1.9.1 installed on my system when I installed the ruby2.0 package. But after installing the newer version, to my surprise the symlinks where pointing to the older version. So ruby, irb and gem commands were in the wrong version.

{% highlight bash %}
$ ls -la /usr/bin/ruby
lrwxrwxrwx 1 root root 16 Mar 25 21:35 /usr/bin/ruby -> /usr/bin/ruby1.9.1
{% endhighlight %}

So to change the symlink to point to the newer ruby version, without recreating the symlink, you can run the following command:
{% highlight bash %}
	ln -f -s /usr/bin/ruby2.0 /usr/bin/ruby 
{% endhighlight %}

And this result in:
{% highlight bash %}
$ ls -la /usr/bin/ruby
lrwxrwxrwx 1 root root 16 Mar 25 21:35 /usr/bin/ruby -> /usr/bin/ruby2.0
{% endhighlight %}

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
