---
layout: post
title:  "Creating a Java project with the archetype Maven plugin"
date:   2015-03-25 21:42:10
categories: jekyll update
---

Creating a project form an archetype involves three steps:

1. the selection of the archetype
2. the configuration of that archetype
3. the effective creation of the project from the collected information.

For example, issuing the following command we will create a java project based on the maven-archetype-quickstart (A Java projecct with a junit library dependency setup).
{% highlight bash %}
	$ mvn archetype:generate -DgroupId=com.java.demo -DartifactId=JavaProjectDemo -DarcetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false 
{% endhighlight %}

Then, if you use Eclipse, you will probably want to convert to an eclipse project with the following command:
{% highlight bash %}
	$ mvn eclipse:eclipse
{% endhighlight %}

Finally, you can import the project in your Eclipse workspace.

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
