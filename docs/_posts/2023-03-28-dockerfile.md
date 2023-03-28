---
layout: post
title:  "How to create a Docker Container from a Dockerfile"
date:   2023-03-28 13:30:27 -0500
image: assets/images/docker.png
categories: docker
---

![]({{ page.image | relative_url }})

## Creating a Pylogix container from a Dockerfile

Dockerfiles provide a powerful way to create and manage images that can be used to run applications. In this tutorial, we will show you how to create a Dockerfile from a Python 3.12-slim-bullseye Docker image and install PyLogix.

Prerequisites:

Docker installed on your machine

### Step 1 - Pull the Python 3.12-slim-bullseye Docker Image

First, we need to pull the Python 3.12-slim-bullseye Docker image from the Docker Hub. To do this, run the following command in your terminal:

{% highlight console %}
docker pull python:3.12.0a6-slim-bullseye
{% endhighlight %}

### Step 2 - Create the Dockerfile

Now that we have the Python 3.12-slim-bullseye Docker image, we can create a Dockerfile. To do this, create a file named 
Dockerfile in the same directory as your project files.

In the 
Dockerfile
, we will add the following lines:

{% highlight console %}
FROM python:3.12-slim-bullseye

RUN pip install pylogix

{% endhighlight %}


This tells Docker to use the Python 3.12-slim-bullseye image as the base image and to install PyLogix using the pip  command.

### Step 3 - Build the Docker Image

Now that we have created the Dockerfile, we can build the Docker image. To do this, run the following command in your terminal:

{% highlight console %}
docker build -t pylogix .
{% endhighlight %}

This will create a Docker image with the name you specified in the 
<image-name> field.

### Step 4 - Run the Docker Image
Now that we have built the Docker image, we can run it. To do this, run the following command in your terminal:

{% highlight console %}
docker run -it pylogix
{% endhighlight %}


This will start the Docker container and you will be able to use PyLogix inside it.

Conclusion
In this tutorial, we showed you how to create a Dockerfile from a Python 3.12-slim-bullseye Docker image and install PyLogix. We also showed you how to build and run the Docker image. With this knowledge, you can now create and manage Docker images for your applications.
