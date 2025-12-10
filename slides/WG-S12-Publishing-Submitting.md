---
marp: true
paginate: true
theme: webgames
---


<!-- _class: main -->

# Web Games

## Week 12: Publishing & Submitting your Game

<!--
Welcome to week X
-->

---
<!-- _class: small-txt -->
# Festive Student Social

**When:** Tuesday 16th December, 12:30 – 14:30
**Where:** CM.G10
**Who:** All students on computing courses – you’re invited!

Join us for some festive cheer before the holidays! There’ll be refreshments, good vibes, and a chance to relax and catch up with friends. Whether you’re feeling merry or just need a break from code, this is the perfect way to wrap up the term.

✨ Bring your festive spirit (and maybe your best Christmas jumper)!

We can’t wait to see you there!

*P.S. From 3.30pm Creative Computing (Gaming) students will be showcasing their Commercial Games Project in CM.G32, come along and play test their game*

---

![](../assets/icons/task-list.png#ico-right)

# Objectives

- Explore options for monetising web games
- Explore options for publishing web games
- Overview submission requirements

<!--
In today's session we will...
-->

---

<!-- _class: lead -->

# 1. Monetising Games

---

![](../assets/icons/revenue.png#ico-right)

# Monetisation Options

- Free
- Premium
- IAP
- Advertising
- Publisher revenue share
- PWYW

<!--
There are many options for monetising web games, if you even want to monetise the game at all. However it is an important consideration to make, especially now you are in your third year and moving ever closer to graduating. You need to be thinking about how you might make money from the skills you have and the content you make. 

Obviously you may just want to release the game for free and this is a valid means of gaining feedback on your work and generating an audience around your creations as you begin to establish a portfolio. Being free you also have the lower barriers to entry for an audience and therefore the potential for greater audience traction. Consider however the work that has gone into the game in terms of your time as a long term strategy releasing games for free won’t pay bills, so there needs to be indirect value (such as building and audience / portfolio with view to monetise future games / get a job).

Premium - You could consider selling your game, setting a price could come down to a variety of factors and depends on the depth and scope of the game. Market research is important here, see what other similar titles are selling for to ensure you do not over or under value your game. Placing a price on your game adds a barrier to engagement therefore will decrease the potential number of players. Therefore you might consider a free demo version and a larger premium title. This is how you might view the scope of your “playable prototype” in terms of this assessment. You could portray the game as a demo version where you want to showcase enough in your game that convinces players to want to play more and engage them enough to encourage a willingness to pay for a premium version. There are various options for selling you game depending what platform you use to publish. For example if you self publish you could use simple paypal transactions, or itch.io enables you to sell content on their site. Additionally if you decide to publish on platforms outside the web (e.g. mobile / steam) you can use their stores to enable premium transactions

IAP - In app purchases or in game purchases might be an option for some games, but this depends on the type of game you are building, not all games will be suitable for in app purchases and you do not want to force them in for the sake of it. How you implement these also depends on how you intend to publish the game. If deploying on mobile Construct has an official plugin to handle in app purchases. On web things might be slightly tricker as there is no official plugin that does the hard work for you but could be done by integrating payment services such as paypal and stripe with a firebase database. 

Advertising - Placing ads in your game might be a seemingly easy way to monetise your game, whilst also retaining the benefits of keeping it free for the player to minimise to cost of engagement and therefore maximise player numbers. However, do consider the number of plays required to make advertising a cost effective means of monetising games. Some ad providers require 1,000,000 plays a month, therefore you need a very popular game to make this method of monetisation viable. There are various options for placing ads in a construct game. Again on mobile there are official plugins for ios and android that can help handle things for you. On web as there are various ad providers there is no official plugin so adding ads will require adding some custom javascript to your game and the steps will differ depending on the ad provider. However, these steps are usually straightforward and well documented. Also on web depending where you upload you game ads will be handled for you by the third party, which leads us to publisher revenue share

Publisher Revenue share - There are lots of HTML5 game arcade sites where you can upload you game, many of which will place ads on the game and the offer revenue share for example Kongregate offers 50% revenue share on games uploaded to their platform which works out at between 1 and 2 dollars per 1,000 plays. Some of these platforms also offer further means of making revenue such as using their APIs for in app purchases. As these platforms have access to thousands of players often they can be an attractive partner to work with, do your research into which platforms offer what, and what requirements they might have (e.g. SpilGames have specific requirements and a need to integrate with their API)

PWYW: PWYW stands for pay what you want, which can be a means of enabling the benefits of free to play (audience reach) with the potential of making revenue through premium payments. PWYW puts the decision into the hands of the audience and allows them to determine the price they wish to pay for the game (if any). Obviously many players will pay nothing, but some may decide to pay and research into PWYW methods has shown that people will often pay over the typical asking price. However, your job as a developer will be to create a game that generates enough value and engagement to encourage a willingness to pay. PWYW could be deployed with a simple paypal donate button on your game using the browser and ajax objects, or sites like Itch.io often deploy the pay what you want pricing model for indie games and assets - https://daz.itch.io/tiny-fragments

-->

---

![](../assets/icons/revenue.png#ico-right)

# Monetisation Resources

- [Mobile Advert Plugin](https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/mobile-advert)
- [Mobile IAP Plugin](https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/mobile-iap)
- [Game Monetisation Article MDN web docs](https://developer.mozilla.org/en-US/docs/Games/Publishing_games/Game_monetization)
- Further resources on Ultra...

---
<!-- _class: lead -->

# 2. Publishing Games

---

![](../assets/icons/sharing.png#ico-right)

# Publishing Options

- Self Hosted
- Arcade Portals
- Mobile
- Steam & Desktop

<!--
As discussed at the beginning of the module, by developing using web technologies and using an engine such as construct you are able to deploy your games to a number of different platforms, including the web, mobile, desktop and some console platforms.

Construct has a range of export options, and plugins to handle these different platforms as well as documentation on the process.

If publishing to the web you have the choice of whether to self host the game (e.g on your own website) or publish on one of the many arcade portals including some of those already mentioned such as Kongregate, Itch.io or the construct arcade itself. I would very much recommend looking to publish your game on one of these portals as these have existing eyeballs in order to generate plays for your game. If you only self host it will be a lot harder to generate plays as you have to do all the work in terms of driving traffic yourself. That isn’t to say you shouldn’t self host as part of your own portfolio, but you should do so in combination with uploading your site to other well know HTML5 game portals. 

When uploading to these external portals don’t forget to include links back to your own website, or social media pages as you want to use this as an opportunity to build your brand and awareness of the work you do.
-->

---

![](../assets/icons/sharing.png#ico-right)

# Publishing Considerations

Remember your games can instantly be played on desktop and mobile browsers, so have you considered handling mobile controls?

- Touch  input also handles mouse
- Platform info object can be used to detect platform
- Construct will autoscale your game
- Fullscreen must be requested
- Test across devices (remote preview is great for this)
- Useful reading: [Performance Tips](https://www.construct.net/en/make-games/manuals/construct-3/tips-and-guides/performance-tips)

<!--
Remember your games accessible on both desktop and mobile instantly as long as you have considered both platforms and input mechanisms...

Also Performance is a big factor in web games and the ability for different browsers to process your games varies wildly, so to does connectivity (people with fast versus slow internet). 

There are many things you can do to enhance performance, but most importantly of all you should test your game on a range of devices and browsers. Some key performance tips include…. 

More detail can be found in constructs own guide on performance
-->
---

![](../assets/icons/sharing.png#ico-right)

# Publishing Resources

- [Publishing Projects](https://www.construct.net/en/courses/publishing-games-84)
- [Publishing Mobile Apps](https://www.construct.net/en/tutorials/publish-mobile-apps-26)
- [Exporting Desktop Apps](https://www.construct.net/en/tutorials/exporting-desktop-apps-with-nw-js-15)
- [MDN Game Distribution Article](https://developer.mozilla.org/en-US/docs/Games/Publishing_games/Game_distribution)
- Further resources on Ultra...

<!--
More resources available on Ultra
-->
---



<!-- _class: lead -->

# 3. Playable Prototpe

---

![](../assets/icons/assessment.png#ico-right)

# S2 - Playable Prototype

A completed web game prototype, with supporting documentation (written & video) that summarises planning, development, testing and potential routes to market.

**Deadline: 15th January**

<!-- 
The playable protoype assessment is a completed web game that addresses the aims of the module. This game is accompanyied by supporting documentation that includes written and video components. 
-->

---

![](../assets/icons/assessment.png#ico-right)

# S2 - Requirements

The genre and concept of your game is up to you but your focus should be on creating games that are easy to pick up, casual in nature, yet still have an addictive replay value and social shareability.

The features you implement are up to you. However, you may wish to consider features that enhance shareability and create avenues for monetisation. Additionally you should aim to publicly publish your game to gather wider feedback and testimonials for your game.

---

<!-- _class: twos -->

![](../assets/icons/assessment.png#ico-right)

# S2  - Supporting Documentation

## Development Document

- Title
- Abstract
- Pre-production Materials
- Technical Description
- User Testing & Feedback
- Critical Reflection

## Walkthrough Video

A short video to serve as a professional showcase of your game. The video must demonstrate a full playthrough of the core gameplay loop, from the start screen to a clear end state (win or loss).

<!--
Your prototype should be accompanied by supporting documentation which includes a written development document and a walkthrough video

The development document should consist of...[Explain each element]

A short video to serve as a professional showcase of your game. The video must demonstrate a full playthrough of the core gameplay loop, from the start screen to a clear end state (win or loss). The recording should have clear audio and visuals to effectively present your work. While commentary is not required, you may include it to highlight specific game mechanics or design choices.

The written development document should not exceed 2,000 words

[EXPLAIN]
-->

---
![](../assets/icons/assessment.png#ico-right)

# S2 - Marking Criteria

- Concept (10%)
- Design & User Experience (25%)
- Technical Implementation (40%)
- Documentation (25%)
<!--
The playable prototype is assessed on the following criteria

[EXPLAIN]
-->

---

![](../assets/icons/assessment.png#ico-right)

# S2 - Submission

The deliverables for the Prototype Game are as follows:

- A Construct .cp3 file to run your game
- Development Document (word or pdf)
- Walkthrough video

Each of these files should be uploaded to the submission portal on Ultra.

**DO NOT** just add a One Drive link to the submission portal.

<!--
Please ensure you follow the submission requirements correctly. There will be mark penalties for not doing so.
-->
---
![](../assets/icons/assessment.png#ico-right)

# Assessment Support

I will be on leave between 20th Dec - 5th Jan (inclusive), other than these dates I am available for assessment support ahead of the deadline on 15th January.

You can book this support using [this link](https://outlook.office.com/bookwithme/user/2898184395f04dcdaf2e79711f520ab4@bathspa.ac.uk?anonymous&ismsaljsauthenabled&ep=plink)

---

![](../assets/icons/assessment.png#ico-right)

# Project Development

![w:500 Illustration of laptop with users hands on coffee mug and mouse](../assets/images/development.gif#right)

Use the remainder of the session to continue working on your playable protoypes and address some of the feedback you gathered during testing.

---

<!-- _class: main -->

# Up Next...

## Nothing... that's it!

<a style="text-decoration: underline; position: absolute; bottom: 40px; font-size: 20px; color: #272838;" href="https://www.flaticon.com" target="_blank" title="cloud service icons">Icons sourced from Flaticon</a>
<!--
Next week...
-->