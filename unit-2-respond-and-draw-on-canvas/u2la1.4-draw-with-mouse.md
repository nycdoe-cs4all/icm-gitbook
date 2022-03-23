---
description: How can I use built-in variables to create a program that lets the user draw?
---

# U2LA1.4: Draw with Mouse

### Overview/Teacher Feedback

This learning activity introduces p5`s program flow, demonstrating how setup() and draw() function. By using p5`s mouse position variables and turning off the background function, they create expressive drawing programs. The use a new data structure, object literals, is a way of keeping code more organized so that students do not get overwhelmed.

* This lesson is primarily a code-along, as it introduces several new concepts include object literals. Students will be rewarded for sitting through a very teacher-oriented lesson with ample play time and the chance to share and review each other’s work - and object literals, which we will continue using through out the course, will make life MUCH easier.
* When you introduce frames, some students may struggle with the concept. If students are struggling, you might want to demonstrate with a paper stack - start drawing then replace with another paper and continue drawing, to show how a background erases what was previously there.&#x20;
* The wrap up and share out can take many forms. It’s recommended you give students time to move, as they are sitting still and working independently for most of the class, and may be eager to move and share.

### Objectives

Students should be able to:

* Understand how moving background out of the draw function allows the user to draw
* Utilize pmouseX and pmouseY to create something that draws.
* Use object literal to simplify code that involves many variables

### Suggested Duration

1-2 periods (\~45 minutes each)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.7** Design or remix a program that utilizes a data structure to maintain changes to related pieces of data.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

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
* **Object literal**: a comma-separated list of name-value pairs inside of curly braces. (If you’ve worked in other languages, this is like a python dictionary that can also hold functions.)

### Planning Notes

|                                                                                                                       Planning Notes                                                                                                                      |                                                                         Materials Needed                                                                         |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| This may bleed over into two periods with the addition of object literals in JavaScript. That’s okay! They will also get MUCH more practice with these as they go through the course, so help them as needed and it will become more intuitive over time. | Only a computer is required, but you may want pads of paper or other wireframing supplies to help students express their ideas if they are struggling with code. |



### Resources

* [Lesson Starter Code ](https://editor.p5js.org/cs4all/sketches/y5WZ8h6G0)
* Video tutorial: [2.1 Variables in p5.js (mouseX, mouseY) ](https://www.youtube.com/watch?v=RnS0YNuLfQQ)| [Code](https://github.com/CodingRainbow/Rainbow-Code/tree/master/p5.js/2.1\_Variables\_in\_p5.js\_mouseX\_mouseY)&#x20;
* [Objects in p5.js](https://youtu.be/-e5h4IGKZRY) (Youtube Tutorial)
* [Introduction to Objects - Code.org ](https://youtu.be/ZunUF\_WGMb4)(Youtube Video)
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

Start students with [this code](https://editor.p5js.org/cs4all/sketches/y5WZ8h6G0) which they should duplicate and put into their own accounts/ Structure this section as a code along. After you have had a chance to review the brain starter, introduce the frameCount variable using the starter code sketch.

So far we have been drawing static images: they don't change over time. But one of the exciting things about drawing computationally is that we can make our drawings dynamic: we can have them change over time and respond to what the user does, or to some other kind of input.

You have probably noticed that setup() and draw() come up repeatedly in the examples. These are both functions, like rect and ellipse, except that instead of calling them, we have been declaring them in our code. p5 takes care of calling them for us. In fact, it calls setup once, when our program starts, and then it calls draw once and again, forever (or until we close the sketch window).

To prove it, look at this example. Each time our draw() function is called, p5 adds 1 to a variable called frameCount. In the sketch below, we draw this variable to our canvas, using the text function. As you can see, frameCount keeps growing, as p5 calls draw() over and over again.

Students may need an introduction to frames - be prepared to explain the way they work (counting each new frame that is drawn, roughly 60 frames per second) as you run the code and watch the numbers tick up.

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

Be sure to draw student attention to what happens when you move your mouse quickly, etc as a way to introduce drawing with a line. Analyze sketch as a group and have students explain the application of mouseX and mouseY. Students may not want to draw with something that leaves gaps, which means that we need to figure out how to draw with lines. This can be problematic because lines require four values, which means we will need to demonstrate how to use pmouseX and pmouseY to create a continuous line. (Protip - have students comment out the ellipse and replace it with the line instead of deleting the code entirely, so they have a reference for later!)

```
function setup(){
	createCanvas(600, 240);
	background(0);
}

function draw() {
	
	line(mouseX, mouseY, pmouseX, pmouseY);
}
```

### Object Literals in p5.js

Once you’ve covered the basics, remind students that we have done just that - the basics. Our ellipse and/or line look very boring. Remind them that we can add stroke/strokeWeight/fill (although lines do not have a fill) and we can even make mouseX/mouseY control those values, too! With students, create a list somewhere in the room of all the things that you could change about this line (and feel free to get specific - you can change the color or just one value in the color, opacity, etc). Create this example with students before diving into objects:

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

Before you set students free to play, review the list they made of all the things that could change about their line - that’s a long list, and that means they could be making a lot of variables. This is where our object literals come in: this is a Javascript structure that is really just a comma-separated list of key:value pairs. As students have never encountered this before, walk them through how to implement in the example and talk about how they can call values using keys, as in the example below, which you should code along with students:

```
//NOTE: You are coding a lot of properites for theLine to demonstrate 
//objects literal - but you're only going to use one in this example. 
//A good follow up is 'If I wanted to make a stroke color using this 
//information, how would I do that?' and then let students come up 
//with the answer using variable.property notation.

var theLine = {
    weight:5,
    red: 255,
    green: 0,
    blue: 255,
    opacity: 100
  }

function setup() {
  createCanvas(400, 400);
  background(220);
  
}

function draw() {
  strokeWeight(theLine.weight)
  line(mouseX, mouseY, pmouseX, pmouseY)
}
```

Follow this by asking students how they could use the key:values from the object to change the stroke, and allow students to come up with the answer you code together. It’s important for students to understand that the keys act like variables, and can be essentially anything - although like with variables, they should make sense based on the program.

Please note that if students need or want to give any keys values based on p5 functions (like color(), dist(), etc) they would need to do so in setup. This can take one of two forms. Either they can declare the variable globally and initialize it in setup, as they do for most of the course, or they can follow the same steps outlined above and then reassign the values in setup or draw.

When reassigning values to keys, it looks very similar to assigning/changing values in a variable, like so:

```
theLine.weight = 10 //this would assign the value of 10 to the 'weight' key of theLine object.Student Practice (10 - 15 minutes)
```

(If any students use conditionals in the next section, this would also be how to adjust values!)

### Student Practice && Play

After introductions, provide students 10 - 15 minutes to complete the following challenge

Create a basic drawing program that draws as the mouse moves.

Make your program unique - you can draw with a line, a shape, a design. You can adjust the fill and transparency, and even try to calculate values to change how your program looks. **You MUST use an object literal to hold all of the changing values of your drawing tool!** Ask that students make the most UNIQUE program possible, as we will be looking at each other’s code!

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

