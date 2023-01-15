---
title: Let JS do the work!
date: 2022-12-05 08:00:00 +0100
categories: [JavaScript]
tags: [javascript,js]     # TAG names should always be lowercase
---

*Most coders out there have probably once become as excited as I got today when they injected a code from JavaScript into the HTML for the first time!*

This process happens by writing a classified **ul** in HTML (so we can point at it in JavaScript later), making an array of values, and generating the list items for each array item using JavaScript. Now we only need to address the **ul** and inject out **li** code inside it. 
In the code below you can see how I made a lis of my siblings and injected it to ul.siblings. 


```javascript
//get a refrence to the 'ul
const ul = document.querySelector('.siblings');

const siblings = ['vahid','vici', 'omid', 'negin','behnood'];

let html = ``;
siblings.forEach(person => {
    //create html template
html += `<li style="color: purple">${person}</li>`;
})

console.log(html);
ul.innerHTML = html;
```

Feel free to check out the both HTML and JavaScript codes for [My siblings list](https://jsfiddle.net/4cgs6kwy/1/).

