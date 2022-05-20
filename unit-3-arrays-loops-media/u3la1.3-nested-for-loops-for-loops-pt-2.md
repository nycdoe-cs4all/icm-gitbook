---
description: How can we use iteration to abstract artwork?
---

# U3LA1.3: Nested For Loops (For Loops pt 2)

### Overview && Teacher Feedback

In this learning activity, students will create a grid using nested for loops. This is a direct lead in to the mini project, which can serve as an extension to this lesson. (Or this lesson can serve as a launch for the mini project, depending on how you’d like to view it.)

Nested loops may be the most difficult loop concept to understand because of the syntax and the sequential logic behind creating the column or rows. So take your time with the lesson and ensure students are comfortable with creating for loops and suing for loops before starting this lesson.

Encourage students to use comments to help with organization, it will decrease the number of errors and questions. If some students are not fully able to understand the concept it is not essential for future lessons but it will be very useful to know especially for the wallpaper project. Creating a template of the nested for loop can also be very useful for confused students.

This pair programming experience is very open-ended - try to encourage students to talk together about features for their program, rather than each person deciding for the group when it is their turn to navigate.

Push students to think about the user experience in leaving their feedback: did they know while loop is working correctly? How could this be improved?

### Objectives

Students should be able to:

* Create for loops&#x20;
* Nest two for loops&#x20;
* Create a grid of shapes

### Suggested Duration

45 minutes (\~1 class period)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Algorithms:**

* Explain why I used specific instructions to complete a task.&#x20;
* Compare and contrast my instructions with other instructions that complete the same task.&#x20;
* Demonstrate the benefit of using an event, conditional or loop in my prototype.

**Prototype:**

* Experiment with the commands of a programming language.&#x20;
* Explain why I chose specific commands to communicate my instructions.

### Vocabulary

* **Loops** - A sequence of instructions that is repeated until a certain condition is met.&#x20;
* **Iterations** - the repetition of a process or utterance.&#x20;
* **For loop** - loops through a block of code a number of times&#x20;
* **Nested loop** - one loop is running inside of another loop.

### Planning Notes

|                                                      Planning Notes                                                     |         Materials Needed         |
| :---------------------------------------------------------------------------------------------------------------------: | :------------------------------: |
| _There are no specific planning notes for this lesson, but it is the first lesson students will be using media - whoo!_ | **No special materials needed.** |

### Resources

* [Nested For Loops](https://youtu.be/AjZuozaFl38) (Youtube Video)
* [4.1 While and for loop](https://www.youtube.com/watch?v=cnRD9o6odjk\&t=500s) | [Code](https://github.com/CodingRainbow/Rainbow-Code/tree/master/p5.js) (4.1a to 4.2b)&#x20;
* [Learning Processing: Chapter 6. Loops ](http://learningprocessing.com/examples/)
* [Getting Started With p5.js: Chapter 4. Variables (Section: Repetition)](https://p5js.org/books/)

### Assessments

Assess the **Do Now** assignment. Check for the ability to:

* Identify a student’s knowledge of for loop syntax

Assess the **learning activity**. Check for the ability to:

* Complete exercises 1 and 2&#x20;
* Understand the structure of nested loops.&#x20;
* Apply understanding of nested loops to create grid designs.&#x20;
* Use of nested loops to define control structures.

Assess the **Wrap Up** assignment. Check for the ability to:

* Describe how nested loops work.

### Do Now/Warm Up (3 - 7 min)

_Have students try to create a grid using the for loop method from the previous lessons._

![Image showing row of ellipses and several completed columns](<../.gitbook/assets/Screen Shot 2021-12-13 at 10.42.43 AM.png>)

**Example** ([p5 editor](https://editor.p5js.org/cs4all/sketches/S1rbcElNW) |[ repl.it](https://replit.com/@qrtnycs4all/U3LA13-Grid-Without-Loops-Example-Code))- Students should realize how tedious and prone to errors this method can be.

_Ask Students:_

1. How do you think we can do this in a more efficient way?&#x20;
   1. To break down all the parts of a grid (columns and rows).
2. Review how the position increments with each iteration.

### Nested For Loops (7 - 12 min)

As you review the Do Now, explain that in a previous lesson, we drew rows and columns using for loops. Here is an example of how we accomplished that using multiple for loops (display linked example code ([p5 editor](https://editor.p5js.org/cs4all/sketches/S1rbcElNW) |[ repl.it](https://replit.com/@qrtnycs4all/U3LA13-Grid-Without-Loops-Example-Code))). The first for loop increments the x position creating a row of ellipses and the second loop increments the y position creating a column of ellipses.&#x20;

This is a lot of repetitive code, and aside from being tedious and error-prone, our brains should be firing a flashing light whenever we see that much repitition: it usually means there is an easier, or at least more efficient, computational way to solve our problem.

In this example, we can accomplish creating an entire grid of shapes with _just two loops._ The catch is that we will be putting one inside the other; our goal is that the first loop will draw a row of circles, from left to right, but for each new circle placed, the second loop will draw a column going down. It will end up looking something like this in process (although it will appear static on screen unless we really mess with the frame rate):

![Gif of the grid of ellipses being constructed by going over and then down.](<../.gitbook/assets/ry9esneaV\_lesson 5.gif>)

This can be really confusing for students, and that's okay - they will probably have to dive into the loop itself and fiddle with some numbers before it sticks. As you are making the loop, feel free to come back to this gif or any sample drawing and walk through the process of what is happening to cement their understanding.

With your students, code out the following example in the draw function that you can use to explain (and that they can mess with):

```
for(var x = 30; x < width; x += 30){ //same as x = x +30
  for(var y = 30; y < height; y += 30){ //same as y = y + 30
    ellipse(x,y,15,15)
  }
}
```

The syntax of nesting loops can be confusing for students, so it is recommended to work from the outside in. (Write the first full loop with correct brackets, then put the second loop inside of it with brackets, and then finally put in what should be happening through both loops - the ellipse using both iterative variables.)

In the example above we draw an ellipse at an x location with the variable x and a y location with the variable y. X is incremented by 30 in the outer for loop (which will draw a row) and in the inner for loop, y is incremented by 30 (which will draw a column). Each time the x loop is run, it draws an ellipse in the row, as well as an entire column at that x location as illustrated by the animation above.

The first time the outer for loop runs, x is 30. Then the inner for loop runs. y starts at 30. A circle is drawn. y is set to 60. The second circle is drawn, 30 px below the first. Then y is set to 90, and a third circle is drawn, 30px below the previous one. Now the inner for loop is done, the outer loop sets x to 60, and the cycle continues.

You may need to describe this to students several times, and it's also recommended that you show them how the rows/columns can be changed by adjusting values in the loop. Start with the x loop to show how you can adjust that spacing and make it start/stop at different places, then do the same with the y loop. You may also choose to show them what happens if you make a shape in the x loop but not the y loop so they have a better sense of the control flow at play, here.

Once you feel like students have at least a basic grip of the logic happening in the code, it's time to send them off! With their partners, they should work on the activity below. This will solidify their understanding of for loops. Look out for curly bracket errors. Students may want to create new variables but encourage them to use the x and y variables they create in the for loops.

### Student Activity: Grid Design (10 - 15 min)

Ask students to go find a design they have made in the past, such as their emoji project or taijitu symbol. (Avoid having them make a brand new design unless it is comprised of 3 or less shapes and can be done in about five minutes.)

Then, ask students to use that design in a nested for loops to turn it in a grid, like so:

![Grid of consecutive rainbow circles](<../.gitbook/assets/Screen Shot 2021-12-13 at 11.27.24 AM.png>)

Example Code:

```
function setup() {
  createCanvas(600, 120);
}

function draw() {
  background(220);
	
	//create a row of ellipse
	for(x=0;x<=width;x=x+40){
		//each time the loops is cycled through a column will be drawn at x location
		for(y=0;y<=height;y=y+40){
		fill(255,0,0);//add a red fill
		ellipse(x,y,40,40)
		fill(0,255,0);//add a green fill
		ellipse(x,y,30,30);
		fill(0,0,255);//add a blue fill
		ellipse(x,y,20,20);
		fill(255,0,255);//add a purple fill
		ellipse(x,y,10,10);
		}
	}
}	
```

The focus here is on practice as opposed to innovation and creativitity ONLY because there is a mini project directly after this lesson that will allow them to use this skill in a more ✨creative/interesting ✨way. We want them to have practiced before getting there, but not get totally lost in making this new practice assignment (yet)!

### Wrap Up (5 min)

Ask students to post their project links in a forum such as Slack or the Google Classroom. Then, have them view and comment on two other projects, leaving a glow and grow for each

**Guiding questions:**

* Explain how can you create a grid of shapes using nested for loops&#x20;
* Which errors can we get from nesting for loops?

### **Extensions**

Give students specific and logically challenging tasks for while loops such as:

* Creating a grid of emojis&#x20;
* Using HSB values to make a rainbow grid.
