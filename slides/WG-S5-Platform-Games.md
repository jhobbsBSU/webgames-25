---
marp: true
paginate: true
theme: webgames
---


<!-- _class: main -->

# Web Games
## Week 5 - Platform Games

<!--
Welcome to week 5
-->
---

# Guest Talk with Philip Sinclair

Join Creative Computing Commercial Games students for a Guest Talk from Philip Sinclair, founder of Spectrum 48 (spectrum48.com). Philip will be discussing the journey of their game OCO – from an idea to iOS ‘Game Of The Day’ worldwide and a million downloads as well as discussing their latest ventures.

The talk takes place Tuesday, 21st October 3:30pm, CM.G32

<!--
Whilst scheduled in another module, this talk has high relevance to Web Games with OCO being a game that directly aligns with the module aims. Therefore I highly recommend attending if you can
-->

---

![](../assets/icons/task-list.png#ico-right)

# Objectives

- Explore key features for making platform games
- Understand how tilemaps work
- Build a platform game in 90 seconds
- Undertake the Platform game challenge

<!--
In today's session we will continue our learning of construct and explore options for making platform games
-->

---

<!-- _class: lead -->

# 1. Platform Games

---

![](../assets/icons/platformer.png#ico-right)

# Platform Games

- Constructs features means it’s incredibly easy to create a platform game.
  - Platform movement
  - Solid objects
  - Jump through objects
  - Bullet
  - Fade and Sine
- There are numerous tutorials and examples that can offer a great starting point

---

# Platform Game Resources

![](../assets/icons/platformer.png#ico-right)

- Ultra video tutorial
- Examples Browser
  - Numerous demos and templates can be found by searching 'platformer'
- [How to make a platform game](https://www.construct.net/en/tutorials/platformer-game-2329)
- [Platform Behaviour Documentation](https://www.construct.net/en/make-games/manuals/construct-3/behavior-reference/platform)
- [A Beginnger's Guide to Construct](https://www.youtube.com/watch?v=mBJQSoAn49k&list=PL0GHpYtoYaLK9NZsKTrJdITXxOOhvy5Gl&index=2)

<!--
Useful resources for making platform games
-->
---

<!-- _class: question -->

![bg right:33% w:200](../assets/icons/conversation.png)


# Can we make a platform game in 90 seconds?

<!--
Demo a speed creation of a platform game
-->
---

<style scoped>p, ul li{ font-size: 26px;} </style>

![](../assets/icons/platformer.png#ico-right)

# Platform Game Demo

On Ultra you will find a video tutorial demonstrating how to create a platform game. This demo shows how to create the first level of the game where the player must collect 10 coins before finding the checkpoint. The demo introduces the following concepts:

- Drawing platforms / terrain with tilemaps
- Moving objects with the sine behaviour
- Using the solid behaviour to create platforms
- Using the platform movement behaviour to control the player
- Adding multiple enemies
- Alter player animations based on movement

---

# Tilemaps

![](../assets/icons/platformer.png#ico-right)

Tilemaps are a  object type in Construct 3 used to build tile-based levels or environments efficiently. They allow developers to draw game worlds using a grid of tiles from a single image called a tileset.

- Enhanced Performance
- Easy Editing
- Custom Collision Handling
- Tile IDs

<!--
A feature that can aid with the creation of platform games (and other game types is tilemaps). Tilemaps are a  object type in Construct 3 used to build tile-based levels or environments efficiently. They allow developers to draw game worlds using a grid of tiles from a single image called a tileset.

Performance: Tilemaps are optimized for rendering and collision detection, making them ideal for large levels compared to using individual sprites.

Editing: You can design tilemaps directly in the layout view using the Tilemap Bar, selecting and placing tiles from the tileset.

Collision Handling: Each tile can have custom collision polygons. Empty tiles are non-colliding by default.

Tile IDs: Each tile has a unique index (starting from top-left) used for scripting and runtime manipulation.

Positioning: Tilemaps use tile-based coordinates, which can be converted to layout coordinates using built-in expressions like TileToPositionX/Y.

[DEMO TILEMAPS]
-->

---

# Platform Game Challenge

![](../assets/icons/platformer.png#ico-right)

Work individually or in a small team (2–3 people) to design and build a short platformer using the features and resources introduced in class.

Your game should include:

- A collectible item that must be obtained to complete the level.
- At least one enemy that restarts the level upon collision with the player.

We will playtest each game at the end of the session

---

<!-- _class: main -->

# Up Next...
## Introduction to Multiplayer

<a style="text-decoration: underline; position: absolute; bottom: 40px; font-size: 20px; color: #272838;" href="https://www.flaticon.com" target="_blank" title="cloud service icons">Icons sourced from Flaticon</a>

<!--
Next week...
-->