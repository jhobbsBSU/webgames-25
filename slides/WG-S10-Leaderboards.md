---
marp: true
paginate: true
theme: webgames
header: CL-OY-VW
---


<!-- _class: main -->

# Web Games

## Week 10 - Leaderboards

<!--
Welcome to week 10
-->

---

![](../assets/icons/task-list.png#ico-right)

# Objectives

- Learn you to implement a leaderboard in Construct 3
  - What is Supabase?
  - Why use it in games?
  - What is AJAX?
  - How Construct 3 uses AJAX
  - Using Supabase + AJAX together

<!-- Speaker notes:
In this session, we’re going to take at options for creating leaderboards in construct by making use of Supabase and AJAX. Alongside leaderboards these tools can enable inventorys, cloud saves and user profiles.” 
-->

---

<!-- _class: lead -->

# 1. Supabase

---

![](../assets/icons/storage.png#ico-right)

# What Is Supabase?

Supabase is an open-source backend-as-a-service (BaaS) built on:

- PostgreSQL Database
- Authentication
- File Storage
- Auto-generated REST APIs

It provides the backend infrastructure so you don't have to build a server.

<!-- Speaker notes:
Supabase is an opensource a backend-as-a-service, which means it gives you all the tools you need to manage data and users without having to write a traditional backend server.

At the core of Supabase is PostgreSQL. PostgreSQL is a powerful, open-source relational database. Unlike simpler key-value stores, PostgreSQL allows you to structure your data with tables, relationships, and constraints, which is essential when you have more complex game data. For example, you might want to store users, their scores, and achievements in different tables but still easily relate them together.

PostgreSQL also supports advanced features like indexes, queries, transactions, and functions, which make data retrieval fast and reliable even as your game grows. Using PostgreSQL through Supabase means you get all this power without needing to configure or maintain the database yourself.

In addition, Supabase adds authentication, so you can manage users securely, file storage for saving assets, and automatically generated REST APIs so your game can send and fetch data using HTTP requests. The main point is that you can focus on building your game, and Supabase takes care of the backend infrastructure for you.”
-->
---

![](../assets/icons/storage.png#ico-right)

# Supabase Key Features

- Full PostgreSQL database
- REST & realtime APIs automatically generated
- Authentication (email, OAuth, magic links)
- Row Level Security (RLS)
- Generous free tier

<!-- Speaker notes:
By using supabase you can access the following features.

First, the full PostgreSQL database gives you a reliable, scalable way to store structured data. This is important for things like leaderboards, user profiles, and game state. 

Next, Supabase automatically generates REST APIs and even supports realtime updates. That means your game can fetch data from the database and even receive live updates without having to constantly refresh or poll the server.

Authentication is built-in, which allows you to manage users easily, whether through email/password, OAuth providers like Google, or magic links. 

Security is also a major focus: Row Level Security, or RLS, allows you to control access to your data at the row level. This is critical for protecting sensitive information like player scores and therefore preventing cheating (to a degree).

Most importantly their is a generous free tier makes it accessible for small projects
-->
---
![](../assets/icons/storage.png#ico-right)

# Why Use Supabase for Games?

- Leaderboards
- Cloud save data
- User profiles
- Secure and scalable backend
- No server maintenance required

<!-- Speaker notes:
“The functionality afforded by Supabase provides you with the means to implement a range of features desireable in web games including, leaderboard, cloud saves, user profiles and more. 

Additionally, security and scalability are built in, so you don’t have to worry about players accessing each other’s data or your backend slowing down as your game grows. From the development perspective Supabase handles all the infrastructure so you can focus on the game itself. 
-->
---
<!-- _class: lead -->

# 2. AJAX

---

![](../assets/icons/loop.png#ico-right)

# What Is AJAX?

AJAX stands for:

- **A**synchronous
- **J**avaScript
- **A**nd
- **X**ML (but usually JSON today)

It allows your game to send & request Send data to a server without reloading the page

<!-- Speaker notes:
AJAX is a technique that allows a game or web app to communicate with a server without interrupting the user experience. The letters stand for Asynchronous JavaScript and XML, but in modern use we almost always work with JSON instead of XML because it’s easier to read and handle.

Asynchronous means that the game can send a request to the server and continue running while it waits for the response. This is crucial for keeping gameplay smooth—your game doesn’t freeze or reload just because it’s fetching data.

With AJAX, a game can send data to the server, such as a player’s score or settings, and request data from the server, like leaderboard entries or cloud saves. 
-->
---
![](../assets/icons/loop.png#ico-right)

# AJAX in Construct 3

Construct provides an **AJAX object** enabling you to:

- Perform GET, POST, PUT, DELETE requests
- Add custom HTTP headers
- Send or receive JSON
- Handle responses via events like:
  - `On completed`
  - `On error`

<!-- Speaker notes:
Construct provides an AJAX object that lets you make HTTP requests easily without writing any code.

You can use it to perform GET requests to fetch data, POST requests to send data, and even PUT or DELETE requests if your server supports them. You can also add custom HTTP headers, which is important when working with APIs like Supabase that require an API key or specific content types.

The AJAX object can send and receive JSON, which is the standard format we use to transfer data between the game and the backend. Construct also has events like ‘On completed’ and ‘On error’ to handle responses. This means you can react to data as soon as it arrives or handle any issues gracefully.

Basically, the AJAX object lets you connect your game to an external server like Supabase very easily, making it straightforward to send player scores or retrieve leaderboard data.

Beyond working with an external service like Supabase the AJAX object is useful for reading internal files within your game. For example you could have local JSON files with game data. The AJAX object allows you to retrive these files and parse the data into a JSON object. 
-->
---

# AJAX Workflow in Games

1. Player triggers an action (finish level, press button)
2. Game creates an AJAX request
3. Server processes it (Supabase REST API)
4. Server returns JSON data
5. Game handles result and displays it

<!-- Speaker notes:
Let’s walk through a typical AJAX workflow in games. First, a player does something that requires communicating with the server—maybe they finish a level or press a button to submit their score.

Next, the game creates an AJAX request and sends it to the server. In our case, that server will be Supabase, which receives the request and processes it according to its database and rules.

Once Supabase finishes processing, it sends back a response, usually as JSON (which means we will also need to use the JSON object). The game then handles this result, such as updating the leaderboard or showing a confirmation message to the player.

This workflow forms the backbone of most online game features, from leaderboards to cloud saves.
-->
---
![](../assets/icons/storage.png#ico-right)

# Supabase + AJAX = Easy Backend

Using both together lets you:

- Save scores to a database (POST)
- Fetch leaderboard (GET)
- Validate with database rules (RLS)
- Avoid building any custom backend code

This is ideal for Construct 3 and HTML5 games.

<!-- Speaker notes:
With Supabase handling the backend and AJAX managing communication from Construct 3, you can perform actions like saving a player’s score to the database using POST requests or fetching leaderboard data using GET requests.

Supabase also includes Row Level Security, or RLS, which ensures that each player can only access the data they’re allowed to see. This prevents cheating and protects user data.

The best part is that none of this requires writing backend code manually. You don’t have to set up servers, configure databases, or create APIs from scratch. This combination allows you to focus on building game features while still having a secure and scalable backend.
-->
---
![](../assets/icons/win.png#ico-right)

# Example Use Case

**Saving a player score**

- Construct sends a POST request to Supabase REST API
- Supabase inserts a row into your database

**Retrieving leaderboard**

- Construct sends GET request
- Supabase responds with JSON array of scores

<!-- Speaker notes:
Now let’s look at a concrete example of how this works in practice in the context of wanting to implement a leaderboard.

When a player finishes a level, Construct sends a POST request to the Supabase REST API. Supabase then inserts that new score as a row in the database. Later, when we want to display the leaderboard, the game sends a GET request to the same API, and Supabase returns a JSON array containing the top scores.

This pattern of POST and GET is central to almost all online game features, from leaderboards to cloud saves. It’s simple, consistent, and reliable, and once you understand it, you can start building more complex interactions with Supabase and AJAX in your games.
-->
---
<!-- _class: lead -->

# 3. Leaderboard Demo

<!--
In the next section we will have a live demo on implementing a leaderboard using Supabase. Before we begin are there any questions so far. 
-->
---

![](../assets/icons/storage.png#ico-right)

# Supabase Sign-up

<br/>
<br/>

### Go to [https://supabase.com/](https://supabase.com/) and create an account

*5 mins*

<!--
To follow along with the demo you will need a supabase account. Go to supabase now and sign-up
-->
---
![](../assets/icons/guide.png#ico-right)

# Leadboard Demo

<br />

Let’s take a look at leadboards in action.

You will find a starter file and key code snippets for creating the database on Ultra.

<!--
On ultra you will find resources to help you with the demo including a starter project file and key code snippets for setting up the database
-->

---

![](../assets/icons/guide.png#ico-right)

# Inventory Demo

An additional video demo is provided on Ultra that expands on the features discussed today and shows how to implement a player inventory. This demo includes:

- User Authentication
- POST requests (saving the inventory)
- GET requests (getting the inventory)
- PATCH requests (updating the inventory)

<!--
On ultra you will find an additional video demo that expands upon the features we've used for a leaderboard to demonstrate creating a user authenticated leaderboard.
-->
---

<!-- _class: lead -->

# 4. Project Development

---

![](../assets/icons/assessment.png#ico-right)

# Project Development

![w:500 Illustration of laptop with users hands on coffee mug and mouse](../assets/images/development.gif#right)

Use the remainder of the session to explore the demo materials and continue project development on your playable prototypes.

---

<!-- _class: main -->

# Up Next...

## Guest Talk - Paul West @ Fumb Games

<a style="text-decoration: underline; position: absolute; bottom: 40px; font-size: 20px; color: #272838;" href="https://www.flaticon.com" target="_blank" title="cloud service icons">Icons sourced from Flaticon</a>
<!--
Next week...
-->