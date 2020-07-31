---
title: "Blog customization: Draft article"
subtitle: Enable draft posts
draft: true
date: 2019-12-01T15:18:12.549Z
excerpt: Adding the feature to create draft posts which are not visible to the readers.
template: post
---
> Stackbit app reference

First thing I learned that change management with CMS is kind of binary. There is only *Publish* button, as soon as you hit it a GitHub commit is created which then triggers the whole build and deploy process. But there is a need to just simply save things without exposing it to the readers. For example I would like to have a possibility to add unfinished posts. Seems to me a simple requirement, you don't have always time to write a post from the beginning to the end, so either you store the drafts somewhere else (which I don't want to do) or you just look around because somebody had already solved this for sure.

One solution is provided by Netflify CMS. With some digging in the documentation you can easily find this:

> By default, all entries created or edited in the Netlify CMS are committed directly into the main repository branch.

but there is a configuration option to change this. If "editorial workflow" mode is switched on

\- every changes will be pushed to a new branch 

\- CMS will provide a dashboard to overview the changes which are in different state and to be able to merge those into master

The config which controls this called **[publish_mode](https://www.netlifycms.org/docs/configuration-options/#publish-mode)**. Sounds good, now we need some better understanding on project configuration to be able to switch this on.

\---
