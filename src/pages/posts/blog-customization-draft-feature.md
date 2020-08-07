---
title: "Blog customization: Draft posts"
subtitle: Enable draft posts
draft: true
date: 2020-07-08T14:18:12.549Z
excerpt: Adding the feature to create draft posts which are not visible to the readers.
template: post
---
> Stackbit app reference > customization series
>
> Precise reference to package versions

# Draft mode

First thing I learned is that CMS gives you a very basic change management. Every change you save will be published right away. This is equally true for configuration changes or new blog posts. I found that a real pain point given that you don't have always time to sit down and write a blog post from beginning to the end. Keeping unfinished posts in other tools is less satisfactory in my opinion. If this is a pain point for me, probably it is for others as well, so a logical step would be to have a look what solutions have emerged to this problem.

## Editorial workflow

One solution is provided by Netflify CMS itself. With some digging in the documentation you can easily find this:

> By default, all entries created or edited in the Netlify CMS are committed directly into the main repository branch.

but there is a configuration option to change this. [Editorial workflow](https://www.netlifycms.org/docs/add-to-your-site/#editorial-workflow) adds an interface for drafting, reviewing, and approving posts. The changed UI actions (Save draft, Edit draft, Approve and publish draft) makes the cooperation with co-writers extremely convenient. In the background Netlify CMS creates a new GitHub branch to persist your changes when you save a draft. In the same time a pull request (PR) is also created. With your approval the PR will be merged into your main branch which will trigger the CI process. There is also a handy dashboard to supervise the pending changes. You can enable editorial workflow if you edit **[publish_mode](https://www.netlifycms.org/docs/configuration-options/#publish-mode)** in */static/admin/config.yml*.

Although this feature looks like a perfect solution to our problem, I found it a bit too much for my need. Not just posts requires constant approval but also every single configuration change as well, which makes the workflow very tedious.

## Simpler solution

Now that I know what I don't want, I could better formalize what do I really need for. 

> Code tinkering