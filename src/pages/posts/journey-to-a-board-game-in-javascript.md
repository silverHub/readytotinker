---
title: A journey to implement a board game in Javascript
draft: false
date: 2019-08-25T18:36:29.005Z
thumb_img_path: /images/christopher-paul-high-y7qq9irgpoa-unsplash.jpg
content_img_path: /images/christopher-paul-high-y7qq9irgpoa-unsplash.jpg
excerpt: >-
  Outline of a project to implement a classical board game in JS with all the
  belongings. Step by step.
menus:
  main:
    identifier: ''
    title: ''
    weight: ''
template: post
---
Photo by Christopher Paul High on [Unsplash](https://unsplash.com/photos/y7Qq9IrgpOA)

## **Prelude**

**The plan.** I was always fascinated by computer games. Back in the days I consumed multiple genre and always wondered how hard would it be to implement one. Since then I had the motivation to figure it out at one day. This day has finally come. I plan to implement a game from scratch without having any in-depth knowledge about how computer games developed, so I'm ready to go through all the bits and pieces and learn it on the hard way. Of course I'm not going unarmed into this battle, I have more than 10 years programming experience with multiple languages (C, Java, JavaScript) and I consider myself up-to-date on FE development techniques and modern browser technologies. As a professional, I like to learn new things, this is also one of the driver which put me on this path, I want to learn new things. The farther from my comfort zone is the better. You should expect very technical details on everything I will face with.

I expect this project will span through a couple of months (maybe years) - depending on my free time - which is absolutely OK. No rushing, I don't want to commit to hard deadlines, I would follow Blizzard's philosophy here: "It's done when it's done". You might say this will jeopardize the whole project, but in this case, not the destination is the important but the path to get there. Even if you reach just halfway, you already gained a lot. The idea is to fuel this project by pure fun and the excitement of learning, I hope this will be enough to complete.

**The game.** After careful consideration I chose to implement the following board game: [Game of Thrones (Second Edition)](https://boardgamegeek.com/boardgame/103343/game-thrones-board-game-second-edition). The game is based on George R. R. Martin popular fantasy book series (Song of ice and fire), (intentionally not mentioning the HBO series) which will most probably never be finished. It is a competitive strategy game with 3-6 players where players battle in the colors of the Great Houses on the map of Westeros for control and glory. A party could easily took 5-6 hours (especially when you are revisiting the rule book from time to time) and requires permanent concentration till the end. What I find truly enjoyable is the polished battle system where you must foresee your opponents next move to be able to properly counter. Usually luck is out of the game (it's possible to opt-in unpredictability in case of the encounters through random modifier cards, but I usually vote that down). It is a challenge at first to digest the vast rule book, but in the end, the dynamics are well-balanced and give space for strategical thinking. Apart from the fact that I own this game and find it really enjoyable to play I believe it provides enough challenge. It comes also with some advantages:

* the game graphics are basically given, the game contains a well-designed map with other game pieces so I could concentrate on how to digitize and render these on the screen instead of designing something from scratch which would be entirely out of my comfort zone (maybe next time)
* the game rules are solid so the real challenge will be how to implement those and present in a user-friendly way

So let's see what we could expect at the end of the journey, the requirements (for myself) would be the following:

* a digital version of the official board game which runs in a browser, implemented in JS and using only browser technologies
* support for multiplayer mode: players can connect through Internet
* support for single player mode: one player can play against bots
* self-learning bots: the bots will employ machine learning to make smarter moves with time (**this will come most probably with the second iteration**)

This is already an impressive list, so let's ponder on a bit how to start. In the end we need a JS application running in a browser, it wouldn't be that hard, right? Let's see. 

TBD thoughts about implementation



**The journey.** For me the path to the solution  has the same importance as the end result. Therefore I'm going to dedicate time to the details, contemplate on things, experiment with different solutions. 

I plan to guide the reader through the process of implementation with a series of blog posts. In every post I will pick a challenge (implementation detail) and try to describe the natural learning process I'm going through to solve this with the best possible way, according to my standards. There might be challenges which focuses on less important aspects and possible that not every solution is actually needed for the end result. This is also fine, as the documentation of the journey will be also a reflection on the learning process on how to develop a game. I try to cover every aspect which emerge during game development, I can't give a comprehensive list upfront as most probably I'm also not aware of everything. The topics will be various, range from graphical design of game elements through the actual coding of different game mechanics to the observation of application architecture and resource handling, I guess in some way all will be connected to FE development. Every journey starts with the first step, in our case the first step is to define what we want to achieve.

TBD: Technical stuff

To make my life easier I confine my soon-to-be application to run solely on Chrome, the most advanced browser today. As GOT is entirely played on the main map I would start to have a look on how can I manifest the main map in the browser.

Next article in the series: [Implementing an interactive map with SVG](https://silverhub.netlify.com/posts/implementing-an-interactive-map-with-svg/)
