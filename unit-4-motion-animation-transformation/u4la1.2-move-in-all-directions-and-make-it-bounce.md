---
description: How can I make objects move in different directions?
---

# U4LA1.2: Move In All Directions & Make it Bounce

### Overview && Teacher Feedback

In this learning activity, we create and animate an ellipse moving in multiple directions.&#x20;

This lesson builds off of the basics in U4LA1.1 as a natural extension - it can be easily combined with that lesson for students who work faster.

### Objectives

Students will be able to:

* Understand the different methods to speed up or slow down the movement of a visual element&#x20;
* Understand and use assignment operators&#x20;
* Move objects backward and diagonally&#x20;
* Move objects to random positions&#x20;
* Have objects bounce when they reach the edge of the canvas

### Suggested Duration

1-2 Days (45 - 90 minutes) _Depending on pacing of your class - you can easily do more practice with basic motion before making things bounce!_

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundation Student Outcomes

\[UNDER CONSTRUCTION]

### Vocabulary

* **Arithmetic operators** - This operator performs arithmetic between variables and/or values.&#x20;
* **Assignment operators** - This type of operator is used to assign values to JavaScript variables.

### Do Now/Warm Up:

Let's try something different: We want to make something move, but we want it to move in a different direction that what we did in the last lesson.

Create an ellipse that exists on the right side of your canvas. How could you animate this ellipse so that it moves from the right to the left (vs left to right like in the last lesson)?

### Motion Review

In the Do Now, students should have created something like the following code. Review this with them and ensure everyone is on the same page of using object literals, which will come in handy later:

```
var circ1

function setup() { 
  createCanvas(400, 400); 
  
  circ1 = {
    x:380,
    xSpd: 3
  }
}

function draw() { 
  background(220); 
  ellipse(circ1.x, 200, 20)
  
  circ1.x = circ1.x - circ1.xSpd //or circ1.x += circ1.xSpd
}
```

It's worth noting that some students may have made the speed a negative number and added it on line 16, and it's always good to reiterate that adding a negative is the same as subtracting a positive. This is also a good moment to review with students the **arithmetic operators**: if your students have been typing x = x + xSpd, they can shorten by writing x += xSpd, which means the same thing.

In fact, there are many **arithmetic operators** beyond just addition:

* x = x + 1 can be written as x += 1&#x20;
* x = x - 1 can be written as x -= 1&#x20;
* x = x \* 1 can be written as x \*= 1&#x20;
* x = x / 1 can be written as x /= 1

Make sure students understand that these aren't _more right,_ but they are generally considered more efficient as it's less to type, and they may see these in future code examples. (Although they can certainly choose which version they'd like to write in their own code based on what they are comfortable with!)

### Moving Vertically

So, taking what we learned, can we make a second circle that moves up and down instead of left or right? Give students \~3-5 minutes to try to create this in their own programs, and then review the code together (possibly by asking students to present). They should've added another circle like so:

```
var circ1
var circ2

function setup() { 
  createCanvas(400, 400); 
  
  circ1 = {
    x:380,
    xSpd: 3
  }
  
  circ2 = {
    y: 50,
    ySpd: 2
  }
}

function draw() { 
  background(220); 
  ellipse(circ1.x, 200, 20) //circ1
  ellipse(200, circ2.y, 20) //circ2
  
  circ1.x = circ1.x - circ1.xSpd //or circ1.x += circ1.xSpd
  circ2.y += circ2.ySpd
}
```

Now we should have two circles, one that moves up and down, and one that moves left and right. What if we wanted a shape to move diagonally? How could we make that happen?

### Move Diagonally

When something moves diagonally, it means that it is changing both its x and y position. So let's add a third ellipse in our program that will do just that! Take a pulse check of students - if they have ideas of how this would look, let them try for \~3-5 minutes before reviewing. Students who are not as confident in their algebra skills may need a little more walkthrough.

```
var circ1
var circ2
var circ3

function setup() { 
  createCanvas(400, 400); 
  
  circ1 = {
    x:380,
    xSpd: 3
  }
  
  circ2 = {
    y: 50,
    ySpd: 2
  }
  
  circ3 = {
    x: 20,
    y: 20,
    xSpd: 3,
    ySpd: 1
  }
}

function draw() { 
  background(220); 
  ellipse(circ1.x, 200, 20) //circ1
  ellipse(200, circ2.y, 20) //circ2
  ellipse(circ3.x, circ3.y, 20) //circ 3
  
  circ1.x = circ1.x - circ1.xSpd //or circ1.x += circ1.xSpd
  circ2.y += circ2.ySpd
  circ3.x += circ3.xSpd
  circ3.y += circ3.ySpd
}
```

With students, adjust the x and y speed so they can see how changing these values (essentially, the 'slope' of the line ellipse is animating in) changes the way it moves.

### \[OPTIONAL] Move at Random

**NB:** _This is a little bit of a different functionality than the other motions - you're welcome to teach it now, or after the bounce section, or skip it entirely. (You can also teach in a pull-group or as a future extension.) It's not necessarily \_difficult\_ it may just detract from some of the pieces happening earlier in the lesson that are more aligned with the 'make it bounce' section._

Alright, we have one final piece of motion to tackle, and then we are going to review how to make these shapes stay on the page. What if you want to make a shape that moves randomly? Time to add our fourth circle!

```
var circ1
var circ2
var circ3
var circ4

function setup() { 
  createCanvas(400, 400); 
  
  circ1 = {
    x:380,
    xSpd: 3
  }
  
  circ2 = {
    y: 50,
    ySpd: 2
  }
  
  circ3 = {
    x: 20,
    y: 20,
    xSpd: 3,
    ySpd: 1
  }
  
  circ4 = {
    x: 200,
    y: 200,
    xSpd: random(-3, 3)
    ySpd: random(-3, 3)
  }
}

function draw() { 
  background(220); 
  ellipse(circ1.x, 200, 20) //circ1
  ellipse(200, circ2.y, 20) //circ2
  ellipse(circ3.x, circ3.y, 20) //circ 3
  ellipse(circ4.x, circ4.y, 20) //circ 4
  
  circ1.x = circ1.x - circ1.xSpd //or circ1.x += circ1.xSpd
  circ2.y += circ2.ySpd
  circ3.x += circ3.xSpd
  circ3.y += circ3.ySpd
  circ4.x += circ4.xSpd
  circ4.y += circ4.ySpd
  circ4.xSpd = random(-3, 3) //pick a new random speed and direction
  circ4.ySpd = random(-3, 3) //pick a new random speed and direction
}
```

Note that because this shape is picking from negative and positive speeds, it will move in any direction and the speed/rate at which it moves is entirely up to the random nature of the program. (Try removing the background to watch this random walker make a fun design!)

### Make it Bounce

In the last lesson, we talked about how we can get our shapes to reset to the edge they started on using conditionals. But what if rather than reset, we want the shape to 'bounce?' (Here, we consider 'bouncing' to be reversing and going in the other direction.)

Let's think about how we could make that happen - this time, instead of changing the x or y position to 0, we just want it to _reverse direction._ How could we solve this? Give students \~3 minutes to think this through before you begin reviewing. Anticipate that most students will have an idea similar to the following:

```
if (circ1.x > 400){
  circ1.x -= circ1.xSpd
}
else {
  circ1.x += circ1.xSpd
}
```

This solution is a good thought, but it ultimately will not work. You can use console.log() to show exactly why - as soon as the x position is bigger than 400, it wil start subtracting, but once it's no longer bigger than 400, it will start adding, resulting in the circle getting stuck unable to move in either direction.

Rather than using an if/else, we just want to use an if that will change the direction of the motion. One thing we learned from the Do Now is that direction is controlled by our speed being negative or positive - so when we reach the edge, we want to take the opposite speed. If we think back to our math knowledge, we can recall that we get a number's opposite when we multiply it by -1. So our code could look like this:

```
//the earlier code is missing for readability, but this is the same sketch from the earlier examples!

function draw() { 
  background(220); 
  ellipse(circ1.x, 200, 20) //circ1
  ellipse(200, circ2.y, 20) //circ2
  ellipse(circ3.x, circ3.y, 20) //circ 3
  
  if (circ1.x > 400) {
    circ1.xSpd *= -1
  }
  
  circ1.x = circ1.x - circ1.xSpd //or circ1.x += circ1.xSpd
  circ2.y += circ2.ySpd
  circ3.x += circ3.xSpd
  circ3.y += circ3.ySpd
}
```

Now, this should bounce when the ellipse reached the far right side of the screen. Cool! But what if we want it to both off both sides? We can simply modify the if statement:

```
if (circ1.x > 400 || circ1.x < 0) {
    circ1.xSpd *= -1
  }
```

...recall that || is the JavaScript operator for 'or.' Now, our ellipse should bounce as it reaches either side of the canvas!

Ask students to create a conditional that will work for circle 2 and then circle 3 - this can be challenging with the diagonal, but they can do it! After allowing 5-10 minutes of work time, review with students.

### \[OPTIONAL] Student Practice/Challenge

You’ve been asked to create an animated simulation of cars traveling through a busy intersection in NYC.

![](https://lh4.googleusercontent.com/nZbcR3r0pJmPmDv7O4Lpkg6hZ7GSPrPrVH4npDwQ\_VxGZCEtkH\_P-AlbYrPOuIb0n7cm8kGAkl1HLlrgV3JsaZHs-PWNECPaGN2MYlCO8XK0EcZSQx0S3uZ0aC4hFm8LO13hHw33)

Take your previous exercise from lesson #1 and modify it so that you have simple shapes (simulating cars) that move in multiple directions and with different speeds.

You should have at least one of each:

* Left / right&#x20;
* Down / up&#x20;
* Diagonally&#x20;
* Random speed or fixed speed
* Make multiple shapes reset or bounce as they reach the end of their 'route'

Here’s a painting by Dutch-born artist Piet Mondrian from 1942 called “Broadway Boogie Woogie”. This painting is inspired by clear real-world examples: the city grid of Manhattan, and the Broadway boogie-woogie, a type of music Mondrian loved.

![](https://lh5.googleusercontent.com/J3TgvaYvT0HMM0YDBWjR\_SStjfvn89XS0TlJ1eV8ykDPvYlUAiJjE\_lMRlsvVH2btmITbbdi9IUH-vbtK5nHQBXoTkdGGcPgYsxWojcikrmwkr4s9Ze-2WjLaZ1EqX5AuCcYkmv2)

How could you use colors, shapes, and animation techniques to code a sketch that creatively simulates a busy intersection?

### Wrap Up

The most important part of this lesson is leaving with a solid understanding of the logic it takes to get a shape to bounce off the edge of the canvas, as this is necessary for the next mini project.&#x20;

You can review that logic as the wrap up.

### Extension

There is no real extension for this lesson, outside of making the code along/group/partner sections more independent for classes whose logical reasoning skills can support that. This lesson leads directly to the DVD Mini Project for this learning activity, which can be extended all you’d like!
