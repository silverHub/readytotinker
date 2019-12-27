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
* 2. click: select a site generator (Gatsby)
* 3. click: select a CMS (Netlify CMS)
* 4. click: deploy (Netlify + GitHub)

Worked like a charm. Based on the wizard, my understanding was the following: 

* source of the page will be stored under my GitHub account (*Note: be prepared to authorize Stackbit to access your GitHub account.*)
* some magic (called site generator) included which is most probably important, but I don't know yet why
* the generated page comes with a placeholder text which I can conveniently modify with content management system (CMS)
* my page is already deployed and accessible on the Internet. Fascinating.

I found this extremely quick and useful in case of simple web pages, like portfolio pages, resumes, blogs. It also gives an easy way to experiment with different solutions, pick any static site generator or CMS and play with the result. As a bonus, the source code is all yours so you can develop extra functionality on top of the existing ones, but that requires deeper understanding of the building blocks. 

**The concept.**  Let's take a simple blog as a use case. A blog usually comes with introduction texts and posts. Static texts are part of the source but posts can be considered dynamic content because usually you need to have a solution to store and add/modify/delete them and this is usually solved with a server side module and a database. With Stackbit there is no server interaction, posts are stored together with the source code. This principle follows the [JAMStack](https://jamstack.org/) architecture, which got popular lately thanks to it's simplicity and excellent scaling possibilities. Seems to me a modern rethink of the good old solutions, like WordPress/Drupal/Joomla. 

Handling posts as part of the source code is a surprising idea for first but it gives you a certain level of freedom and simplicity. The format of these files are well-defined and together with other JSON files which contain further meta-information can be processed during build time. To enable easy processing the content is defined with Markdown. The build produces the final HTML files which are going to be deployed to a hosting service, at the time of writing, only Netlify is supported. So if I would like to do changes in texting or create a new post I need to use Git commits, that can be done manually as well, but the supported CMS engines could also do this for you with the convenience of a basic GUI.

![Netlify CMS](/images/cms.jpg "Netlify CMS")

So why do you need Stackbit? Truth is, if you would start with a Gatsby template you could also get to this point with a fair amount of work. Stackbit just makes it a lot more easier, orchestrating the bits and providing a central place where you can easily manage the whole flow. Also sprinkle a nice customization in the form of templates for various use cases, when you logged in to Stackbit you will get a dashboard with your projects. You can also get free updates if the templates are developed further.

**The pieces.** Here is a high level overview on the building blocks:

***GitHub***: stores the source of the webpage. Change detection is built on webhooks, every commit on master branch triggers a build in Netlify.

***Gatsby***: static site generator based on React, turns our source into static HTML files. Gatsby comes with an opinionated project folder structure, configuration stored in JSON files and certain folders contains dynamic content which is processed during build. 

***Netlify***: provides CI and hosting, the build and deployment process is automated. Build is triggered by Git commits and runs on Netlify server, the artifacts are deployed to Netlify's CDN. Always the artifacts from the latest build is available in CDN. Netlify provides also a CMS system.

***Stackbit***: provides pre-built themes and orchestration. 

To be able to leverage further benefits of this setup, I need to dig deeper. Further posts will come about the customization options.
