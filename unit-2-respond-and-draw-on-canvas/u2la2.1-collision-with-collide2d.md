---
description: What visual cues tell me where my mouse is?
---

# U2LA2.1 - Collision with Collide2D

### Overview

This learning activity introduces if statements and boolean expressions, both simple and compound. They are applied to locating the mouse on the screen and creating circular buttons that the user can hover and click on.

At this point, students have seen mouseX and mouseY and should understand that they hold a changing value. This is theoretically enough to get through the Do Now - however, if students are still struggling greatly (with hints!) after 5 minutes, you can turn this into a Code Along. It’s also recommended students work with partners during the Do Now.

It is up to you to decide if you would like this activity to be pair programmed or done individually.

### Objectives

Students should be able to:

* Understand that conditionals can tell us if the mouse is touching a shape&#x20;
* Utilize the collide2D Library&#x20;
* Use conditionals to create hover reactions

### Suggested Duration

\~2-3 Periods (45 minute each)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundation Student Outcomes

**Abstraction**

* Describe different things I tried in order to achieve a goal.&#x20;
* Explain why I chose to include the specific components of my prototype over others.
* Explain characteristics or patterns that informed a function or an interface I created.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.
* Demonstrate the benefit of using an event, conditional or loop in my prototype.&#x20;
* Explain how a function I prototyped can be used by someone else.&#x20;
* Teach someone the difference between instructions and an algorithm.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.

### **Vocabulary**

* Hover - when the mouse cursor is moved over an object&#x20;
* Hover reaction - something the object does in response to the cursor being moved over it&#x20;
* Collide2D - a library of boolean functions that check if shapes are colliding&#x20;
* User experience - peoples’ attitude**s** and feelings about using a product or project

### Planning Notes

|                                                                                                            Planning Notes                                                                                                            |     Materials Needed     |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------: |
| <p>These lessons involve using an external library; you can certainly teach these lessons without, but it does become more difficult.</p><p></p><p>Make sure you have reviewed and understand using Collide2D before the lesson!</p> | **Chart paper, markers** |

### Resources

* [Collide2D Library Documentation](https://github.com/bmoren/p5.collide2D) | [Blank p5.js Sketch w/ Collide2D Linked ](https://editor.p5js.org/cs4all/sketches/H6r7sf5IW)([p5 editor](https://editor.p5js.org/cs4all/sketches/H6r7sf5IW) | [repl.it](https://replit.com/@qrtnycs4all/Blank-Sketch-with-Collide2D-Library-Linked#script.js))
* [Intro to Collide2D with Ellipse](https://youtu.be/uqkuZ0K52Xc) (YouTube Video) | Optional Starter Code ([p5 editor](https://editor.p5js.org/cmorgantywls/sketches/k6eKf6WG7) | [repl.it](https://replit.com/@qrtnycs4all/U2LA21-Intro-to-Collide2D-with-Ellipse-Starter-Code#script.js))
* Lesson/Practice Starter Code ([p5 editor](https://editor.p5js.org/cs4all/sketches/2h4aTWZsB) | [repl.it](https://replit.com/@qrtnycs4all/U2LA21-Collide-2D-LessonPractice-Starter-Code#script.js))
* [Collide with Other Shapes](https://youtu.be/no83IrSteD4) (Youtube Video) | Starter Code ([p5 editor](https://editor.p5js.org/cmorgantywls/sketches/aUZv6Jll7)| [repl.it](https://replit.com/@qrtnycs4all/Collide-with-Other-Shapes-Practice-Starter-Code#script.js))
* Video tutorial: [3.3 else, and else if, AND and OR](https://www.youtube.com/watch?v=r2S7j54I68c)

### Assessments

Assess the Do Now assignment. Check for the ability to demonstrate the benefit of using a conditional and a loop in their prototype.

Assess the learning activity. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Create a program that can have different outputs depending on inputs.

Assess the Wrap Up assignment. Check for the ability to describe different things they tried in order to achieve this goal.

### Do Now/Warm-Up (5 Minutes)

Using p5 Coordinates, draw the following:

rect(100,150,200,50);

Then identify as many points as you can in the next two minutes that fall inside the rectangle.

### Introduction to Collide2D (20 - 30 Minutes)

As you review the brainstarter, ask students to come up with rules for points (x coordinatres and y coordinates) that would tell you they are definitely a point in this rectangle. You may need to draw the rectangle large on the board to help students understand. They should come to the idea that all x points must be between 100 and 300, and all y points must be between 150 and 200. Introduce students to this idea:

![Image of rectangle showing constraints for x and y coordinates inside of shape.](<../.gitbook/assets/Screen Shot 2021-10-27 at 2.41.02 PM.png>)

Then, show them what this would look like in code. This could be either a code along or a watch me code moment, depending on how quick your students are; it’s meant to be a demonstration that leads into the next idea of using the collide2d library. In whatever format you prefer, demonstrate this to students:

```
//create a variable to control color of the rect, add fill, ensure you have rect from the brainstarter on canvas

if(mouseX > 100 && mouseX < 300 && mouseY > 150 && mouseY < 200){
   rectColor = color(255,0,255)
}
else{
  rectColor = color(0,255,255)
}
```

Explain to students that we could use this logic to make something happen if the mouse is over a rectangle every time, but it’s a lot to type out. Not to mention it doesn’t account for other shapes - if we wanted to determine if we were over an ellipse (or a triangle, heaven forbid!) we would need to figure out different types of logic. All of this is possible, but perhaps more work than we want to do.

Because of this, we will be using another p5.js library. Remind students that p5.js is a JavaScript library that allows you to do specific things on the canvas that aren’t otherwise available. Similarly, the library we will be using - collide2D - is a JavaScript library built in p5. It’s full of functions that someone else has programmed and do the thinking on so we don’t have to, but essentially they look like the above conditional behind the scenes. They have just been made into reusable functions for us so that we can do a little less typing! Ask students to make a copy of this starter code ([p5 editor](https://editor.p5js.org/cs4all/sketches/2h4aTWZsB) | [repl.it](https://replit.com/@qrtnycs4all/U2LA21-Collide-2D-LessonPractice-Starter-Code#script.js)). Start by showing students the [collide2D library](https://github.com/bmoren/p5.collide2D) - explain the parts they can safely ignore and the bits they want to read. Students will want to know how to navigate the table of contents. Once they get there, tell them that you are going to try to decide if the mouse is on top of a rectangle - which code would they want? Students should land on collidePointRect (the mouse is considered a point). Click on it and explain to students how to read the documentation. They should have an example of how it’s used as well as what goes into the function itself. It’s recommended to copy/paste this function into their code as a comment so they can use it as reference. Code the reaction to the rectangle so students have something like this:

```
//collidePointRect(pointX, pointY, x, y, width, height)

if(collidePointRect(mouseX, mouseY, 20, 50, 110, 110){
  rect1Color = color(100,200,50)
}
else{
  rect1Color = color(50,100,200)
}
```

Once students have completed the code along, give them a chance to finish the rest of the practice activities. The practice is redundant on purpose, and if students get bored, ask them to try to change other things on the hover reaction instead of just color.

This lesson also offers a good moment to reinforce the objects that they have been working with in the prior lessons. While each individual shape only has one property that is changing, because all of these properties are the same (they’re colors!) this could be a way to group the object. Note that because you are using color declarations, you’d need to declare the variable globally and assign color values in setup before changing them in draw. The declaration and initialization would look something like this:

```
var colors;

function setup(){
createCanvas(510, 350);

 colors = {
  rect1 = color(255,0,255),
  rect2 = color(255,255,0),
  rect3 = color(0,255,255)
  //you would continue this for each shape
 }
}
```

And when using/updating the values, it would look something like this:

```
//rect 1
  fill(255)
  rect(20,50,110,110)

if(collidePointRect(mouseX, mouseY, 20, 50, 110, 110){
  colors.rect1 = color(100,200,50)
}
else{
  colors.rect1 = color(255,0,255)
}
```

The big takeaway here is that values grouped in an object should have some commonality between them - either that they are all attributes of the same element, or they are all the same attribute of many elements.

### Collide With Shapes (15 - 20 minutes)

Most likely, this section will be the start of the second day of this lesson cycle. As a launch into it, consider asking students to explore other options in the Collide2D library, or find a common error based on the prior day’s work that you display on the board.

Once this section begins, ask students to duplicate this starter code ([p5 editor](https://editor.p5js.org/cmorgantywls/sketches/aUZv6Jll7)| [repl.it](https://replit.com/@qrtnycs4all/Collide-with-Other-Shapes-Practice-Starter-Code#script.js)) into their p5.js account. Then, code along with them the steps to make the strokeWeight of the line increase when the mouse is over the line. _(Note: One oddity about the collidePointLine function is that it has an optional final value. Students have seen optional values before, but this one controls something called ‘buffer’ - explain to students that this is how forgiving/precise you have to be about being on top of the line itself, because lines can be small. Allow for them to play with values between 0 and 1 and test out the varying results!)_

```
//collidePointLine(pointX, pointY, x, y, x2, y2, [buffer])
if(collidePointLine(mouseX, mouseY, 25, 20, 155, 70){
  lineWeight = 10
}
else{
  lineWeight = 2
}
```

After this, send students to find the correct collide2D codes to complete the remaining challenges. This can serve as an excellent pair programming activity or can be completed alone, depending on your preference for your classroom and student moods.

### Extra Practice: Puzzle Edition (20 - 30 Minutes)

One common misconception that students gain through generalization in these lessons is that when you hover of a shape, that specific shape must be the one to change. In reality, as a programmer you are the one giving instructions to the computer about what should be done - and that means that each shape could be a secret switch to trigger something else to happen. (We will come back to this in the mini project.)

[Share students on this starter code](https://editor.p5js.org/cs4all/sketches/HkpyLtUVQ). Give them 15-20 minutes to complete the following exercise.

Give/display the following instructions (they can be adjusted for level as needed). Use conditionals and variables to make the following things happen:

* When you hover over the top left ellipse, it should turn light blue.&#x20;
* When you hover over the top middle ellipse, the bottom left and bottom right ellipse should turn purple.&#x20;
* When you hover over the top right ellipse, it and the bottom middle ellipse should turn black.&#x20;
* When you hover over the bottom left ellipse, it should turn the entire top row of ellipses red.&#x20;
* When you hover over the bottom center ellipse, it should turn the top left ellipse green.&#x20;
* When you hover over the bottom left ellipse, it should turn the bottom right ellipse orange.

### Wrap Up

Students can submit code via a Google Form if you would like to collect it. If not, have students come back together for a discussion on what struggles they encountered in this activity.

### Extensions

Ask students to find a way to keep track of how many times a shape has been hovered on. If it has hovered a certain number of times, make the reaction on hover change.

