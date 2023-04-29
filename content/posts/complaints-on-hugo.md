---
title: "Complaints on GitHub Pages"
date: 2023-04-28T08:43:14-04:00
draft: false
description: 'Complaints on GitHub Pages hosting services when working with Hugo'
tags: ['GitHub', 'Hugo','complaints', 'static website', 'front-end']
keywords: 
- Aether
- GitHub
- Hugo
- Static Site
- HTML
- CSS
- Web Development
- Programming
- Tech
categories: ['Blog', 'Personal']
---

# Welcome

Welcome to the first post of my blog, aethers-vi, in which I will talk about the different complaints and problems
I've been having working with Hugo along with GitHub Pages for the past 3 days, as well as explain some of the 
solutions I found useful for the problem I was having. I'll tell you in advance, it's been hell. 


# Problems


## Lack of documentation

Since the start of my journey trying to start this blog and post for the world for the first time, I've been
struggling with the fact that paying for a server is too expensive for a blog which will be managed by one person 
only, So I went to explore other alternatives that could offer me something more accessible. That's how I learned
about static websites generators.

I came across many static website generators, including Next.js, Jekyll and Hugo, the last one being the one I'm
to make this blog right now. 

Since Hugo seemed interesting and looked like a tool which wasn't going to be that much of a trouble to 
deploy a website and start working on my blog and my social media presence, I decided to give it a shot which
lasted three entire days of sorrow and suffering.

After installing Hugo on my laptop, I followed the steps to create a new site, create a new post, push it to 
a GitHub repo and host it using GitHub Pages. This is where hell starts.

When the site was deployed, it was supposed to load the content and the theme correctly, which means the HTML
and CSS of the time. What an unpleasant surprise for me that only the HTML was loading on the site. 

After seeing this, I decided to do what every software developer would do in a situation like this: Google. 
I'm lying, I first tried to troobleshoot it myself and then googled it. 

After searching through Google for an hour and trying every single solution here was, I started to get desperate. 
I even tried looking up different tutorials that tried different approaches to hosting a Hugo site on GitHub
Pages. This didn't work at all, since it was working for everyone and not for me. I started to even think that
there had to be a problem with the version of Hugo I had installed, or with the blog.


## Unprecise Visual Material

The tutorials I found on YouTube about the topic didn't help much either. Most of them followed the same steps
to get to the same result at the end, without touching the different problems that one may have
trying to follow along. I have to admit that some of the videos did things differently, which helped me
understand many things. But, even though my knowledge developed, I was still in the exact same place with no 
progress regarding my blog.


# Discoveries

Reading half of the posts about the problem I'm having helped me learn some things. The main reason this problems happens
is because of the `index.html` is not able to find the directory in which the styles are located. This happens because in the
`config.yml ` file (or `tml`, which ever you prefer) the `baseURL` isn't set correctly. The baseURL is supposed to be the URL
of the site, in which the site will search for the favicon, images, and most importantly, styles. The three main solutions I 
found for this problems were the following:

1. Changing the `baseURL` to `/`: This is supposed to fix the problem since you're setting the baseURL to be a relative URL,
that way, when the page searches for assets, instead of going `<URL>/.../assets/` it will go `/assets/`. 
2. Changing the `baseURL` to `https://<github_username>.github.io/<name_of_the_site>/`: This uses github as the root directory for 
the assets, so the website goes there when it needs to find the styles and any other element needed for the site.

Neither of this solutions worked for me. I tried setting the end of the baseURL to a `/`, I tried deleting 
that, I tried leaving it blank, I tried setting
to a relative directory, and even enable the `relativeDirectory` and `uglyURLs` parameter on the `config.yml` file to see if that 
was the problem, and nothing seemed to work.

# Solution

After trying almost everything at hand, I came across a page called Netlify. This page offers a free hosting service with some limitations
for people and teams to host their websites there. 

At the beginning, I was skeptical with the idea of using this service, but then I gave it a try. The firs time I tried, it worked perfectly
but the home button of the page wasn't working as expected, so I went back to the GitHub Pages to keep trying since I though it was supossed to work
well there. 

After losing my patience once again, I came back to Netlify after deploying everything on GitHub and hosted it there, and figure out that 
for the home button to work, I had to set the baseURL to `/` once again so the site searches for the relative directory of each thing on order to work correctly.

Then, after deploying on Netlify, I had a beautiful website fully working with no issues. 

