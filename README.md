OVERVIEW

The Rick and Morty App is a tribute to the Rick and Morty cult TV Series. Visitors can view all 671 characters with their different properties, generate a random character, or filter characters based on different features (Alive/Dead, Human/Alien/Unknown, Male/Female/Genderless).

Timeframe

2 days.

Demo

[img]https://i.ibb.co/j4fXDwJ/Project02.gif[/img] 

Deployed version

https://rickandmorty-ga.netlify.app/ 

TEAM MEMBERS

Ineta Bliudziute: https://github.com/inetabliu
Vania Tominc (me): https://github.com/VaniaTominc 

TABLE OF CONTENTS
Brief
Technologies used
API
Frontend
Development tools
Installation
Process
Planning
Concept
Organisation
Frontend
Components
Styling
Project walkthrough
Bugs, challenges, wins
Bugs
Challenges
Wins
Extra features and key learnings
Extra features
Key learnings

BRIEF

Consume a public API – this could be anything but it must make sense for your project.
Have several components.
The app can have a router – with several "pages", this is up to you and if it makes sense for your project.
Include wireframes – that you designed before building the app.
Be deployed online and accessible to the public (hosted on your public GitHub, not GA GitHub!).

TECHNOLOGIES USED

API

https://rickandmortyapi.com/

Frontend

React.js
Axios
Bulma
SASS
CSS3
React Router DOM

Development tools

Visual Studio Code
Insomnia
Yarna
Git & GitHub
Google Chrome development tools
Adobe Photoshop (for images)
Zoom
Slack
Netlify (deployment)

INSTALLATION

Clone or download GA-Project-02.



Inside your Terminal move to your desired folder and use command:



Open project and open a terminal inside your chosen code editor:

In terminal type:
yarn to install yarn package,
yarn start to run localhost in the browser.

PROCESS

Planning (day 1)

Concept

Ineta and I wanted to create something fun and colourful. We wanted to find an API, which would have enough data to work with, but also an API that contains images. After browsing through many public APIs, we found “The Rick and Morty API”, a cheerful API that met all our searching criteria.

Organisation

Since our hackathon lasted only two days, and it was the first time when we didn't code solo, we decided to realize our project from the start to the end by doing everything together. To realize this, we used VSCode live share, where one of us was typing. It helped us a lot because two pairs of eyes are better than one. We could easily spot whether anything was missing in our code, and we could debug our code faster. Moreover, it was a fantastic experience, as we could consolidate our knowledge with this coding approach.

Front-end (day 1 – day 2)

Components

CharacterIndex & CharacterCard

For displaying all characters on the page, we created two components. It was done for the readability of the code itself. The main component is CharacterIndex, and the CharacterCard component is called inside it.



In characterIndex component, we then called our chosen API with axios and got access to the data located in the database. A minor problem arose here, however, because the official Rick and Morty API allows the user to receive only up to 20 characters per page.



After trying to find a solution to displaying all the characters, Ineta came up with a genius idea. We created an additional asynchronous function handlePageChange() that calls the next page. Each time the user presses the “show me more” button, the data of the next page appears on the page.



In the characterIndex component, we also created a filter function. The user can choose between different options, and depending on the selected option, the website only shows the data that meets the filter conditions.



When writing the filter function, we followed the instructions in the official API documentation.



CharacterShow

If a user clicks on an individual character, he is redirected to a page with detailed information about that character. We got the character's data from the API based on his id.




RandomCharacter

I thought it would be fun to create a component, where a random character from the Rick and Morty show appears. To achieve this I created a variable called random and stored it inside Math.floor(Math.random() * 671) + 1. In the show, there are 671 characters. When API is called, the ID is called based on the number, created by a random variable.



Styling and sound effects

This was the first project in which Ineta and I worked with the CSS framework Bulma. Bulma made styling and positioning HTML elements much easier and smoother. From the beginning of the project, we wanted to create an application in which the visitor would feel like he was in the real world of Rick and Morty. We wanted to achieve this by imitating the colour scheme from the original series. Our website is therefore in colours that are strongly present in the world of Rick and Morty. In order to make our website even more interactive, we added various special CSS effects and different sound effects.

App walkthrough





BUGS, CHALLENGES, WINS

Bugs
When the user clicks on “generate random character” and is redirected to the random character page, the page is refreshed twice. A similar thing happens when the user clicks on “go back to all characters”. It is probably due to the location.assign() method we used inside the Navbar component.

Challenges
Filtering. Our original plan was to show only characters that meet all three conditions on the page. If the user selects a man who is dead and alien, only characters who meet these conditions would be shown. Due to lack of time, we were unable to write this feature. So we had to be content with just showing characters who meet one condition.
How to bypass the official API, which does not allow the display of more than 20 characters per page. We solved this issue with an additional function that is triggered when the user presses the “show me more” button.

Wins

Pair programming. It made me more confident working with other people on projects.
Working with React and structuring the code into components.
Working with an API and dealing with the data returned.
Using the CSS framework Bulma for the first time.
Create a unique website in 48 hours that puts even the most solemn people in a good mood for its cheerfulness.

FUTURE FEATURES AND KEY LEARNINGS

Extra features

Making our website more mobile friendly.
Implementing the filter function properly. It would be cool if the characters could be filtered on the basis of more conditions, not only on one. 

Key learnings

First time working as a group/pair, and it was a brilliant experience. I learned the importance of teamwork, and how to work productively as a pair. All in all, it was fantastic to share the same ideas and solve problems together.
Understanding how React works in the real world. I could finally understand what was going on under the hood of the library.
Using the CSS framework Bulma for the first time. An awesome tool, though a little limited when it comes to customization.
