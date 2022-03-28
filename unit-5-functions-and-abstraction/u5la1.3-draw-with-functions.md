---
description: How can I create a function that will draw a design?
---

# U5LA1.3: Draw with Functions

### Overview & Teacher Feedback

In this lesson, students will write their first custom function that will perform an action on the screen. Today, that action will be to draw a smiley face (or other design of your choosing, if you’d like to showcase something else!).

This lesson is very teacher-heavy as students get introduced to the thought process behind writing functions. However, it is immediately followed by a mini-project that will allow them to complete work independently and explore some of these ideas on their own.

### Objectives

Students will be able to...

* Create a function that draws a design&#x20;
* Incorporate parameters to control aspects of their function such as position

### Suggested Duration

1 Period (\~45 minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.5** Modify a function or procedure in a program to perform its computation in a different way over the same inputs, while preserving the result of the overall program.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Abstraction, Generalization and Detail Removal:** Component parts are grouped by general characteristics, and unnecessary details filtered out.

### Vocabulary

* Function&#x20;
* Arguments&#x20;
* Parameters

### Planning Notes

|                                                                            Planning Notes                                                                           |                     Materials Needed                    |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------: |
| This lesson is mostly delivered in a code along. Prior to the lesson, ensure you have a working Smartboard/Projector and students have computers available to them. | _No materials needed beyond computer and starter code._ |

### Resources

* [Starter Code](https://editor.p5js.org/cs4all/sketches/gO8RjHdqA) (p5 Editor)&#x20;
* [Your First p5.js Abstraction ](https://youtube.com/playlist?list=PLc2XcmagK0XEqNrnwC5vbJ4dW5qOCIUFK)(YouTube)

### Assessments

* **happyFace()** function (Formative)&#x20;
* **angryFace()** function (Formative)

### Do-Now/Warm Up (\~5 Minutes)

Display link to starter code and ask students to duplicate the code so they can be ready to begin the lesson. If you would like, this is also a great place to put an SEL check, like asking students to complete a mood meter, journal, or otherwise react to how their day or week is going.

### Code Along: Happy Face (\~20 Minutes)

In this code along, you will build a function called **happyFace()** that will take the existing code for the happy face and turn it into a function. While the first step in the code along is always the same, subsequent steps can be a choose-your-own-adventure based on how your class has performed on past skills from the transformation lessons.

To begin, explain to students the setup of functions. At the bottom of the starter code, begin by setting up an empty function, explaining each piece, like so:

```
//Write your functions down here!
function happyFace(){

}
```

From there, take the code for the happy face - lines 11 - 17 - and copy/paste them into the function. Remove them from the draw() function so you have something that looks like this:

```
function setup() {
  createCanvas(400, 400);
  angleMode(DEGREES)
}

function draw() {
  background(220);
  text(mouseX + ", " + mouseY, 20, 20)
  
  //Happy Face
  
  //Angry Face
  noStroke()
  fill(235, 161, 70)
  ellipse(275,200,100)
  strokeWeight(2)
  stroke(0)
  line(270,196,289,183)
  line(254,196,237,188)
  strokeWeight(1)
  arc(284,200,25,25,0,180)
  arc(261,232,20,40,180,0)
  arc(245,200,15,25,0,180)
  
}

//Write your functions down here!
function happyFace(){
  strokeWeight(1)
  stroke(0)
  fill(169, 222, 183)
  ellipse(125,200,100)
  arc(110,200,25,25,180,0)
  arc(160,200,15,25,180,0)
  arc(136,226,40,10,0,180)
}
```

Students will notice that the happy face has disappeared. Explain that now the function has been DEFINED, you can CALL it in the draw function. In the draw function, write happyFace() below the comment so it reappears. This may not seem super impressive to students - it’s where they started, after all - but the benefit of this method is that now they can make MANY happy faces. Ask students how they could make more and prompt them to the idea of writing the function call several times if needed. They will notice a problem - there is still only one happy face. Ask students why this is - many will realize it’s because it is drawing at the same place every time.

This is your chance to choose a code along path that is most sensible to your students from the options below!

#### Option A:&#x20;

* Students will create parameters for x and y&#x20;
* Students will use this x and y to control the positions of each shape, adding and subtracting to keep the distances correctly related to each other.
* _This is an easy and direct approach for students who may not have felt comfortable working with push(), pop(), and translate()._

```
//Final Product
function happyFace(xPos, yPos){
  strokeWeight(1)
  stroke(0)
  fill(169, 222, 183)
  ellipse(xPos,yPos,100) //125, 200
  arc(xPos-15,yPos,25,25,180,0)
  arc(xPos+35,yPos,15,25,180,0)
  arc(xPos+11,yPos+26,40,10,0,180)
}
```

#### Option B:

* Students will create parameters for x and y&#x20;
* Students will use this x and y to control the translation of the shape, and will rewrite the shape to draw from 0.&#x20;
* Be sure to include a push and pop so the translation only applies in the function!
* _This option is fantastic for students who excelled in the transformation lessons and have been applying them in their code to increase efficiency. It may confuse students still struggling with the coordinate system._

```
//Final Product
function happyFace(xPos, yPos){
  push()
    translate(xPos,yPos)
    strokeWeight(1)
    stroke(0)
    fill(169, 222, 183)
    ellipse(0,0,100) //125, 200
    arc(-15,0,25,25,180,0)
    arc(35,0,15,25,180,0)
    arc(11,26,40,10,0,180)
  pop()
}
```

#### Option C:

* In this option, start with Option A, and then ask students if they have learned anything that would make moving many shapes easier. Once they get to translation, revise the function.
* This would also be a terrific second day activity, or something to bring out as an extension when students work on the mini project.

Once students have a working function and can use the function call several times to draw many smileys, ask them what else they may want to change about the smiley. Rather than coding that in now, ask them to include comments to come back to later.

### Independent Practice: Angry Face (\~10 minutes)

Explain to students that they will now practice what they’ve learned by turning the angry face into a function. You can choose to have students work alone or to pair program. If they are pair programming, have them swap after each 2-3 steps/new lines of code!

### Wrap Up

Time permitting, consider having one or two students share their solutions with the class, or having students feeling stuck share their non-solution to get feedback from the class.

You may want to collect their work (via Google Form or similar) to review the functions they have written as an exit ticket. Consider having them add any questions they still have as comments before submitting!

### Extensions

_**After this lesson, students will be creating functions of their own unique designs. Encourage students to try for the most efficient way to write their functions now, and if they need more to do, ask them to review a previous design - like the taijitu symbol - and turn it into a function.**_
