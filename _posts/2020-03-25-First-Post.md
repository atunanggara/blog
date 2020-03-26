---
toc: false
layout: post
description: Setting up Index Page and About Me on fastpages.
categories: [fastpages]
title: First Post - Setting up Index Page and About Me on fastpages
---

<!-- # First Post - Setting up Index Page and About Me on fastpages -->

This first post will be about how I set up my `Index Page` and `About Me` for this [fastpages](https://github.com/fastai/fastpages) site along with an introduction on how I stumble upon the platform.

## Introduction

In the past couple of weeks, the [Introduction to Machine Learning for Coders](https://course18.fast.ai/ml) by Jeremy Howard has helped me better understand Random Forest technique and provided me with a nice introduction to deep learning.

![covid-19]({{site.baseurl}}/images/covid-19wordcloud.jpg "https://flic.kr/p/2iDBF1E")

Then, [Covid-19](https://www.who.int/emergencies/diseases/novel-coronavirus-2019) happened.

Since I am a fan of [fast.ai](https://www.fast.ai/), I listened to [Jeremy's YouTube summary on the situation](https://youtu.be/GZ0yNMnvwqY). At the end of his video, he pointed his audience to the [fast.ai forum](https://forums.fast.ai/c/covid-19/52).

When I searched through it, I stumbled upon the beautiful [Covid-19 Dashboards](https://covid19dashboards.com/) website. The beauty and simplicity of the format is what really sold me into creating my site using this [fastpages](https://github.com/fastai/fastpages).

## Setting up

In terms of [setting up fastpages](https://github.com/fastai/fastpages#setup-instructions), it is pretty self-explanatory. I am thankful to [Abdul Majed](https://twitter.com/1littlecoder) for his nice [walk-through video](https://youtu.be/L0boq3zqazI) that helped reassure me that I am on the right track.

Yet, I find myself stumbling through what would be the next step for me once I have the blog template up and running. So, here is my attempt to share with you what I have done to customize the `Index Page` and `About Me` page.

### Index Page

The Index Page can be accessed under `index.html` on the main repository:
![covid-19]({{site.baseurl}}/images/index-html.png)

Once I hit the `Edit this file` [button](https://help.github.com/assets/images/help/repository/edit-file-edit-button.png), I used my markdown skill to edit the pages:

![edit pages]({{site.baseurl}}/images/Index-playaround.png)

A few things to note:

- The `Index Page` is created using markdown, even though it is an html file. If you are not familiar with markdown, here are some guides from [fastpages](https://fastpages.fast.ai/markdown/2020/01/14/test-markdown-post.html) or from [github](https://guides.github.com/features/mastering-markdown/)
- **Line 6** uses `<!--` in the beginning and `-->` at the end to comment the index.html file. Since markdown do not have the capacity to comment, I used [html comment tag](https://html.com/tags/comment-tag/) instead.
- The welcome image is taken from [flickr](https://flic.kr/p/7BWCTs). I embedded the image by uploading it into github repository `images` folder and coding it into the page (`![edit pages]({{site.baseurl}}/images/Index-playaround.png)`).

### About Me

The `About Me` page can be accessed under `_pages/about.md` on the main repository:
![about me]({{site.baseurl}}/images/blog_about.png)

Same process as the `Index Page` setup above.

## Summary

I hope that this post will help others who are trying to set up their `Index Page` and `About Me` fastpages site. Feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/atunanggara/) or [Twitter](https://twitter.com/atun_anggara) if you have any questions!
