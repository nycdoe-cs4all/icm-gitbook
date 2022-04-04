---
description: How can we use iteration to make abstract artwork?
---

# U3LA1.1: While Loops

### Overview && Teacher Feedback

This lesson introduces repetition using while loops. Students will create a sketch with a repeated element to fill a specific space.

While loops is a great introduction to loops because of the syntax for declaring, conditional checking and incrementation are not as complicated as it is for a for loop.

Common misconceptions are forgetting to increment the variable, writing a valid condition and forgetting to use curly brackets. It is always important to have students write comments to debug their code.

This pair-programming experience is very open-ended - try to encourage students to talk together about features for their program, rather than each person deciding for the group when it is their turn to navigate.

Push students to think about the user experience in leaving their feedback: did they know while loop is working correctly? How could this be improved?

### Objectives

Students should be able to:

* Explain how the components of the while loops are essential to efficiency&#x20;
* Create while loops&#x20;
* Use while loops to generate multiple shapes

### Suggested Duration

45 Minutes (\~1 period)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Abstraction**

* Give examples of specific patterns in something I can see, do or touch.&#x20;
* Describe different things I tried in order to achieve a goal.&#x20;
* Explain how I might help others identify patterns.

**Algorithms**

* Explain why I used specific instructions to complete a task.&#x20;
* Compare and contrast my instructions with other instructions that complete the same task.&#x20;
* Demonstrate the benefit of using an event, conditional or loop in my prototype.

**Prototype**

* Experiment with the commands of a programming language.&#x20;
* Explain why I chose specific commands to communicate my instructions.

### Vocabulary

* **Loops** - A sequence of instructions that is repeated until a certain condition is met.&#x20;
* **Iterations** - the repetition of a process or utterance.&#x20;
* **While loop** - The while loop loops through a block of code as long as a specified condition is true.
* **Control structure -** codebase portion that supports decisions based on analysis of variables

### Planning Notes

|                                                     Planning Notes                                                    |       Materials Needed       |
| :-------------------------------------------------------------------------------------------------------------------: | :--------------------------: |
| There are no specific planning notes for this lesson, but it is the first lesson students will be using media - whoo! | No special materials needed. |

### Resources

* [4.1 While and for loop](https://www.youtube.com/watch?v=cnRD9o6odjk\&t=500s) (Youtube Video) | [Code](https://github.com/CodingRainbow/Rainbow-Code/tree/master/p5.js) (4.1a to 4.2b)&#x20;
* [Learning Processing: Chapter 6. Loops](http://learningprocessing.com/examples/)&#x20;
* [Getting Started With p5.js: Chapter 4. Variables (Section: Repetition)](https://p5js.org/books/)
* [While Loop w/ Code Comments ](https://editor.p5js.org/cs4all/sketches/HJUxl-eN-)(Code Sample)
* [Spicy Challenge Example](https://editor.p5js.org/cs4all/sketches/r1UO4XZSb) (Code Sample)

### Assessments

Assess the Do Now assignment. Check for the ability to:

* Identify the changeable values of an ellipse.&#x20;
* Identify a design pattern in the placement of the ellipses.

Assess the learning activity. Check for the ability to:

* Complete exercises #1 & 2.&#x20;
* Show understanding of the while loop syntax and structure.&#x20;
* Apply while loops to create a design with multiple simple and/or complex shapes placed around the canvas.

Assess the Wrap Up assignment. Check for the ability to:

* Explain the use of while loops.&#x20;
* Create while loops to repeat multiple shapes.&#x20;
* Identify the challenges of working with while loops.

### Do Now/Warm Up (\~5-7 minutes)

_Have students create 5 equidistant ellipses._

Open a new sketch, name it U3LA1 While loops and recreate the image below

![A row of five equally spaced, congruent ellipses](<../.gitbook/assets/Screen Shot 2021-12-01 at 3.03.52 PM.png>)

Ask students to do the following:

1. Add 5 more ellipses to the current row, they will most likely get frustrated because they will have to keep the ellipses equidistant.&#x20;
2. Answer the prompt: how we can call the ellipse function more efficiently? Push their thinking to think about why loops are necessary.

### Repeat Shapes with a While Loop

From this Do Now, ask students how could they code their loops effectively? Students might talk about copy/pasting lines of code, adjusting only selected numbers, etc. Most, if not all students, probably came to a solution like so:

```
function draw() {
	background(180);
	ellipse(100, 60, 40, 40);
	ellipse(200, 60, 40, 40);
	ellipse(300, 60, 40, 40);
	ellipse(400, 60, 40, 40);
	ellipse(500, 60, 40, 40);
}
```

But this is a lot of repitition, and something that students should start getting used to is if something looks like it repeats frequently, there is probably an easier, or at least more efficient, way to handle it in our code.&#x20;

Talk students through the actual process that you are following, which is something to the effect of:

![Handwriting that describes the loop of drawing ellipses and moving right.](<../.gitbook/assets/Screen Shot 2021-12-02 at 10.01.14 AM.png>)

Essentially, we are are drawing a new circle every 100 pixels,  and we may be tempted to write a conditional statement that says something to that effect. However, students will find this conditional doesn't work as intended, and that is because conditionals are not meant to act as loops. Conditionals run once, and once the condition is met, they stop running. (Albeit in the draw function, which is called repeatedly, it can appear as if the loop is repeating.)

Luckily, there is a control structure that can help us do this! Introducing the while loop: a loop that only runs WHILE a certain condition is true, and stops running once it ceases to be true. It looks something like this:

```
var x = 100
while(x < width){
  ellipse(x, 60, 40,40)
  x = x + 100
}
```

There are three steps needed to make sure our loop works correctly:

1. We **declare and initialize a variable**. Initializing a variable is setting the initial value for that variable, or where you want it to start. In this case, we would like to it begin at 100 pixels.&#x20;
2. We **check whether it meets a condition**. The condition is inside the parentheses. We want to execute the code in the brackets on condition that x is still less than the width of the canvas.&#x20;
3. We **change the value of that variable in a way that will eventually make it meet the condition**. In the code below, 100 is added to x inside the brackets. Every time the code is run x will increase by 100 until its value is larger than the width of the canvas. Then the loop will be completed and the program will move on in the code.

This ensures we don't create an infinite loop, which will certainly crash our browsers. Be prepared for browser crashes - make sure students DO NOT have the AutoSave feature selected as it might refresh before their loops are done. When students inevitably crash everything, cheer for them! They know enough code to break something!

Code this for loop with students so that they have an example saved in their account. (They can comment out previous ellipses from the Do Now.)

The big benefit of loops is that not only does it make our code cleaner and more efficient, but our code is now easy to change, customize, and update. If we want the row of ellipses to start somewhere else, we can adjust the starting variable. If we want to increase or decrease the spacing between the ellipses, we can adjust what we add to x. And we can change the circles themselves without having to make edits to multiple places in our code! Give students 2-3 minutes to just play with numbers and add shapes/features to their loop - it's important they understand the loop can do more than just draw one repeated shape.

### Student Practice & Play

After students have had a chance to experiment with the code from the lesson section, send students to work either individually or in pairs/small groups, based on your classroom. (We STRONGLY encourage collaborative pair or group work to help students grow their soft skills as they learn to code!)

Instruct students to use the while loop to do the following (and be on the lookout for curly bracket errors, and multiple while loop errors):

* Start a row at the left end of the canvas&#x20;
* Draw a row of ellipses 50 pixels apart&#x20;
* Draw ellipses only on the left half of the canvas

For students who need an extra spicy challenge, ask them to try to recreate one of the following in their while loop. Make sure they understand they only need ONE while loop that will contain multiple shapes!

![Row of concentric, differently colored circles looking like targets.](<../.gitbook/assets/Screen Shot 2021-12-02 at 10.44.12 AM.png>)

![Row of red 😐 faces.](<../.gitbook/assets/Screen Shot 2021-12-02 at 10.44.29 AM.png>)

**Alternately, or in addition, students may take a design they have created previously and try to get it to repeat in a while loop, or build a new custom design that will be repeated.**

### Wrap Up

Ask students to post their project links in a forum such as Slack or Google Classroom. Then, have them view and comment on two other projects, leaving a glow and grow for each

Guiding questions:

* How do while loops make the code more efficient?&#x20;
* Explain the parts of a while loop. Why are they important?
* What was challenging about using a while loop?

### Extensions

Give students specific and logically challenging tasks for while loops such as:

* Repeating their emoji from unit 1&#x20;
* Creating a grid of ellipses
