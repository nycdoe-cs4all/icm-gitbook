---
description: How can I use sliders to control elements of my program?
---

# Using Sliders

### When to Use This Extra

This is a brief lesson that can be used anytime after students have created variables. If you make an easy-to-follow guide, this can even be something that could be used as an **extension or sub lesson** when you want students to explore but are not necessarily available to offer guidance.

* **Earliest/Most Aligned:** After U1LA2.2: Custom Variables in p5.js

### Overview && Teacher Feedback

This lesson is going to be a very brief overview of sliders that will allow students to start engaging with an HTML DOM element very early on. They don't need to understand every single piece to get the basics and get their slider working!

As mentioned above, this is fairly straightforward, and it could easily be given as an extension or sub lesson if you create a guide that is easy for students to follow. Essentially, keep this one in your back pocket and feel free to pull it out whenever your students need a little something extra to keep their interest!

### Objectives

Students will be able to:

* Create sliders to control values in their program
* Understand the basic functionality of sliders

### Suggested Duration

\~1 Period (45 Minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

### Vocabulary

**sliders -** an HTML element you can add to your page to control values of a variable by clicking/dragging the dot on the slider.

### Resources

* [HTML Sliders](https://p5js.org/examples/dom-slider.html) (Reference Sheet)
* [Interacting with DOM using Sliders ](https://youtu.be/587qclhguQg)(Youtube Video)

### Assessments

Slider Art Assignment (Formative)

### Do-Now/Warm Up

**Display on board:** Describe how we have set and changed variable values in the past. Are there interactions we may want to allow users to have that could change the value of different variables?

_Allow students time to think and brainstorm and clarify as necessary that this could be clicking, typing, etc - have them think to ways they have interacted with other apps and websites!_

### Introducing Sliders

Today, we are introducing a new thing that we can use in our sketches to help control values in our programs: the slider! Sliders are technically an HTML element that we use to control parts of our JavaScript code. (This is part of the HTML Document Object Model, or HTML DOM, that we may explore at various points in the year.)

Sliders look a bit like this:

![Three sliders labeled red, green, blue at different levels on a lavender screen.](<../.gitbook/assets/Screen Shot 2022-03-21 at 10.42.01 AM.png>)

We are going to recreate essentially this example to control the background of a sketch together, so let's open up a blank editor so we can get started. **NB:** _You are basically recreating the example from the reference sheet, so feel free to use that as guidance!_

**Sliders always have three parts:**

1. Defining a variable and setting it to a slider. _This can have ANY name!_&#x20;
2. Giving the slider a (x,y) position on your page.&#x20;
3. Declaring a variable in your program that takes the value from the slider. _Ideally, we do this in draw because it is always running and thus always updating based on new slider values._

Once students have their blank editor open, begin coding along this example of making a slider that controls just the red value of their background:

```
var redSlider

function setup() {
  createCanvas(400, 400);
  redSlider = createSlider(0, 255, 50)
  redSlider.position(10,10)
}

function draw() {
  r = redSlider.value()
  
  background(r, 220, 220);
}
```

Now let's think about what's happening:

1. On line 1, we create a variable to hold our slider.
2. On line 5, we create our slider and save it in the variable redSlider.
3. The (0, 255, 50) stand for the LOWEST value of the slider, the HIGHEST possible value of the slider, and the STARTING value of the slider. Ask students to change some of these values - starting with the STARTING value - to see how it changes things. Make sure students understand that THESE sliders go from 0 - 255 because that's our color number range - if the slider controlled something else, the range could look different!
4. On line 6, we are giving a position to the slider. Without this, you will notice the slider exists under the canvas. Similar to step 3, ask students to change these values to move the slider around the page.
5. And finally, on line 10, we make a variable to capture the value of the slider and use that variable in our background (on line 12).

Tah-dah! Now, ask students to create _two more sliders_. They can either do this independently or, ideally, they can work with a partner where each will take turns creating a slider while the other navigates them. The two remaining sliders should work to control the green and blue values of the background. When they are done, they should have three distinct sliders on their screen.

### Sliders & Modern Art Challenge

Look at the fine art examples below. Try to recreate one in p5.js - then, try to make it interactive using the slider AND other elements that you have learned about! (Each slide shows several different works - try to think about just ONE work from an artist, or think about your favorite elements of each that you could combine)

**Note:** We have used sliders to control color, but they can control _anything with a numeric value._ What could you have them control that _isn't_ a color? How could this affect your final product?

![Alexander Calder Art](https://lh6.googleusercontent.com/E3P\_nrw3hM30Fb4F2UYb6DlDQLl00nS43f4ol5pKBYu1AxwvALUXYLDxthdHgKNpK-DL43DcpoFW5N3cu0334kDUGx1SVNKSswUATe1VS-yTLdSUVYngcTV\_VL7ICUwdSc0qci\_a)

![Mary Corse Art](https://lh4.googleusercontent.com/yhBoomMi7reAObYVY7u2lFhTHlY1FNmwjl9tL65haZpY7WXEBACgZwB5dAEpBI93IVTgRl3SAg0FpnB1XUrACTjnpULyEKD0c6JoI8G6rmpW8FGBHIrDjt\_5MVDfBjsdcmIkjI9U)

![Olafur Eliasson Art](https://lh6.googleusercontent.com/zIBAkKzryQcXV8dTlIYKYm7TG4kGsi3meOgxgblRHK-LuU\_5agsAJ1c3l7KDzx\_K8eHhFQRct8td63tD2Gpj56QrxvYCHaEa5xuMzQrtfxoJT9KyV4vL1KkWZREmY3a9YaHNcQrg)

![Dan Flavin Art](https://lh3.googleusercontent.com/sAHNnDQ32qQz9q3s0VsrLMWJCXKIma2lme2Z2wA1gc5AGKKWu74wEENf7HlXO---0mBc19t1Cihh8EUHJkYZ1gDPzElj-McQ6T-qUcaibIslSo0nuFuguwVUJ\_eVmrwPxCDlDD5C)

![Carmen Herrera Art](https://lh5.googleusercontent.com/Wj3VvQtOtHO2ba6Y9ToC4MBFG5dCiI8DJg\_BMUtq-hxC4tr-Nix4qEGwwubGx92hJ3dGGkEyRRVOdXCDT0Z2P7Zdl9SaFkh8HnkqS2zWgSwilEmMfxkU9EI45WU-xq7IqSlKBjm9)

![Vassily Kandinksy Art](https://lh3.googleusercontent.com/1XUBuHSpjQO2pPJlrw5hWcFV4gmjQ5oSQvE34WEScFjaoCZAOMZUalL6TF7JylONC4r3q\_jY8hb5xAzljecDThXGMZs\_Vorcdg5q11N7DNIbRvyjehqvCmAtDYBTjcoMu9zrHIQH)

### Wrap Up

Conclude with a gallery walk activity in which students circulate and get a chance to play with as many projects as possible by manipulating the sliders. Ask students to leave feedback either as code comments or on post its lefts near the computers.

### Extensions

Sol Le Witt is an artist famous for large installations, but many of them were not actually created by the artist - rather, the artist created instructions and would send the instructions to museums for them to recreate. (Now that he is deceased, this is the only way to recreate his work!)

Ask students to follow a Sol Le Witt tutorial from one of the following resources, or to try to create their own Sol Le Witt style tutorial in pseudocode that other students could follow:

1. [Whitney Kid's Tutorial](https://whitney.org/education/families/kids-art-challenge/sol-lewitt)
2. [SF MoMA Tutorial](https://www.sfmoma.org/read/drawing-with-instructions/)
3. [National Gallery of Art Tutorial](https://www.nga.gov/learn/teachers/lessons-activities/new-angles/sol-lewitt.html)

