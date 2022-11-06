---
layout: post
title:  "How to use Docker Images offline"
date:   2022-11-05 07:50:27 -0500
categories: 
---
Are you looking for a way to save a docker image to a flash drive or take to an on-premises environment? 

Create a folder for where you are going to save your docker image.

{% highlight console %}
mkdir docker
{% endhighlight %}

Enter Folder

{% highlight console %}
cd docker
{% endhighlight %}

Make sure you have an image from the docker repository of your choice


{% highlight console %}
docker pull python:3.11-rc-alpine
{% endhighlight %}

{% highlight console %}
docker images
{% endhighlight %}


{% highlight console %}
docker save python:3.11-rc-alpine python_3.11_rc_alpine.tar
{% endhighlight %}



[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
