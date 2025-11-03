---
marp: true
paginate: true
theme: webgames
header: YD-KR-TD
---


<!-- _class: main -->

# Web Games

## Week 6 - 3D & Multiplayer Features

<!--
Welcome to week 6
-->

---

![](../assets/icons/task-list.png#ico-right)

# Objectives

- Explore Constructs 3D Features
  - Z Elevation
  - 3D Object
  - 3D Camera
- Understand how Multiplayer works
- Get feedback on the first assessment

<!--
In today's session we will...
-->

---

<!-- _class: lead -->

# 1. 3D Features

---

![](../assets/icons/cube.png#ico-right)

# 3D in Construct

Primarily a 2D game making engine Construct has features that allow you to create 3D games

- Z Elevation
- 3D Object
- 3D Camera
- Third party addons

<!--
Whilst construct is a 2D engine it does have features to enable 3D including...
-->

---

![](../assets/icons/cube.png#ico-right)

# Construct Camera

![w:450 Diagram showing how the Construct engine camera works in 3D space](../assets/images/s6/construct-camera.png#right)

All construct games are actually rendered in a 3D world. The camera sits at a Z elevation of 100 and points down onto a 2D canvas at Z elevation 0.

---

![](../assets/icons/cube.png#ico-right)

# Z Elevation

![w:400 Diagram depicting Z elevation](../assets/images/s6/z-elevation.png#right)
Due to how all games are rendered in a 3D world Construct has always had some level of 3D provided through Z elevation

Z elevation allows you to move objects along the Z axis and therefore move objects closer of further away from the camera.

<!--
[DEMO]
-->

---

![](../assets/icons/cube.png#ico-right)

# 3D Shape

![w:500 Illustration of the basic 3D shapes in construct](../assets/images/s6/3d-shape.png#right)

- Adds basic 3D shape to games
  - Box, Prism, Cone & Wedge.
- Can add “textures” to the shape faces
- Depth of shape controlled via z height
- Collisions not affected by Z elevation changes

<!--
https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/3d-shape

[DEMO]
-->

---

![](../assets/icons/cube.png#ico-right)

# 3D Camera

![w:550 Screenshot from 3D camera demo in construct](../assets/images/s6/3d-camera.png#right)

The 3D Camera object allows you to modify the usual position and angle of the games camera and move it anywhere in the 3D world.

Moving the camera can quickly change a 2D game to 3D and completely modify the experience

<!--
https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/3d-camera

[DEMO]
-->

---

![](../assets/icons/cube.png#ico-right)

# Docs & Examples

![w:550 Screenshot from 3D zombie game demo in construct](../assets/images/s6/3d-zombie.png#right)

- [Using 3D in Construct](https://www.construct.net/en/tutorials/using-3d-construct-2746)
- Search '3D' and 'Z Elevation' in the examples browser

---

<!-- _class: lead -->

# 2. Multiplayer

---

![](../assets/icons/multiplayer.png#ico-right)

# Multiplayer in Construct

The multiplayer object in Construct provides features that allow real-time online multiplayer games.

The object makes use of **WebRTC API** to provide real-time communications and transmit game data between peers

---

![](../assets/icons/multiplayer.png#ico-right)

# Signalling

Scirra (the makers of Construct) provide a signalling server you can use for players to connect to each other. Players must connect to this signalling server before then joining a game “room”. The signalling server handles these connections.

Multiple games may be using this signalling server. To ensure players are allocated to the right game you need to give your game a unique name..

You can run multiple instances of your game (e.g. “Stable” vs “Beta” or “Europe” vs “America”).

<!--
Scirra (the makers of Construct) provide a signalling server you can use for players to connect to each other. Players must connect to this signalling server before then joining a game “room”. The signalling server will automatically assign players to rooms based on the player number a game is limited to. 

Multiple games may be using this signalling server. To ensure players are allocated to the right game you need to give your game a unique name when setting up multiplayer.

You can run multiple instances of you game and again the signalling server can allocate players based on an instance name (e.g. “Stable” vs “Beta” or “Europe” vs “America”). 
-->

---

<!-- _class: question -->
![bg right:33% w:200](../assets/icons/conversation.png)

# Why might you want to run multiple instances of your game?

---

![](../assets/icons/multiplayer.png#ico-right)

# Player Connections

![w:400 Comparison of construct events when using families versus when not using families](../assets/images/s8/multiplayer-connections.png#right)

The first player in a room becomes the host and acts as the server to transfer game data to other players.

All game information must be relayed through the host.

To keep games updated broadcast messages that are sent from the host to every player.

<!--
The first player in a room becomes the host and acts as the server to transfer game data to other players. This mean you can run multiplayer games without a need for your own dedicated host server. Once players are connected the signalling server is no longer used.

As one player in a game room will act as the host this means all game information must be relayed through them. No other players are directly connected to each other, they are only connected to the host.

To keep games updated so what is happening on each players screen you can make use of broadcast messages that are sent from the host to every player. Listening to these broadcast messages can allow you to update in game events.

-->

---

![](../assets/icons/multiplayer.png#ico-right)

# Connection Quality

It takes time for messages sent between players to arrive. Even players in close proximity should expect a delay in transmission (known as latency). The further the distance between players the larger this delay is likely to be.

Due to latency within games messages sent between players may arrive at inconsistently. Hosts will always have a slight gameplay advantage as they experience zero latency.

<!--
It takes time for messages sent between players to arrive. Even players in close proximity should expect a delay in transmission (known as latency) and this delay might be anywhere from 20 - 200ms. The further the distance between players the larger this delay is likely to be.

Due to latency within games messages sent between players may arrive at inconsistently, some may take longer than others and some might go missing completely. The multiplayer object in Construct has measures in place to correct these delays and compensate for them, however this won’t account for everything.

Hosts will always have a slight gameplay advantage as they experience zero latency.

-->

---
<style scoped>p, ul li{ font-size: 28px;} </style>
![](../assets/icons/multiplayer.png#ico-right)

# Multiplayer Flow

The lifecycle of a multiplayer game in Construct looks like this:

- Connect to signalling room and login
- Join a room
- Wait for peers to join and begin game
- Object data and meesages exchanged between peers
- Game ends and players leave the room

Games end instantly if the host leaves, but other players can leave at anytime

<!--
[SHOW DEMO PROJECT]
-->
---

![](../assets/icons/multiplayer.png#ico-right)

# Multiplayer Documentation

The events, conditions and expressions that come with the multiplayer object are extensive and creating multiplayer games can become complex.

For further reading I recommend the official documentation on the multiplayer object, as well as the tutorials and further examples provided by Construct...

[https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/multiplayer](https://www.construct.net/en/make-games/manuals/construct-3/plugin-reference/multiplayer)

---

![](../assets/icons/guide.png#ico-right)

# Multiplayer Demo

On Ultra you can find a video tutorial on implementing Multiplayer. This demo creates a multiplayer quiz game and demonstrates the following features

- Logging players in and connecting them via signalling server
- Sending messages between players
- File handling using the JSON object to read in quiz data

The demo materials include a video and commented Construct project file

<!--

[SHOW DEMO]

-->
---

<!-- _class: lead -->

# 3. Assessment Feedback

---

![](../assets/icons/assessment.png#ico-right)

# Contextualising Statement

The contextualising statement assessment is due this Friday:

**7th November, 11:59am**

Use the time in today's session to get feedback or [book a tutorial](https://outlook.office365.com/owa/calendar/BookingwithJakeHobbs@bathspa.ac.uk/bookings/)

<!--
For the next class you should prepare a short presentation that provides an overview of your proposed concept for the Playable prototype assessment. 

There is no requirement to have visual aids for the presentation, but you might find these useful to help explain the idea.

This presentation is a few days before your contextualising statement deadline so provides a good opportunity to get feedback before you need to submit a written version of your proposal. 
-->
---

![](../assets/icons/assessment.png#ico-right)

# Research & Development

Use the remainder of the session for research & development:

- Explore construct
- Rapid prototype game ideas
- Ideate for the playable prototype assessment
- Test mechanics for your playable prototype
- Get feedback on the Contextualising Statement assessment

---

<!-- _class: main -->

# Up Next...

## Prototyping

<a style="text-decoration: underline; position: absolute; bottom: 40px; font-size: 20px; color: #272838;" href="https://www.flaticon.com" target="_blank" title="cloud service icons">Icons sourced from Flaticon</a>

<!--
Next week...
-->