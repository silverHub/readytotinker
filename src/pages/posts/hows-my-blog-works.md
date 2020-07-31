---
title: How's my blog work?
subtitle: This question really gave me some headache recently. But let's start
  at the beginning.
draft: false
date: 2019-12-01T15:18:12.549Z
thumb_img_path: /images/blog.jpg
content_img_path: /images/blog.jpg
template: post
---
# **The wonder of Stackbit**

During my recent surfing session I stumbled upon a minimalist little app, called [Stackbit](https://www.stackbit.com/).  After reading the marketing info I decided to give it a try. Stackbit (at the time of writing it is still in Beta but seems stable) promised to create a personal page in no time and absolutely free. 

Who wouldn't try that? 

After 4 click I had my page ready.

1. click: page template chosen
2. click: site generator ([Gatsby](https://www.gatsbyjs.org/)) selected
3. click: CMS system ([Netlify CMS](https://www.netlifycms.org/)) selected
4. click: deployment ([Netlify](https://www.netlify.com/) + [GitHub](https://github.com/)) triggered

Worked like a charm. Based on the wizard, my understanding was the following: 

* source of the page will be stored under my GitHub account (*Note: be prepared to authorize Stackbit to access your GitHub account.*)
* some magic (called site generator) included which is most probably important, but I don't know yet why
* the generated page comes with a placeholder text which I can conveniently modify with content management system (CMS)
* my page is already deployed and accessible on the Internet. Fascinating.

![Stackbit](/images/stackbit.jpg "Stackbit theme selector")

I found this extremely quick and useful in case of simple web pages, like portfolio pages, resumes, blogs. It also gives an easy way to experiment with different solutions, pick any static site generator or CMS and play with the result. As a bonus, the source code is all yours so you can develop extra functionality on top of the existing ones, but that requires deeper understanding of the building blocks. 

# **Solution overview**

Let's take a simple blog as a use case. A blog usually consist from static (introduction texts, icons etc..) and dynamic data (blog posts on various topics). Static data is part of the source code but for dynamic content you need to have a solution in place to store and add/modify/delete and this is traditionally solved with a server side module and a database. 

Your Stackbit blog is delivered as a static webpage without server interactions. Still, you can add arbitrary pages and blog posts through the content management system. These changes are released within minutes. In the background, your dynamic content is stored on GitHub as part of the source code. Netlify CI system is triggered by every GitHub action and compiles your source into a shippable webpage. Here is the overview:

![Figure about technical components behind a Stackbit blog](/images/stackbitblog.png "Solution overview")

The solution follows the [JAMStack](https://jamstack.org/) architecture principles. Having a simple static site at the end of the build process has numerous advantages:

* your site loads faster, no server-side calls to hinder rendering
* excellent scaling as you can deploy the whole blog to CDN

The complexity of the dynamic content management is hidden behind CMS and a sophisticated build process. 

#  Components

Handling dynamic content as part of the source code is a surprising idea for first but it gives you a certain level of freedom and simplicity. The format of these files are well-defined and together with other JSON files which contain further meta-information can be processed during build time. To enable easy processing the content is defined with Markdown. The build produces the final HTML files which are going to be deployed to a hosting service, at the time of writing, only Netlify is supported. So if I would like to do changes in texting or create a new post I need to use Git commits, that can be done manually as well, but the supported CMS engines could also do this for you with the convenience of a basic GUI.

![Netlify CMS](/images/cms.jpg "Netlify CMS")

So why do you need Stackbit? Truth is, if you would start with a Gatsby template you could also get to this point with a fair amount of work. Stackbit just makes it a lot more easier, orchestrating the bits and providing a central place where you can easily manage the whole flow. Also sprinkle a nice customization in the form of templates for various use cases, when you logged in to Stackbit you will get a dashboard with your projects. You can also get free updates if the templates are developed further. Here is a high level overview on the building blocks:

***GitHub***: stores the source of the webpage. Change detection is built on webhooks, every commit on master branch triggers a build in Netlify.

***Gatsby***: static site generator based on React, turns our source into static HTML files. Gatsby comes with an opinionated project folder structure, configuration stored in JSON files and certain folders contains dynamic content which is processed during build. 

***Netlify***: provides CI and hosting, the build and deployment process is automated. Build is triggered by Git commits and runs on Netlify server, the artifacts are deployed to Netlify's CDN. Always the artifacts from the latest build is available in CDN. Netlify provides also a CMS system.

***Stackbit***: provides pre-built themes and orchestration. 

To be able to leverage further benefits of this setup, I need to dig deeper. Further posts will come about the customization options.