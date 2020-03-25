---
toc: true
layout: post
description: Setting up my own blog with fastpages.
categories: [markdown]
title: First Post - Setting up fastpages blog  
---

# First Post - Setting up fastpages blog  

This first post will be about my set up for this blog using [fastpages](https://github.com/fastai/fastpages) and how I stumble into it.  

## Introduction  

In the past couple of weeks, the [Introduction to Machine Learning for Coders](https://course18.fast.ai/ml) by Jeremy Howard have helped me better understand Random Forest technique and provided me with a nice introduction to deep learning. 

![covid-19]({{site.baseurl}}/images/covid-19wordcloud.jpg "https://flic.kr/p/2iDBF1E") 

Then, [covid-19](https://www.who.int/emergencies/diseases/novel-coronavirus-2019) happened.  

Since I am a fan of [fast.ai](https://www.fast.ai/), I ended up listening to [Jeremy's YouTube summary on the situation](https://youtu.be/GZ0yNMnvwqY). At the end of his video, he pointed his audience to the [fast.ai forum](https://forums.fast.ai/c/covid-19/52). 

When I searched through it, I ended up going through the beautiful [covid-19 Dashboards](https://covid19dashboards.com/) website. The beauty and simplicity of the format is what really sold me into creating my blog using this [fastpages](https://github.com/fastai/fastpages) format. 

## Setting up

In terms of [setting up fastpages](https://github.com/fastai/fastpages#setup-instructions), it is pretty self-explanatory. I am thankful to [Abdul Majed](https://twitter.com/1littlecoder) for his nice [walk-through video](https://youtu.be/L0boq3zqazI) that helped reassure me that I am following the right path.  

However, I find myself stumbling through what would be the next step for me once I have the blog up and running. So, here is my attempt to share with you what I have done to customize this blog. 

### Main page

The main page can be accessed under `index.html` on the main repository:   
![covid-19]({{site.baseurl}}/images/index-html.png "")   

Once I hit the `Edit this file` [button](https://help.github.com/assets/images/help/repository/edit-file-edit-button.png), I used my markdown skill to edit the pages: 

![edit pages]({{site.baseurl}}/images/Index-playaround.png "")   

Two things to note: 
- **line 6** shows me using `<!--` in the beginning and `-->` at the end to comment the index.html file. Since markdown do not have the capacity to comment, I used [html comment tag](https://html.com/tags/comment-tag/) instead. 
- If you are not familiar with markdown, here are some guides from [fastpages](https://fastpages.fast.ai/markdown/2020/01/14/test-markdown-post.html) or from [github](https://guides.github.com/features/mastering-markdown/)

### About Me

The `About Me` page can be accessed under `_pages/about.md` on the main repository:  
![about me]({{site.baseurl}}/images/blog_about.png "")   

Repeat the process on the Main Page. 

## Summary

I hope that this post will help others who are trying to set up their first fastpages site. Feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/atunanggara/) if you have any questions!
