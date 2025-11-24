---
marp: true
paginate: true
theme: webgames
header: DP-OB-CG
---


<!-- _class: main -->

# Web Games

## Week 9 - Saving & Loading

<!--
Welcome to week 9
-->

---

![](../assets/icons/task-list.png#ico-right)

# Objectives

- Explore options for saving & loading data
  - Local Storage
  - Save & load actions
- Work on playable prototype projects

<!--
In today's session we will look at different options for saving and loading data in your projects
-->

---

<!-- _class: lead -->

# 1. Local Storage

---

![](../assets/icons/storage.png#ico-right)

# Local Storage

The localStorage object allows you to store data locally on the user’s device. Within a web game a typical use case would be to store a personal best high score.

As the name suggests local storage is saved to the users device, so is only accessible ‘locally’ to that user. However, as local storage is saved to the device, rather than left ‘in the cloud’ this data is accessible when offline.

<!--
Documentation: https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/local-storage
-->
---

![](../assets/icons/storage.png#ico-right)

# Local Storage Basics

- Local storage values are stored under named ‘keys’
- Can set or get the values stored under these keys
- Events occur asynchronously - need to wait for them to complete

<!--
The basics of utilising local storage is straightforward. Values you want to store are saved under names keys. We can then reference these key names to set or get the values stored in them. For example we might create a key named score and store the value 1000. Reading and writing data to local storage does not complete immediately, so you should listen for on get and on set events to ensure action has been completed before trying to then access the data.

-->
---

![](../assets/icons/guide.png#ico-right)

# Local Storage Demo

Let’s take a look at local storage in action. For this we will use the Endless Runner game created in week 4.

You will find a starter file and accompanying written guide for this demo on Ultra.

---

<!-- _class: lead -->

# 2. Save and Load

---

![](../assets/icons/save.png#ico-right)

# Save and load actions

Construct has some simple Save and Load system actions that allow you to save the state of the game with little effort.

When run, the save action saves the current state of all game objects and variables meaning that when running the load action we can return to this saved state.

<!--

Construct has some simple Save and Load system actions that allow you to save the state of the game with little effort. When run, the save action saves the current state of all game objects and variables meaning that when running the load action we can return to this saved state.

Saved game data is stored on disk by the browser, either to WebStorage or IndexedDB, this means if the users clears their cache the saved data still persists. However saved data is unique to the browser it is saved to (e.g. if a user switches from chrome to firefox they will be unable to access their saved game). 

Each saved game is saved to a slot and we can have multiple slots saved to separate files. Currently once a slot is created Construct provides no way of clearing this data, although we can rewrite new data to these slots, and keep track of which slots are in use. This allows you to mimic the clearing of slots and give the user control over which slots are available for use, which is covered in the advanced demo.

-->
---

![](../assets/icons/guide.png#ico-right)

# Save & Load Demo

Let’s take a look at the save and load functionality in action. For this we will use the Platform game created in week 5.

You will find a starter file and accompanying written guide for this demo on Ultra.

---

![](../assets/icons/save.png#ico-right)

# Multiple Save Slots

By combining local storage and the save and load actions it is possible to create 'save slots' in construct. This more advanced method of handling saves  is demonstrated in a video tutorial which continues on from the basic demo we've just covered.

In addition to showing how to create multiple save slots the video demonstrates the use of Global UI elements, useful for having persistent UI layers across different layouts.

---

<!-- _class: lead -->

# 3. Project Development

---

![](../assets/icons/assessment.png#ico-right)

# Project Development

![w:500 Illustration of laptop with users hands on coffee mug and mouse](../assets/images/development.gif#right)

Use the remainder of the session to explore the demo materials and continue project development on your playable prototypes.

---

<!-- _class: main -->

# Up Next...

## Creating Leaderboards

<a style="text-decoration: underline; position: absolute; bottom: 40px; font-size: 20px; color: #272838;" href="https://www.flaticon.com" target="_blank" title="cloud service icons">Icons sourced from Flaticon</a>
<!--
Next week...
-->