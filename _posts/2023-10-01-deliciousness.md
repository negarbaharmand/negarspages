---
title: "Introducing Deliciousness: A Multipage React App for Food Enthusiasts"
date: 2023-10-01 08:00:00 +0200
categories: [JavaScript, React, API]
tags: [javascript, react] # TAG names should always be lowercase
---

Hello there! I'm excited to introduce you to my latest project, Deliciousness, a multipage **React app** that combines my love for coding and food recipes. As a junior-level developer, I'm constantly learning and experimenting, and this app is a testament to my journey. You can check out the app repository on GitHub [here](https://github.com/negarbaharmand/deliciousness.git) and try it live [here](https://negarbaharmand.github.io/deliciousness/).
![App overview](/assets/images/deliciousness-page-overview.png)

Deliciousness is structured into two main packages: "component" and "pages." This design choice reflects the separation of concerns and modularity, making the app easier to manage and extend as it grows.

![Github overview](/assets/images/deliciousness-github.png)

### Dependencies:

To build Deliciousness, I used a set of key dependencies that played a crucial role in its development:<br>
**React:** The app's foundation, providing a powerful and efficient way to build user interfaces.<br>
**React Router:** For seamless navigation and page routing, making the app user-friendly and intuitive.<br>
**styled-components:** A CSS-in-JS library that allows me to easily style components, improving code maintainability.<br>
**framer-motion:** This library brings animations to life, enhancing the user experience and making the app more engaging.

### Key Components:

Let's take a quick look at some of the key components in the "component" package:<br>
**Category:** This component displays food categories like Italian, American, Thai, and Japanese, using stylish icons. It also uses React Router's NavLink for active styling.<br>
**Popular, Search, Veggie:** These components cater to various aspects of the app. "Popular" showcases popular food picks, "Search" lets users search for recipes, and "Veggie" displays vegetarian recipes. These components are animated with framer-motion for a visually appealing experience.

### Routing and Navigation:

Deliciousness leverages **React Router** for seamless navigation between pages. **NavLink** ensures that active links are styled, enhancing user interaction.

### API Integration:

The app integrates with the **Spoonacular API** to fetch food recipes. I implemented **local storage caching** for popular and vegetarian recipes to reduce API requests and improve performance.<br>

Building Deliciousness has been an exciting journey for me, and it has allowed me to put my skills to the test, learn new concepts, and create something enjoyable.
