
# Intro to p5.js: Shapes, Color and Position (Olympic Rings)

## Sequence

1. [Context & Purpose](#context-&-purpose)
2. [Getting Started](#getting-started)
3. [Part 1: Shape](#part-1-shape)
4. [Part 2: Color](#part-2-color)
5. [Part 3: Documentation](#part-3-documentation)
6. [Close](#close)
7. [Practice](#practice)

## Context & Purpose 

This lesson is an introduction to a JavaScript library called `p5.js`, and while there's plenty we could say about that, we're going to stick to two main things:

1. It is, at its core, truly JavaScript. There are some abstractions that have been made to make it easier to write, but ultimately you're writing JavaScript.
2. If p5.js is your first programming language, it can be a little tricky to tell apart the p5 code (which will only work when you load in the p5 library) from the JavaScript code (which will work in almost any modern web browser).

Before digging in, it's important to know what types of things p5.js is capable of making, so here are some [simple examples](https://p5js.org/examples/) to browse through, and here are some more [complex ones](https://showcase.p5js.org/#/). 


## Getting Started 

This lesson will introduce how to code basic shapes, how to use color, how to position shapes on the p5.js canvas and how to use the p5.js reference. 

We will work through this lesson using the provided [repl.it template](https://replit.com/@IleiniMelendez/Intro-to-p5-21). Within the `index.html` file, the p5 library has already been imported along with the script (JS file) named `sketch.js`. 

In the `sketch.js` file, you should see the following starter code:

```JavaScript
function setup() {
  createCanvas(600, 500);
}

function draw() {
  background(230);
  // Delete the slashes on the next line to "uncomment" the ellipse
  // ellipse(50, 50, 50, 50)
}
```
Let's begin!

## Part 1: Shape

The code begins with `function setup()` which contains a line of code bound by curly braces. The code inside of these curly braces will run once when your page loads.

The second function is `function draw()` which contains more lines of code bound by curly braces. The code inside of these curly braces will run as a loop over and over as long indefinitely.

Take a moment to remove the `//` in front of the ellipse and see what happens in the preview window. 

#### Helpful Questions:
* What changed about our drawing?
* What happens if you change the first number from a 50 to something bigger, like 300?
* Beneath the ellipse, code: `console.log(ellipse)`. Open the preview window in a new tab and open the `inspect` tool. What type of information do you see in the console?
* What happens if you delete the 3rd number in the ellipse function?

The ellipse function takes in four arguments (numbers). The first and second number set the (x,y) position of the center. The third number sets the width of the ellipse and the fourth sets the height.

We will continue to use the `ellipse()` function to recreate the Olympic Rings symbol. Follow the commented instructions on `sketch.js` file to build out the Olympic Rings. Consider using the function `strokeWeight()` which sets the thickness of the border of the ellipse and the function `noFill()` which removes the interior color of the ellipse. To explore these functions in detail, use the `Search reference` tool in the [p5.js reference](https://p5js.org/reference/). 


## Part 2: Color

This is all lovely, but right now, our drawing is all in shades of grey, and while it's possibly recognizable in its current form, we we can do better.

So far we've called the `ellipse()` function, and we've also briefly touched on the `noFill()` function which makes our drawing tool do only outlines, not the filling of shapes, and the `strokeWeight()` function, which tells us how thick the lines should be when we draw.

To change the color of those lines, we need to call the `stroke()` function, and it takes three arguments:
1. The amount of RED, on a scale from 0-255
2. The amount of GREEN, on a scale from 0-255
3. The amount of BLUE, on a scale from 0-255

That order is sacred, so it's always RED, GREEN, BLUE (or RGB for short), and then the numbers we fill in create a sort of color recipe, telling us how much of each color to use.

#### Helpful Questions:
* What color is `stroke(255, 0, 0)`? How much red does it use? Green? Blue? (answer: all, none, none, respectively)
* What color is `stroke(0, 255, 0)`?
* What color is `stroke(255, 0, 255)`?


So that means that if we want to color our first ring blue, we'll need to add a `stroke(0, 0, 255)` function call right before we draw the ellipse.

At this point, the blue is VERY much the wrong shade and it's currently coloring ALL the rings, not just the one below our `stroke()` function call. It's helpful to find a color picker (there's one built right into Google) that can let you pick a color using your human eyes, and then it will tell you the recipe, rather than the other way around.

It is also important to note that the function `stroke()` is equivalent to dipping your brush in paint, or to picking up a new marker, and so the color will stay that way until you change it. So the only to give each Ring a different color is to carry on changing color between each `ellipse()`.

OPTIONAL: Color can take three numbers as an argument (an RGB recipe/formula), or one string (a message in quotes) with a color name inside. So `stroke("gold")` for the "yellow" Ring might work just as well.


## Part 3: Documentation

The people who are good at writing code have usually memorized a few key things that they use often, and then they look everything else up in **documentation**. Documentation is essentially a user's guide to writing code, and documentation exists for almost every language you might want to write in, and that includes p5.js.

Open up the [p5.js reference](https://p5js.org/reference/) and find the pages for the functions we've used so far (specifically ellipse, stroke, strokeWeight, noFill). With this new powerful resource in hand, the final Olympic Rings symbol should look like this: [Olympic Rings](https://cssi-p5-project-examples.glitch.me/rings.html).

## Close 

The best way to practice the skills you've learned in this lesson is to complete one of the three practice prompts below or the accompanying lab. If you get through the first 50 - 70% of the challenges in this practice portion or the lab, you are ready to move on to the next concept!

## Practice

Please Note: None of these challenges is "better" than any other, and the only wrong challenge is one that's too easy or too hard **for you**.

#### Mild

At this point, you have the rings ready to go. Try to create at least one more item from the Olympics either below or on the right hand side of your canvas. Some ideas might include:
* Gold, silver, and bronze podiums.
* An Olympic swimming pool.
* An Olympic track.
* A gold medal with a ribbon.
* A flag from one of the countries that competes at the Olympics.

#### Medium

Create a new project by "forking" the [Medium Template](https://replit.com/@IleiniMelendez/Medium-Practice-Intro-to-p5-21). In it, try to create an emoji and keep going until your partner can guess which emoji you're trying to draw.

#### Spicy

Create a new project by "forking" the [Spicy Template](https://replit.com/@IleiniMelendez/Spicy-Practice-Intro-to-p5-21#index.html). In it, create a scene - some place you'd like to visit. This might be a real or an imaginary place, and it might be a place you've been many times, or only ever seen in photos (like in the movie *Up*). Whatever the case, use your imagination to create something that excites or inspires you. 
