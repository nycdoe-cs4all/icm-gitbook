---
description: How can I move the p5 origin to effect the position of shapes?
---

# U4LA2.1: Translation Battleship

### Overview && Teacher Feedback

This lesson introduces linear transformations: translation, push(), and pop().

Translate is a useful little skill mostly when used in conjunction with other things - on its own, it seems pretty boring and pointless. That’s okay - just acknowledge it with kids, and explain that its use is coming, but for now, they just need to learn what it does. Then they’ll get to how it can be useful.

This should be pretty direct for students as transformations are an 8th-grade math standard. This can be used to open up the idea that even in math, you aren’t really moving the shape - you’re moving the origin. This is the big takeaway from this lesson that students need to know moving forward!

### Objectives

Students will be able to:

* Use push and pop to apply transformations to the canvas&#x20;
* Transform an entire drawing.&#x20;
* Transform some of its elements.

### Suggested Duration

45 minutes (\~1 period)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

\[COMING SOON]

### Vocabulary

* **Transformation** - In computer graphics a common task is to transform the coordinates (position, orientation, size) of objects in the display window.&#x20;
* **Translation -** In computer graphics, translation refers to the movement of objects from one position to the other in a two-dimensional or three-dimensional plane.
* &#x20;**translate()** - Specifies an amount to displace objects within the display window&#x20;
* **push()** - Saves the current drawing style settings and transformations&#x20;
* **pop()** - Restores drawing style settings and transformations

### Planning Notes

|                                                                       Planning Notes                                                                       |                                                    Materials Needed                                                   |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------: |
| This lesson mostly consists of an exploratory game activity. Please take care to preview the lesson and make sure you are familiar without the tool works! | No extra materials needed, unless you need to turn the plugged activity into something paper-based for your studnets. |

### Resources

_Elements of this lesson were adapted from_ [_http://genekogan.com/code/p5js-transformations/_](http://genekogan.com/code/p5js-transformations/)__

* **Translate Exploration Example Starter Code** ([p5 editor](https://editor.p5js.org/cs4all/sketches/Hy7EE-c6m) | [repl.it](https://replit.com/@qrtnycs4all/U4LA21-Translation-Exploration-Starter-Code#script.js))
* **p5 editor:** Translation Battleship (Plugged Starter Code): [Level 1](https://editor.p5js.org/cmorgantywls/sketches/ivol7UfjI) | [Level 2](https://editor.p5js.org/cmorgantywls/sketches/U1zQeJC5P) | [Level 3](https://editor.p5js.org/cmorgantywls/sketches/Ej\_0eGbUN)
* **repl.it:** Translation Battleship (Plugged Starter Code): [Level 1](https://replit.com/@qrtnycs4all/Lv1-Transformation-Battleship#sketch.js) | [Level 2](https://replit.com/@qrtnycs4all/Lv2-Transformation-Battleship#sketch.js) | [Level 3](https://replit.com/@qrtnycs4all/Lv3-Transformation-Battleship#sketch.js)
* [Transformations Pt. 1](https://youtu.be/o9sgjuh-CBM) (Youtube Video)

### Assessments

_No major assessments in this lesson - take checks for understanding as you see fit!_

### Do Now/Warm Up

What would happen if you translated a point at (10,20) by 50 units on the x axis and 30 units on the y? Where would it end up? What if you had a point at (0,0) and translated it by 20 units on the x axis and 5 units on the y?

### About translate()

**NB:** _Remind students again that translate() is a useful little skill mostly when used in conjunction with other things - on its own, it seems pretty boring and pointless right now. That's okay! Acknowledge that, remind them this will all be important later, and continue on._

An alternative to positioning elements by setting their coordinates directly is to change the position of the entire coordinate system: to move, rotate, and scale the x and y-axis.&#x20;

In Math, if we have a single point - let’s say (0,0) - and translate it by (10,20), where would its new place be? P5 works in a similar way. We can think of it less about translating the shape and more about moving the origin, which in turn moves all shapes on the screen.&#x20;

Using the translate() function we can achieve this. This function can shift the coordinate system left, right, up, and down. Moving the coordinate system is called translation.

![image of translate(x, y, \[z\]) with x and y annotated for their purpose](https://lh4.googleusercontent.com/T\_KVtgO2rkLh-gtERU5DX-wjnP852WIctRftdmIQja5rQIqRa3-yZremoYcXsPIky8YHiOUGFWP64fXSnrEcdK7c16Fn8LhgwNHmMW-KzfYXasOqEHzudXGXV9NtFjhU3rdenuX5)

**NB:** _The z-axis is only relevant if we are working in 3 dimensions (or layering in interesting ways), which is why it's optional!_

In these two examples, we are translating the coordinate system origin to (40, 20) or (60, 70) and then drawing a rectangle 20 pixels left and down of the origin.

![Two graphs demonstrating translations that move the origin and so also the shape.](https://lh4.googleusercontent.com/\_AiOBDZH9wN2nNaCjzD8Ghr-ejAeSiC8BIgnrmGIRFS3-d82ZZn7590B8qNf\_Vf3dQo1SWQAucSKWXE9jCupPrSSwVK-6tlRwPniHgCJfSNV2u2xBN5HV7bNGiLtEtxDMnIu0XVQ)

As far as the rectangle is concerned, it hasn't moved at all. Its upper left corner is still at (20, 20). When you use transformations, the things you draw never change position; the coordinate system itself does.

It’s important to say all of this to the students so they understand what’s happening - but also this isn’t fully going to click until they start doing it themselves. As was mentioned before, kids have a very hard time grasping why this is useful/more useful than just changing coordinates, and they aren’t really going to see full benefits until future lessons. Embrace and acknowledge that!

Because it moves the whole coordinate system, any elements drawn after the call to translate will also be affected by it. Copy and paste the following [example](https://editor.p5js.org/cs4all/sketches/Hy7EE-c6m) in the editor and make changes to the code:

```
function setup() {
  createCanvas(400, 400);
  background(204);
}

function draw() {
  translate(mouseX, mouseY);
  ellipse(0, 0, 40, 40);
  ellipse(5, 5, 10, 10);
  ellipse(-5, -5, 5, 5);
  ellipse(55, 10, 10, 10);
  ellipse(-55, -5, 5, 5);
}
```

Even though the ellipses have a static location, they all follow the mouse because the origin has been translated to wherever the mouse position is. This is useful if trying to translate a design in its entirety without doing extra math. (You can also have students adjust the values in translate() to test what this looks like when the shapes aren't moving.)

### Exercise #1: Draw an Ellipse at a Translated Location

Modify the previous examples and do the following. Draw a white ellipse at the following translated location:

* 40 pixels to the left of the mouse cursor&#x20;
* 40 pixels to the right of the mouse cursor&#x20;
* 40 pixels over the mouse cursor&#x20;
* 40 pixels under the mouse cursor

Add two other elements that are not affected by translate().

### Translation Battleship

**P5 Editor Links:**

1. ****[**Level 1** ](https://editor.p5js.org/cmorgantywls/sketches/ivol7UfjI)**(one translation for everything) -** _Pause_ after this _to talk about adding multiple translations in a sketch, with the results being cumulative. Then, you're on to Level 2!_
2. ****[**Level 2**](https://editor.p5js.org/cmorgantywls/sketches/U1zQeJC5P) **(separate translations for each shape - cumulative)** - _Pause here to talk about push() and pop(), outlined below. These are also WILDLY USEFUL THINGS that students will not understand the use of until a bit farther into this learning activity! Once they understand the idea of push() and pop(), then move on to:_
3. ****[**Level 3**](https://editor.p5js.org/cmorgantywls/sketches/Ej\_0eGbUN) **(with push() and pop())**

**Repl.it Links:**

* ****[**Level 1**](https://replit.com/@qrtnycs4all/Lv1-Transformation-Battleship#sketch.js) **(one translation for everything) -** _Pause_ after this _to talk about adding multiple translations in a sketch, with the results being cumulative. Then, you're on to Level 2!_
* ****[**Level 2**](https://replit.com/@qrtnycs4all/Lv2-Transformation-Battleship#sketch.js) **(separate translations for each shape - cumulative)** - _Pause here to talk about push() and pop(), outlined below. These are also WILDLY USEFUL THINGS that students will not understand the use of until a bit farther into this learning activity! Once they understand the idea of push() and pop(), then move on to:_
* ****[**Level 3**](https://replit.com/@qrtnycs4all/Lv3-Transformation-Battleship#sketch.js) **(with push() and pop())**

#### push() and pop()

Sometimes, a sketch will involve multiple translations to draw the same thing in different locations. If we want to draw the same shape in multiple locations we can use push() and pop() to keep track of and revert our translations as we go.

* push() before a translation pushes through that translation for just the shapes listed below it.&#x20;
* pop() after a translation and shapes pops off the translation so that it does not affect anything below it.

![Screenshot of a sketch using push() pop() with translate](<../.gitbook/assets/Screen Shot 2022-03-10 at 11.13.02 AM.png>)

Both ellipses have all the same parameters, but appear in different places! push() and pop() also track and revert style and color changes -- fill(), stroke(), etc.&#x20;

Thus all translations and style/color commands made between a single push() and pop() apply only to the operations made between them. Take a look at the following example.

```
//Source: genekogan.com/code/p5js-transformations/

function setup() {
	createCanvas(400, 400);
}

function draw() {
	background(255);
	
	push();
  	translate(50, 50);
	fill(255, 0, 0);
  	rect(0, 0, 100, 100);
	pop();

	push();
  	translate(250, 150);
	fill(0, 255, 0);
  	rect(0, 0, 100, 100);
	pop();

	push();
  	translate(140, 280);
	fill(0, 0, 255);
  	rect(0, 0, 100, 100);
	pop();
}
```

In this sketch, we could have achieved the same visual output by simply drawing the rectangles at those exact points. Or we could have used translate() without push() and pop() by undoing each translation manually.

For simple shapes like rectangles, it is easier to not use translations, but rather to specify the points manually. But when we begin to draw more complex shapes, or when we use other transformations, translations become advantageous.

### Wrap Up

Most of this lesson involves students playing Translation Battleship, and there are no major assessments or collectibles to turn in. At the end of class, consider debriefing how the games went with a focus on the code itself. (There is a very real world in which no one 'won' any rounds.)

* How can translate, push/pop be useful in your programs?
* What was a challenge?
* What do you still have questions about?
