---
description: How can I use built-in variables to create a program that lets the user draw?
---

# U2LA1.4: Draw with Mouse

### Overview/Teacher Feedback

This learning activity introduces p5`s program flow, demonstrating how setup() and draw() function. By using p5`s mouse position variables and turning off the background function, they create expressive drawing programs

* This lesson is primarily a code-along, as it introduces several new concepts. Students will be rewarded for sitting through a very teacher-oriented lesson with ample play time and the chance to share and review each other’s work.&#x20;
* When you introduce frames, some students may struggle with the concept. If students are struggling, you might want to demonstrate with a paper stack - start drawing then replace with another paper and continue drawing, to show how a background erases what was previously there.&#x20;
* The wrap up and share out can take many forms. It’s recommended you give students time to move, as they are sitting still and working independently for most of the class, and may be eager to move and share.

### Objectives

Students should be able to:

* Understand how moving background out of the draw function allows the user to draw
* Utilize pmouseX and pmouseY to create something that draws.

### Suggested Duration

1 period (\~45 minutes)

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe how I might use patterns to express an idea.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.&#x20;
* Explain how a function I prototyped can be used by someone else.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.

### Vocabulary

* **Control flow**: The order in which steps of an algorithm are executed; determined by logical constructs such as IF statements, loops, and calls to other procedures.
* **pmouseX**: The system variable pmouseX always contains the horizontal position of the mouse or finger in the frame previous to the current frame, relative to (0, 0) of the canvas.&#x20;
* **pmouseY**: The system variable pmouseY always contains the vertical position of the mouse or finger in the frame previous to the current frame, relative to (0, 0) of the canvas.&#x20;
* **frameCount**: The system variable frameCount contains the number of frames that have been displayed since the program started.

### Planning Notes

|                                                                                                           Planning Notes                                                                                                           |                                                                         Materials Needed                                                                         |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| This lesson is scheduled to take one period, but students may finish more quickly; if they do, it is meant to bleed naturally into lesson 2 on the map function, so feel free to start the second in the same period if necessary. | Only a computer is required, but you may want pads of paper or other wireframing supplies to help students express their ideas if they are struggling with code. |



### Resources

* [Lesson Starter Code ](https://editor.p5js.org/cs4all/sketches/y5WZ8h6G0)
* Video tutorial: [2.1 Variables in p5.js (mouseX, mouseY) ](https://www.youtube.com/watch?v=RnS0YNuLfQQ)| [Code](https://github.com/CodingRainbow/Rainbow-Code/tree/master/p5.js/2.1\_Variables\_in\_p5.js\_mouseX\_mouseY)&#x20;
* [Draw with Mouse](https://youtu.be/NQ9-ENFtr6s) (Youtube Video)&#x20;
* Learning Processing book: [Chapter 3](http://learningprocessing.com/examples/chp03/example-03-02-mouseX-mouseY), sections 3.1, 3.2 and 3.4 | [Code](https://github.com/shiffman/LearningProcessing-p5.js/blob/master/chp03\_flow/)&#x20;
* Getting Started With p5.js: Chapter 5, examples 5.04 to 5.09 | [Code](https://github.com/lmccart/gswp5.js-code/tree/master/05\_Response)

### Assessment

Assess the student practice activity. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Create a drawing tool using the p5 draw function

### **Do Now/Warm-Up (3-5 minutes)**

Ask students to recall the difference between the setup() and draw() functions and discuss with their partner.

### **Draw with Mouse (20 minutes)**

Start students with [this code](https://editor.p5js.org/cs4all/sketches/y5WZ8h6G0) which they should duplicate and put into their own accounts/ Structure this section as a code along. After you have had a chance to review the brain starter, introduce the frameCount variable using the starter code sketch. Students may need an introduction to frames - be prepared to explain the way they work (counting each new frame that is drawn, roughly 60 frames per second) as you run the code and watch the numbers tick up.

Tell students you are now going to remove the background. Ask for predictions before you make the change - what do they think will happen? Once removed, either by deleting or by moving into setup, ask if their predictions came true and why they think this is taking place. Then, ask what will happen if you put background back into the setup - what will happen now? The code should look like this, and the numbers that were continuously ticking up should still be - except now they will create a blur.

```
function setup(){
	createCanvas(600, 240);
}

function draw() {
  background(180); 
  // Displays the frame count
  
  text("I'm drawing", 20, 20);
  text(frameCount, 100, 20);


  ellipse(300, 80, 10, 10);
}
```

Once students have established this idea, move forward with “Draw with the mouse” section, demonstrating how mouseX and mouseY can be used to move and draw with shapes. Replace the x and y values in the ellipse with mouseX and mouseY and see what happens when there is no background. Be sure to draw student attention to what happens when you move your mouse quickly, etc as a way to introduce drawing with a line. Analyze sketch as a group and have students explain the application of mouseX and mouseY.

Although it might seem that our ellipse is only drawn once, it is actually being drawn over and over again for as long as our sketch runs. The reason we don't see any changes is that the ellipse is being drawn, again and again, in the same exact position. For us to see any changes, something needs to vary.

Explain: We have already used mouseX and mouseY in the previous learning activity, to help us place our shapes. Like width and height, mouseX and mouseY are built-in variables. p5 continuously checks where the mouse is and updates mouseX and mouseY with the latest position.

Now, instead of writing their current values on the screen like we did before, let's use these variables to set the position of an ellipse ––to make it vary**.**

```
function setup(){
	createCanvas(600, 240);
}

function draw() {
  background(180); 
  ellipse(mouseX, mouseY, 10, 10);
}
```

Students may not want to draw with something that leaves gaps, which means that we need to figure out how to draw with lines. This can be problematic because lines require four values, which means we will need to demonstrate how to use pmouseX and pmouseY to create a continuous line. (Protip - have students comment out the ellipse and replace it with the line instead of deleting the code entirely, so they have a reference for later!)

```
function setup(){
	createCanvas(600, 240);
	background(0);
}

function draw() {
	
	line(mouseX, mouseY, pmouseX, pmouseY);
}
```

Once you’ve covered the basics, remind students that we have done just that - the basics. Our ellipse and/or line look very boring. Remind them that we can add stroke/strokeWeight/fill (although lines do not have a fill) and we can even make mouseX/mouseY control those values, too! We can also mix in other parts of p5, such as the dist() function, which will calculate the distance between two points and return a number. This can help us make things happen in our program like getting different appearances when you move your mouse quickly or slowly. Create the following example, finding the distance between mouseX/mouseY and pmouseX/pmouseY

_Note: Students can conceptually struggle with how speed connects to distance. Be prepared to explain!_

```
function setup(){
	createCanvas(600, 240);

	background(0);
}

function draw() {
	var weight = dist(mouseX, mouseY, pmouseX, pmouseY);
	strokeWeight(weight);
	line(mouseX, mouseY, pmouseX, pmouseY);
}
```

### **Student Practice (10 - 15 minutes)**

After introductions, provide students 10 - 15 minutes to complete the following challenge

Create a basic drawing program that draws as the mouse moves.

Make your program unique - you can draw with a line, a shape, a design. You can adjust the fill and transparency, and even try to calculate values to change how your program looks. Ask that students make the most UNIQUE program possible, as we will be looking at each other’s code!

You can draw with a line, a shape, a design. You can adjust the fill and transparency, and even try to calculate values to change how your program looks.

Encourage students to be creative. This is a great opportunity to experiment with code. They can use mouseX and/or mouseY for different values and test the output. They can play with the dist() function and experiment with color and shapes.

Encourage them to do the following:

* Draw with different shapes.&#x20;
* Change the fill or stroke based on your mouse position&#x20;
* Change the size based on your mouse position.&#x20;
* Use the dist() function to vary your tool based on how fast your mouse is moving

### **Wrap-Up**

Wrap-Up will be a bit longer to give students a chance to see each other’s work. A recommended strategy is this:

Ask students to pull up their program and hit play, so it’s running. Put on a song and allow students to circulate around the room - when the song stops, students must sit at the closest computer to them and explore the program and code. (Think: musical chairs, but always the right number of chairs.) Repeat this several times.

When you have finished, come together for student shout outs. Show student code and go over interesting examples.

### **Extensions**

Students can push the drawing program as far as they would like - either with their own imagination or trying one of the following:

* **T**ry to code a rainbow by separating multiple colored lines and drawing with each one.
* Make the drawing tool different depending on where on the canvas you're drawing. Split the canvas into four; the drawing app should be different in each quadrant.

