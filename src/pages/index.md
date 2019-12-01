---
title: Home
sections:
  - component: HeroBlock
    content: >-
      You will find every important information about me here.


      Additionally you should find technical blog posts and the list of my pet
      projects as well. With time.
    section_id: hero
    title: Title of Hero section
    type: heroblock
  - actions: []
    component: ContentBlock
    content: >-
      This is the "about" excerpt. It can be used to provide a paragraph about
      yourself that people can read on the homepage to get a sense of who you
      are. There also exists a dedicated about page where you can write more
      about yourself for those who are interested.
    image: /images/intro.jpg
    section_id: about
    title: About me
    type: contentblock
  - actions:
      - label: View Blog
        url: blog/index.html
    component: PostsBlock
    num_posts_displayed: 4
    section_id: recent-posts
    title: Recent Posts
    type: postsblock
menus:
  main:
    title: Home
    weight: 1
template: home
---

