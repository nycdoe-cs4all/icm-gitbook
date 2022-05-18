---
description: How can I use mouse clicks in p5.js?
---

# U2LA2.2: Mouse Clicks && Shapes As Buttons

### Overview && Teacher Feedback

This lesson continues to use collide2D to determine if the mouse is hitting a shape, and now introduces click functionality in two different ways. Make sure students have completed the prior lesson before beginning so they are up to speed on what is happening and have all necessary resources.

This lesson adds on to what they were doing in U2LA2.1 - so much that students will be duplicating code from that lesson to continue! Adding clicks once collide2D is being used is not a huge lift, but it feels mind blowing to the students.

Students may be confused as to why a variable is changing in conditionals instead of a fill or other action - the reason for this is efficiency in drawing order, and to make sure each button changes independently of the others. If students are struggling, try this quick unplugged example:

* Have two students stand at the front of the room as you walk through the code. When the variable is declared, hand one student a paper cup or plate with the variable name on it.&#x20;
* Make sure students understand that it is an empty holder until initialized. When the variable is initialized, put a marker (or another colored writing utensil) in/on the cup/plate.&#x20;
* Give another color to the second student. When the fill is called using the variable, have the first student take the marker from the cup/plate and mime coloring.&#x20;
* When the if statement is activated, have the second student swap the marker from the first student’s hand.
* &#x20;Swap back when the if statement is not activated.

Code reading is much more challenging than code writing. Encourage students to read and discuss code as often as possible!

### Objectives

Students should be able to:

* Use conditionals to define a reactive shape button&#x20;
* Use mouseIsPressed or function mousePressed() to create mouse click reactions

### Suggested Duration

1 Period, \~45 minutes

_Use your best judgment in timing! This lesson can easily be completed in one period, however, if you believe students need more practice, give them ideas of how they could keep honing these skills and allow them time to work!_

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe different things I tried in order to achieve a goal.&#x20;
* Explain why I chose to include the specific components of my prototype over others.
* Explain characteristics or patterns that informed a function or an interface I created.
* Explain why using patterns is necessary when creating with a computer.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.
* Demonstrate the benefit of using an event, conditional or loop in my prototype.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.

### **Vocabulary**

* **mouseIsPressed** - this is a built-in variable that is True when the mouse button is pressed, and False when it is not pressed&#x20;
* **mousePressed()** - a major callback function in the p5 library that executes once, each time the mouse is pressed.&#x20;
* **Efficiency** - In this case, making it easier and faster to debug and edit your code&#x20;
* **Nesting Conditionals** - When one conditional lives within another -- so both of the conditions have to be met before your code will execute.

### Planning Notes

|               Planning Notes               |                                                                Needed Materials                                                                |
| :----------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------: |
| No specific planning notes for this lesson | If you need to act out changing values of variables in conditionals, having paper plates or cups on hand can help with variable understanding. |

### Resources

* [Collide && Click](https://youtu.be/9lRIv80js\_U) (Youtube Video) | [Starter Code](https://editor.p5js.org/cmorgantywls/sketches/Ch4Ef2U90) - completed in last lesson ([p5 editor](https://editor.p5js.org/cmorgantywls/sketches/aUZv6Jll7)| [repl.it](https://replit.com/@qrtnycs4all/Collide-with-Other-Shapes-Practice-Starter-Code#script.js))
* Blank Collide2D Template ([p5 editor](https://editor.p5js.org/cs4all/sketches/H6r7sf5IW) | [repl.it](https://replit.com/@qrtnycs4all/Blank-Sketch-with-Collide2D-Library-Linked))
* [Variables in p5.js ](https://www.youtube.com/watch?v=Bn\_B3T\_Vbxs\&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA\&index=7)(make your own)&#x20;
* Video tutorial 3.4: [Boolean Variables ](https://www.youtube.com/watch?v=Rk-\_syQluvc\&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA\&index=14)
* Learning Processing book: [Chapter 3](http://learningprocessing.com/examples/chp03/example-03-05-mouse-key-events), section 5 | [Code](https://github.com/shiffman/LearningProcessing-p5.js/blob/master/chp03\_flow/)

### Assessments

Assess the **learning activity**. Check for the ability to:

* Repeat the process demonstrated in the code along&#x20;
* Create a program with clickable shape buttons

Assess the **Wrap Up** assignment. Check for the ability to:

* Explain the characteristics or patterns that informed the interface they created.

### Do Now/Warm Up (3-5 minutes)

Ask students to open up the following website and just record what they notice about how they must interact with it:

{% embed url="https://bubblespop.netlify.app" %}

### Making Shapes Clickable (10 - 20 minutes)

The brainstarter should have shown students that hovering isn’t always enough: to engage with the bubble wrap, they need to be able to click on the shapes that are on the screen. In their p5 programs, there are several ways to do this, but all of them utilize what we call event Listeners - that is, something in the program that is waiting to see if an event, like a mouse being clicked, is happening.

To start, we are going to use the mouseIsPressed variable. This variable holds a boolean variable, which either holds the value false if the mouse is not being pressed or true if the mouse is being pressed. This works great for certain situations and it’s pretty quick and easy to deal with. Later in the lesson, we will look at another way of checking of the mouse is pressed and we will compare the pros/cons of each.

Have students open their work from U2LA2.1, specifically the hover reactions they had created from [this starter code](https://editor.p5js.org/cmorgantywls/sketches/Ch4Ef2U90). With the students, show them how they can include this variable with the collide2D library in order to make the line change only when clicked. The code look something like this:

```
if(collidePointLine(mouseX, mouseY, 25,20,155,70) && mouseIsPressed){
 lineWeight = 10
}
else{
 lineWeight = 2
}
```

Once you’ve finished, ask students to go back into their code and try making all of the other shapes clickable, as well. This should not be a particularly long task; when they are done, regroup and ensure they understand that using mouseIsPressed in any conditional will determine if the mouse is being clicked or not - it does not need to take place on a shape.

### Problems Counting (10 - 20 minutes)

Now, mouseIsPressed is a great quick solution to our problem of getting information from the mouse. However, it does have some limitations which we will see in this section. If you feel that your students are really struggling with the code or with big concepts, this may be something you choose to come back to at a later date/time or split into multiple lessons to allow time to process.

Explain to students that we will be trying to make a variable that counts, or keeps score - this is the backbone of a lot of games and it’s a useful skill to have! Go ahead and start a new program with the collide library linked ([blank template for that is here](https://editor.p5js.org/cs4all/sketches/H6r7sf5IW)). Ask students to create a single ellipse in the middle - this is what you’ll be clicking on! Then declare a variable at the top of your program called score, initialize it in setup with a value of 0, and display it somewhere in the screen using the text() function. Ask students to figure out how you could make this score increase by one each time the circle is clicked. Give students time to think and work (potentially in pairs or groups) before coming together to make sure you agree on this:

```
if(collidePointCircle(mouseX, mouseY, 200, 200, 100) && mouseIsPressed){
   score = score + 1 //alternately, score += 1
}
```

This will make the score increase, but students will probably be quick to notice something odd: despite the fact that they told it to increase by 1, it will increase in jumps. Explain that this is because mouseIsPressed checks to see if the mouse is clicked in the moment the code is run - and because the draw function runs on a loop VERY QUICKLY, we are often not fast enough to lift up our finger before it loops and counts it a second, third, or even fourth time.

To help us when this problem arises, there are other tools built into the p5 library that interrupt the flow of the draw function and run only once when an action occurs. The one we will look at today is the mousePressed major callback function - but they can look on the [p5 reference sheet](https://p5js.org/reference/) under ‘Events’ if they’d like to know more for now.

Show students how to add in this function - ensuring it is completely outside of both setup an draw - and how to move the conditional they wrote earlier into this function. Explain the logic of what is happening, that this function only checks the conditional when the mouse is pressed and then only one time.

```
function mousePressed(){
  if(collidePointCircle(mouseX, mouseY, 200, 200, 100) && mouseIsPressed){
   score = score + 1 //alternately, score += 1
 }
}
```

From here, you may ask students to try to make other things clickable using mousePressed, or simply wrap up the lesson.

### Wrap Up

Ask students to respond to one or more of the following questions:

* What is the difference between the variable mouseIsPressed and the callback function mousePressed?&#x20;
* Why might you choose to use one instead of the other?&#x20;
* Which of the methods we learned today seems easier to you?&#x20;
* Describe a situation where mouseIsPressed works fine.&#x20;
* Describe a different one where you would prefer mousePressed.

### Extensions

Encourage students to further explore conditional logic by using nested if-else statements to set each shape so it is one color when a mouse is not touching it, another color when the mouse is hovering, and a third color when it is clicked.
