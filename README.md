# General Assembly - Project 02: The Rick and Morty.

## Overview

**The Rick and Morty** App is a tribute to the Rick and Morty cult TV Series. Visitors can view all 671 characters with their different properties, generate a random character, or filter characters based on different features (Alive/Dead, Human/Alien/Unknown, Male/Female/Genderless).

+ ### Timeframe

2 days.

+ ### Demo

<p align="center">
  <img src="https://i.ibb.co/j4fXDwJ/Project02.gif">
</p>

+ ### Deployed version

https://rickandmorty-ga.netlify.app/ 

<br />

## Team members

+ **Ineta Bliudziute:** https://github.com/inetabliu,
+ **Vania Tominc (me):** https://github.com/VaniaTominc.

<br />

## Table of contents
+ Brief
+ Technologies used
  - API
  - Frontend
  - Development tools
+ Installation
+ Process
  - Planning
    + Concept
    + Organisation
  - Frontend
    + Components
    + Styling
  - Project walkthrough
+ Bugs, challenges, wins
  - Bugs
  - Challenges
  - Wins
+ Extra features and key learnings
  - Extra features
  - Key learnings

<br />

## Brief

+ **Consume a public API** – this could be anything but it must make sense for your project.
+ **Have several components.**
+ **The app can have a router** – with several "pages", this is up to you and if it makes sense for your project.
+ **Include wireframes** – that you designed before building the app.
+ **Be deployed online and accessible to the public** (hosted on your public GitHub, not GA GitHub!).

<br />

## Technologies used

+ **API:**

  - https://rickandmortyapi.com/

+ **Frontend:**

  - React.js,
  - Axios,
  - Bulma,
  - SASS,
  - CSS3,
  - React Router DOM.

•	**Development tools:**

  - Visual Studio Code,
  - Insomnia,
  - Yarn,
  - Git & GitHub,
  - Google Chrome development tools,
  - Adobe Photoshop (for images),
  - Zoom,
  - Slack,
  - Netlify (deployment).

<br />

## Installation

+ Clone or download **GA-Project-02**.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129626931-b272f1ea-6bce-457f-9f12-6fa25e9ecf46.png">
</p>

+ Inside your Terminal move to your desired folder and use command:

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627061-e18195a9-873b-4e1c-a380-27a2545215e9.png">
</p>

+ Open project and open a terminal inside your chosen code editor:

  - In terminal type:
    + ```yarn``` to install yarn package,
    + ```yarn start``` to run localhost in browser.

<br />

## Process

+ ### Planning (day 1)

#### ➡️ Concept

Ineta and I wanted to create something fun and colourful. We wanted to find an API, which would have enough data to work with, but also an API that contains images. After browsing through many public APIs, we found “The Rick and Morty API”, a cheerful API that met all our searching criteria.

#### ➡️ Organisation

Since our hackathon lasted only two days, and it was the first time when we didn't code solo, we decided to realize our project from the start to the end by doing everything together. To realize this, we used VSCode live share, where one of us was typing. It helped us a lot because two pairs of eyes are better than one. We could easily spot whether anything was missing in our code, and we could debug our code faster. Moreover, it was a fantastic experience, as we could consolidate our knowledge with this coding approach.

+ ### Front-end (day 1 – day 2)

#### ➡️ Components

  - #### CharacterIndex & CharacterCard

For displaying all characters on the page, we created two components. It was done for the readability of the code itself. The main component is ```CharacterIndex```, and the ```CharacterCard``` component is called inside it.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627727-2199ab12-9fee-4309-866f-edc3cbb7016d.png">
</p>

In ```characterIndex``` component, we then called our chosen API with `axios` and got access to the data located in the database. A minor problem arose here, however, because the official Rick and Morty API allows the user to receive only up to 20 characters per page.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627770-27b7f715-e46f-4613-ac9e-0b672eb045d0.png">
</p>

After trying to find a solution to displaying all the characters, Ineta came up with a genius idea. We created an additional asynchronous function ```handlePageChange()``` that calls the next page. Each time the user presses the “show me more” button, the data of the next page appears on the page.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627918-9a3ca933-e3ea-490c-bc99-c631e8825671.png">
</p>
 
In the ```characterIndex``` component, we also created a filter function. The user can choose between different options, and depending on the selected option, the website only shows the data that meets the filter conditions.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627938-3c515389-0508-428b-8a2d-22119d7e2d67.png">
</p>
 
When writing the filter function, we followed the instructions in the official API documentation.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627957-3eb459ba-ddb8-497f-96bd-9225657cca54.png">
</p>
 
  - #### CharacterShow

If a user clicks on an individual character, he is redirected to a page with detailed information about that character. We got the character's data from the API based on his id.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129627967-d8dd6a8c-7039-461c-9766-ef3685383432.png">
</p>
 
  - #### RandomCharacter

I thought it would be fun to create a component, where a random character from Rick and Morty show appears. To achieve this I created a variable called `random` and stored it inside ```Math.floor(Math.random() * 671) + 1```. In the show, there are 671 characters. When API is called, the ID is called based on the number, created by a random variable.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129628041-61220f00-fd7b-420a-a951-08e9dbd01830.pngg">
</p>
 
#### ➡️ Styling and sound effects

This was the first project in which Ineta and I worked with the CSS framework Bulma. Bulma made styling and positioning HTML elements much easier and smoother. From the beginning of the project, we wanted to create an application in which the visitor would feel like he was in the real world of Rick and Morty. We wanted to achieve this by imitating the colour scheme from the original series. Our website is therefore in colours that are strongly present in the world of Rick and Morty. In order to make our website even more interactive, we added various special CSS effects and different sound effects.

+ ### App walkthrough

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129628113-e67ef55d-9aa4-4809-a482-15a048aed9fe.png">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129628561-872ce493-5f3d-475c-82c2-96e5c9431d21.png">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/83227280/129628137-fa4a55d0-1afd-401d-aa39-01e3d4acb705.png">
</p>
  
<br /> 

## Bugs, challenges, wins

+ ### Bugs

  - When the user clicks on “generate random character” and is redirected to the random character page, the page is refreshed twice. A similar thing happens when the user clicks on “go back to all characters”. It is probably due to the ```location.assign()``` method we used inside the Navbar component.

+ ### Challenges

  - Filtering. Our original plan was to show only characters that meet all three conditions on the page. If the user selects a man who is dead and alien, only characters who meet these conditions would be shown. Due to lack of time, we were unable to write this feature. So we had to be content with just showing characters who meet one condition.
  - How to bypass the official API, which does not allow the display of more than 20 characters per page. We solved this issue with an additional function that is triggered when the user presses the “show me more” button.

+ ### Wins

  - Pair programming. It made me more confident working with other people on projects.
  - Working with React and structuring the code into components.
  - Working with an API and dealing with the data returned.
  - Using CSS framework Bulma for the first time.
  - Create a unique website in 48 hours that puts even the most solemn people in a good mood for its cheerfulness.

<br />

## Future features and key learnings

+ ### Extra features

  - Making our website more mobile friendly.
  - Implementing the filter function properly. It would be cool if the characters could be filtered on the basis of more conditions, not only on one. 

+ ### Key learnings

  - First time working as a group/pair, and was a brilliant experience. I learned the importance of teamwork, and how to work productively as a pair. All in all, it was fantastic to share the same ideas and solve problems together.
  - Understanding how React works in the real world. I could finally understand what was going on under the hood of the library.
  - Using CSS framework Bulma for the first time. An awesome tool, though a little limited when it comes to customization.
