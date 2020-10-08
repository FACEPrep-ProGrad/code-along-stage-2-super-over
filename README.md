![Image description](https://i1.faceprep.in/ProGrad/prograd-logo.png)

# ProGrad Lab | HTML & CSS - Super Over Stage - II

## Learning Goals

In this exercise, the goal is to apply as many as possible of the concepts you've just learned:

- when and how to use different HTML tags,
- how to structure HTML page and add the content to it using _block and inline elements_,
- how to use flexbox to position elements on the page and
- how to style the page.

## Getting started

1. Fork this repo
2. Clone this repo

Whenever you create a first significant change, you should make your first commit.

3. Follow these [guidelines to add, commit and push changes](https://github.com/FACEPrep-ProGrad/general-guidelines-labs-project-builders.git).

## Instructions

### Introduction

In this exercise, you will continue from where you left previously. If you want, you can visit the [official page](https://faceprep-prograd.github.io/prograd-premier-league-super-over/) to pick up some of their styles, but this is not necessary; You already have all the assets for this version in the assets folder as well as the necessary text in the `index.html`.

Our goal is to get as close as possible to this:


Although it doesn't look too complicated, we will have to apply quite a few styles on our web page: set a background color on different elements, set a font weight (bold, normal), and position elements using our newly acquired skills in flexbox.

Now we are gonna work on the second part as said earlier:

- part II - add styles and make it perfect. 🎨

So let's get started!

**The assets we provided contain all the required images to successfully finish the exercise.**

### Part II - CSS/styles

#### CSS 1 | Setup

As you might recall, the first thing we have to do to add styles to our page is to create a `style.css` file and link it to our `index.html`.

So let's begin by creating a new file, in the same folder as our HTML file, and name it `style.css`. Now, link the file to the _index.html_.

_Hint_: In case you need to refresh your memory on how to do this, check _Day - 2 CSS_ lessons.

_Hint2_: You might want to consider adding the following line to your CSS, just to confirm that you have linked it correctly:

```css
body {
  background-color: red;
}
```

Refresh the page in Chrome, and if your _style.css_ is linked properly, the page should turn red. (*You can delete the *background-color* property we added as a test once you have confirmed it's working.*) :wink:

:::info
Before we move forward, add at the very top of your _style.css_ file the following lines:

```css
@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");

* {
	box-sizing: border-box;
	font-family: Montserrat;
    margin:0;
    padding:0;
}

body{
    font-family:"Montserrat";
    font-size: 10px;
    background: #edeef0;
}

/* General settings for font */
h1,
h3,
h4{
    font-weight: 700;
}

h2{
    font-weight: 500;
}
h1{
    font-size: 5em;
}
h2{
    font-size: 4em;
}
h3{
font-size: 2.5em;
}
h3{
    font-size: 1.8em;
}


p{
    font-size: 1.5em;
}
hr{
    width: 400px;
}
```

:::

This will be the default font you will be using on the entire webpage.

Now we are ready to start adding some styles to our page.

#### CSS 2 | The Navbar

In the first part of this exercise, you created the navbar. Now we have to add some styles to make it more like this:

![](https://i1.faceprep.in/ProGrad/css-1.png)

We'll help you style the part of the code we previously provided for you - the upper _list_ of the _nav_ tag.

```html
 <nav>
        <ul>
            <li class="logo-text">
                <img class = "logo-img" src="./assets/ipl_logo.png" alt=""/> </li>
            <li>
                <ul>
                    <li><a href="#teams" class="nav-link">TEAMS</a></li>
                    <li><a href="#fixtures" class="nav-link">FIXTURES</a></li>
                    <li><a href="./game.html" class="nav-link">GAME PLAY</a></li>
                    <li><a href="#pointstable" class="nav-link">POINTS TABLE</a></li>
                </ul>
            </li>
        </ul>
    </nav>
```
```css

.logo-text{
    font-size: 3em;
    font-weight: 700;
    color: #f05136;
}
.logo-img{
    height: 2em;
    width: 2em;
}
nav ul{
    display:flex;
    justify-content: space-between;
    align-items: center;
    list-style: none;
    padding: 10px;
}

nav ul li{
    margin: 0 20px;
}
.nav-link{
    font-size: 1.8em;
    text-decoration: none;
    color: black;
    cursor: pointer;
}

.nav-link:hover{
    color: #f05136;
}

```

_Useful information_:

- _background_:  #edeef0
- _navigation hover_: #f05136
- _font color_: black

As you can see, a lot of _flexbox_ is involved - if needed, revise the lesson again or sneak peek into the official docs (use your Google skills) or use this [resource](https://flexbox.help/) as a help.

Make sure to use flexbox at any time where you need to position elements on a specific place - practice as much as possible: the more you understand now, the easier will be later.

#### CSS 3 | The Header

![](https://i1.faceprep.in/ProGrad/css-2.png)

In this section, as you can see everything is _centered_. You can add some flexbox rules to the _id_ you attached to this section such is _display: flex;_ and _justify-content: center;_. But this is just the beginning - you still have to set _align-items_ and _flex-direction_.

```html
<header id="teams">
        <div>
            <article>
                <img class="logo" src="./assets/csk.png"/>
                <h4>Chennai Super Kings</h4>
            </article>
        </div>
    </header>
```
```css
#teams{
    background:  #9013fe;
    color:white;
    height: 450px;
    display:flex;
    justify-content: center;
    align-items: center;
}

.logo {
    width: 10vw;
    height: 10vw;
}
header div p{
    font-size: 2.5em;
    font-weight: 200;
}


#gameplay{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    
}

#teams div{
    display:flex;
    flex-wrap: wrap;
    justify-content: space-around;
    /* margin: top left bottom right */
    margin:10px 0;
    width: 100%;
}

#teams div article{
    background: white;
    color:black;
    height: 200px;
    width: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    text-align: center;
    border-radius: 10px;
}


```
_Useful information_:

- _background color_:#9013fe 


#### CSS 4 | The Section - Fixtures

![](https://i1.faceprep.in/ProGrad/css-3.png)

This section has pretty much the same layout as the previous - some code to be reused :wink:.

Again use a lot of flexbox to get the right position of elements - direction, justify-content, align-items.

**Inspect elements to get the right size of the font for each of them**. However, this is not a crucial thing, so don't spend too much time on it - focus on positioning primary.

```html
<section id="fixtures">
        
            <div class="flex container-fix">
                <a name="schedule"></a>
                <div class="flex qualifier">
                    <div class="flex set">
                        <div class="card1">
                            <img class="csk-img" src="./assets/csk.png" alt="CSK">
                        </div>
                        <h3>VS</h3>
                        <div class="card1 ">
                            <img class="kkr-img" src="./assets/KKR.png" alt="KKR">
                        </div>
                    </div>
                </div>
                <div class="flex semiFinal">
                    <div class="flex set">
                        <div class="card1">
                            <img class="csk-img" src="./assets/csk.png" alt="CSK">
                        </div>
                        <h3>VS</h3>
                        <div class="card1">
                            <img class="kxi-img" src="./assets/KXI.png" alt="KXI">
                        </div>
                    </div>
               </div>
                <div class="flex final">
                    <div class="flex set">
                        <div class="card1">
                            <img class="csk-img" src="./assets/csk.png" alt="CSK">
                        </div>
                        <h3>VS</h3>
                        <div class="card1">
                            <img class="mi-img" src="./assets/MI.png" alt="MI">
                        </div>
                    </div>
                </div>
            </div>
       </section>
```
```css
/* fixtures */
.container-fix{
    
    width: 94%;
    height: 90vh;
    margin: 1%;
    align-items: center;
    /* background-color: lightgray; */
    padding: 1%;

}
 .qualifier{
    width: 25%;
    height: 70vh;
    padding: 1%;
    margin: 1%;
    border: 2px solid rgb(247, 245, 245);
    border-radius: 5px;

}
.semiFinal{
    width: 25%;
    height: 35vh;
    padding: 1%;
    margin: 1%;
    border: 2px solid rgb(248, 245, 245);
    border-radius: 5px;
}

.final{
    width: 25%;
    height: 17vh;
    padding: 1%;
    margin: 1%;
    border: 2px solid rgb(248, 250, 249);
    border-radius: 5px;
}
.set{
    width: 95%;
    height: 15vh;
    padding: 1%;
    margin: 1%;
    border: 1.5px solid orangered;
    border-radius: 5px;

}
.card1{
    width: 40%;
    height: 13vh;
    padding: 1%;
    margin: 1%;
    
    background-color: white;
}
h3{
    margin: 5vh auto auto auto;
    border: 1px solid orangered;
    border-radius: 70px;
    background-color: orangered;
    color: white;
    transform: scale(1.00);
   box-shadow: 5px 5px 15px rgba(0,0,0,0.6);
}
#result{
  border:none;
  background-color: rgb(7, 131, 13);
}

.flex{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
}

.csk-img{
    width: 80%;
    margin-left: 10%;
}
.kkr-img{
    width: 45%;
    margin-left: 25%;
}
.dc-img{
    width: 70%;
    margin-left: 15%;
}
.kxi-img{
    width: 60%;
    margin-left: 20%;
}
.rcb-img{
    width: 48%;
    margin-left: 20%;
}
.rr-img{
    width: 70%;
    margin-left: 20%;
}
.shr-img{
    width: 70%;
    margin: 2vh auto auto 20%;
}
.mi-img{
    width: 100%;

}
```


#### CSS 5 | The Footer

![](https://i1.faceprep.in/ProGrad/css-4.png)

The footer part is very simple one. 
#### CSS 6 | The Gameplay

![](https://i1.faceprep.in/ProGrad/css-5.png)

Let us build the game play part. The code is given as an reference.

```html
 <div class="container">
        <div class="row">
            <div class="col">
                <img
                    src="./assets/csk.png"
                    alt=""
                    class="profile-icon"
                    height="150px"
                    width="150px"
                />
                <span class="name" id="team-1-name"></span>
                <div class="row round-runs" id="team-1-round-runs">
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                </div>
            </div>
            <div class="col">
                <div class="row score">
                    <span id="team-1-score"></span>
                    <span>-</span>
                    <span id="team-2-score"></span>
                </div>
            </div>
            <div class="col">
                <img
                    src="./assets/MI.png"
                    alt=""
                    class="profile-icon"
                    height="150px"
                    width="150px"
                />
                <span class="name" id="team-2-name"></span>
                <div class="row round-runs" id="team-2-round-runs">
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                    <span class="col">-</span>
                </div>
            </div>
        </div>
        <div class="row">
            <button
                id="strike-button"
                onclick="handleStrikeButtonClick()"
            ></button>
        </div>
        <div class="row" id="result" hidden></div>
    </div>
```
```css
@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");
* {
	box-sizing: border-box;
	margin: 0;
	font-family: Montserrat;
}
body {
	background: #9013fe;
	display: flex;
	justify-content: center;
	height: 100vh;
}
.container {
	background: white;
	display: flex;
	flex-direction: column;
	border-radius: 20px;
	width: 700px;
	padding: 50px;
	align-self: center;
}
.row {
	display: flex;
	flex-direction: row;
}
.col {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
.container > .row {
	width: 100%;
	justify-content: space-evenly;
}
.profile-icon {
    border-radius: 50%;
    border: 2px solid bisque;
}
.name {
	margin: 20px 0;
	font-size: x-large;
	font-weight: bold;
}
.score {
	margin: -80px 0 0;
	font-size: xx-large;
}
.score > span {
	margin: 0 5px;
}
.round-runs {
	font-size: xx-large;
	width: 200px;
	justify-content: space-evenly;
}

#strike-button {
	border: none;
	border-radius: 25px;
	background: linear-gradient(135deg, #c02425, #f0cb35);
	font-size: large;
	width: 300px;
	color: white;
	padding: 10px;
	margin-top: 50px;
	margin-bottom: -50px;
	outline: none;
}
#strike-button:hover {
	box-shadow: 0 0 10px 0 black;
}

#result {
	margin-top: 50px;
	background: linear-gradient(90deg, #f79d00, #64f38c);
	background-clip: text;
	text-transform: uppercase;
	font-size: xx-large;
	font-weight: bold;
	color: transparent;
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}

```
**Once again, a friendly reminder**: You don't have to wait to finish everything in order to follow the steps listed in the [guidelines](). In a moment when you've made a first significant step in working on this assessment. 

## Summary

In this exercise, you've built the complete design of a piece of the super over game project. If you managed to make it look anything like the original, good job! :trophy:

This concludes the HTML / CSS module. We are proud of you!

Happy Coding ProGrad ❤️!
