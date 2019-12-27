---
title: How's my blog work?
subtitle: >-
  This question really gave me some headache recently. But let's start at the
  beginning.
draft: false
date: 2019-12-01T15:18:12.549Z
thumb_img_path: /images/blog.jpg
template: post
---
**The wonder of Stackbit.** During my recent surfing session I stumbled upon a minimalist little app, called [Stackbit](https://www.stackbit.com/). I've just read the first sentence but right away I decided to give it a try. Stackbit promised to create me a personal page in no time at all and absolutely free. Who wouldn't try that? 

![Stackbit](/images/stackbit.jpg "Stackbit theme selector")

After 4 click I had my page ready.

* 1. click: choose a template
* 2. click: select a site generator
* 3. click: select a CMS
* 4. click: deploy

*Note: be prepared to authorize Stackbit to access your GitHub account.*

Worked like a charm. So at that moment my understanding was the following: it uses my GitHub account to store things. There is some magic included (called site generator) which is most probably important. The page comes with a placeholder text and although I don't know how the page built up but I can conveniently modify the content with a CMS system. On top of that my page is already deployed and accessible on the Internet. Fascinating.

I realized that I need to dig deeper if I want to get more benefit from this. So let's dig deeper and start with a high level overview what's happening here.

**The concept.** The goal here is to deliver a static web page in no time, focus is on client side, every variable which requires server side tinkering is simply left out from the equation. Let's see the use case of a simple blog which usually comes with introduction texts and posts. Posts can be considered dynamic content because usually you need to have a solution to store and add/modify/delete them and this is usually solved with a server side module and a database. But in this case we have no server interaction, posts are stored together with the source code. This principle follows the [JAMStack](https://jamstack.org/) architecture, which got popular lately thanks to it's simplicity and excellent scaling possibilities. Seems to me a modern rethink of the good old solutions like WordPress/Drupal/Joomla.

**The pieces.** GitHub

This idea is surprising for first but in the end it gives you a certain level of freedom and simplicity. 

JAMStack.

We have Stackbit 

Netlify (CMS)

GitHub
