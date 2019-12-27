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
**The wonder of Stackbit.** During my recent surfing session I stumbled upon a minimalist little app, called [Stackbit](https://www.stackbit.com/).  I've just read the first sentence but right away I decided to give it a try. Stackbit (still in Beta but works stable) promised to create me a personal page in no time at all and absolutely free. Who wouldn't try that? 

![Stackbit](/images/stackbit.jpg "Stackbit theme selector")

After 4 click I had my page ready.

* 1. click: choose a template
* 2. click: select a site generator
* 3. click: select a CMS
* 4. click: deploy

Worked like a charm. Based on the wizard, my understanding was the following: 

* source of the page will be stored under my GitHub account (*Note: be prepared to authorize Stackbit to access your GitHub account.*)
* some magic (called site generator) included which is most probably important, but I don't know yet why
* the generated page comes with a placeholder text which I can conveniently modify with content management system (CMS)
* my page is already deployed and accessible on the Internet. Fascinating.

I found this extremely quick and useful in case of simple web pages, like portfolio pages, resumes, blogs. It also gives an easy way to experiment with different solutions, pick any static site generator or CMS and play with the result. As a bonus, the source code is all yours so you can develop extra functionality on top of the existing ones, but that requires deeper understanding of the building blocks. 

**The concept.**  Let's see the use case of a simple blog which usually comes with introduction texts and posts. Static texts are part of the source but posts can be considered dynamic content because usually you need to have a solution to store and add/modify/delete them and this is usually solved with a server side module and a database. But in our case there is no server interaction, posts are stored together with the source code. This principle follows the [JAMStack](https://jamstack.org/) architecture, which got popular lately thanks to it's simplicity and excellent scaling possibilities. Seems to me a modern rethink of the good old solutions like WordPress/Drupal/Joomla. 

Handling posts as part of the source code is a surprising idea for first but it gives you a certain level of freedom and simplicity. The format of these files are well-defined and can be processed during build time, that's why we use a static site generator. 

The goal of Stackbit is clear to deliver a static web page in no time, focus is on client side, every variable which requires server side tinkering is simply left out from the equation.

**The pieces.** GitHub



JAMStack.

We have Stackbit 

Netlify (CMS)

GitHub
