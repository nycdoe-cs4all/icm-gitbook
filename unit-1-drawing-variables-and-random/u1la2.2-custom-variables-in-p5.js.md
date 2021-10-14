---
description: How can I create custom values to hold values in my p5.js projects?
---

# U1LA2.2 Custom Variables in p5.js

### Overview && Teacher Feedback

In this learning activity, students create their own variables to set the position, size, and grey scale color of their shapes without repeating code.

In the do-now, you will know you are doing it correctly if you hear groans of annoyance from your students. Our goal is to give them a headache so they care about the content.

We will first look at variables for values that are all the same, such as the “y” position in the example given, and discuss creating variables and moving the set of ellipses up and down.

For some students, the ideas of positions relating to another (variable) position is really confusing. If this concept is not cleared up during the code along, there are two strategies you can take:

\*For the scientific/mathematically minded students, you can break down that all coordinates are a relation of distance from something, it’s just that that something is usually the origin. This is usually best explained with graph paper in a small group or one-on-one conference with struggling students. 

\*For students who need more tangible examples, you can do an unplugged activity (this works especially well if you have tiles on your floor). Pick a student and start them on a tile. Then, select another student and position them and tell them “you two are going to move, but you still must be x tiles to the right of Sarah and y tiles down from Sarah…” Keep adding students with different positions and ask the students to shift around the room to demonstrate. This is best done as a whole class activity, as you will need room to move AND it’s a useful visual for everyone.

While it seems that we introduce position based off a point and then move on, students will get a lot of practice with this in the next lesson, and will also be required to make a design that moves cohesively as part of the mini-project at the end of the learning activity. Thus for time, we are choosing to give students more experience in reading code.

If you’ve never used DeltaMath, it is amazing and free and students can add as many teachers as they’d like. Make sure you have your teacher code handy! Pre-DeltaMath you might want to run through a problem together - it’s easiest if you write down values as you go. Additionally, keep the conversions of javascript to pseudocode posted either on chart paper or on a slide while students work.

### Objectives

Students should be able to: Identify repeated values in their code and use variables in their place. Create and implement custom variables

### Suggested Duration

2 periods (45 minutes each)

A solid period is devoted to variable practice using DeltaMath. This is **strongly** recommended for classrooms using this as an AP Computer Science Principles prep course (or classrooms where variable understanding is weak), but it can be skipped if your students already have a thorough understanding of variables in computer science. Without this addition, this lesson could easily be one period.

### Blueprint Foundations Student Outcomes

**Abstraction**:

Describe how I might use patterns to express an idea. Describe different things I tried in order to achieve a goal. Explain why using patterns is necessary when creating with a computer.

**Algorithms**:

Describe more than one set of instructions that might complete a task. Describe how instructions can have different outputs depending on inputs. Explain why I used specific instructions to complete a task. Compare and contrast my instructions with other instructions that complete the same task.

**Programming**:

Experiment with the commands of a programming language. Explain why I chose specific commands to communicate my instructions. Discuss what can and cannot be done with a specific set of commands.

### Vocabulary

**Scope** - where a variable can be ‘seen’ by the computer within a program 

**Global Variables** - variables declared outside of a function which can be used in any function. 

**Local (script) Variables** - variables declared within a function whose scope is limited to that function 

**var** - declaration of variable words in p5.js

### Planning Notes

|                                                                                        Planning Notes                                                                                       |                                                                                                                       Materials                                                                                                                       |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| DeltaMath is WONDERFUL, but make sure you’ve made your teacher account, classes, and assignment before class has started. You’ll need to distribute your teacher code for students to join. | No additional materials beyond the computer. If you want to the unplugged distance activity from the Teacher Reflection but DO NOT have a tiled floor, you might have students hold strings/yarn (keep them taught!) to stay the same distance apart. |

### Resources

* [Code Along 2 (with original code) ](http://editor.p5js.org/cs4all/sketches/H1zfOrRXX)
* Video tutorial: [2.2 Variables in p5.js (make your own)](https://www.youtube.com/watch?v=Bn_B3T_Vbxs\&index=6\&list=PLRqwX-V7Uu6Zy51Q-x9tMWIv9cueOFTFA) | [Code](u1la2.2-custom-variables-in-p5.js.md#vocabulary) 
* Learning Processing book: [Chapter 4. Variables ](http://learningprocessing.com/examples/chp04/example-04-01-declaringvars)
* Getting Started With p5.js: Chapter 4, examples 4.1, 4.2 | [Code](https://github.com/lmccart/gswp5.js-code/tree/master/04\_Variables)

### Assessments

**Formative Assessment**: DeltaMath code reading assignment

**Summative**: Emoji Project (End of Learning Activity)

### Do Now/Warm Up

Have students get computers and pull up [this code](http://editor.p5js.org/cs4all/sketches/rJsRRER7Q). Ask them to move all of the ellipses down thirty pixels. Once students start to finish getting all ellipses shifted down, ask them to move the ellipses back up 40 units. Then ask them to move everything to the right 20 units.

Once students are done, ask them what is frustrating about this process, and what might make it easier.

Students should be able to verbalize that changing every single number individually is frustrating. While most won’t be able to say that making a variable would make this a simpler process, they should be thinking that there must be someway for them to move everything together/at the same time. This is the launch to your activity!

### Position Elements with Custom Variables (15 min)

Bring students back together to briefly code-along their first custom variable.

Instead of changing values manually, explain that we can use variables instead. A variable is just a “container” that holds a value which we can then apply and quickly change values in multiple places in our code.

Remind students that there are three steps to creating a variable:

**Declare** - Declaring our variable is basically just telling the program “hey! I’m creating a variable, and this is what it’s going to be called.” All you need to do when you want to declare a variable is write the term “var variableName”. 

**Initialize** - give variableName a value. This is called an assignment operation. We are assigning a value to our variable. If I write variableName = 50, every time I use my variable name, the program will replace it with the number 50. 

**Use the variable** - Your code won’t break if you don’t use the variable, but then what was the point? If we add an ellipse at ellipse(100,100,variableName,variableName), our ellipse will be 50px wide and 50px high.

These three steps will be used in three lines of code. See the image below.

![Image shows a variable being declared, initalized, and used in a p5 program.](<../.gitbook/assets/Screen Shot 2021-10-14 at 9.42.54 AM (2).png>)

Notice where we placed these lines of code. The declared variable is way at the top before setup. We gave it a value in setup, and then use it in our draw function although we can use it in setup as well.

They should declare this variable above the setup() function, but give it a value within setup(), like so:

```
var y;

function setup() {
  createCanvas(600, 120);
  var y = 60;
}

function draw() {
	background(180);
	ellipse(120, 60, 60, 60);
	ellipse(200, 60, 60, 60);
	ellipse(280, 60, 60, 60);
	ellipse(360, 60, 60, 60);
	ellipse(440, 60, 60, 60);
}
```

**As you code, discuss the following:**

* Why are we calling our variable y? Make sure students understand that we name variables useful things so we keep track of them - you might ask them how we could make this even more precise, and then change the variable name to something like ellipseY. You should also model adding comments with your variables about what this will control. 
* Where could we use this variable? Students should tell you in the y position. 
* What value should this variable have to start? If students aren’t sure, suggest starting at 60 to make sure it runs - then you can change it from there. 
* Why do you think we named our variable above all the other functions? This is your introduction to global variables. Some students will see the visual cue that the variable is declared before we use it and that it’s used in two functions - some will not. It’s okay to explain this a bit more, they will see it again in more detail when they learn about random(). 
* Why did we need to set the value of y in the setup? This is a great question they might not grasp yet, but will during the next lesson - setup runs ONCE and sets up the value of our variable. Draw runs continuously. Right now, nothing will go ‘wrong’ if we give our variable a value in draw, but they it’s good to start getting the differences in now.

After the variable is added in, give it a few different values, running the program each time to see the change (you might want to make the canvas longer for this).

### **Move a Design with One Variable** (20 Min)

Ask students: we’ve changed the y position, but now I want to move this entire design to the left or right by changing the x, as well. Why is that going to be different from changing the y position?

Students should vocalize that the numbers are different, so they might not immediately recognize that they can use one variable. Encourage them to use one variable!

Code along with students do discuss how we could move left and right. It’s recommended that [you use this code ](http://editor.p5js.org/cs4all/sketches/H1zfOrRXX)that has the original, commented out, and the variable modified code. This will allow you to look back at where you started.

This code along will be partially on a computer, and partially drawn - if you have chart paper, that’s recommended. Don’t worry about graph paper - just worry about marking ellipses and their centers. Ask students to look at the code and pick one ellipse that will be our starter (most students will pick the far left, because that’s how we read).

Ask:

1. How far away from this ellipse is the next closest one? Students should notice that it is 80 pixels away, from looking at the x position in the code. This is where the chart paper comes in handy - you can note this distance away so students have a visual of center-to-center relationships. 
2. If I move this entire design - so it still looks exactly the same! - how far away will the next closest ellipse be? Some students may struggle with how far you’re moving the design, but it shouldn’t matter - if the design stays the same, they will still be 80 pixels apart. If students are confused, adjust circleY to show that the design moved, and ask if the distance between the circles left and right changed at all. 
3. Repeat these questions with the third ellipse, jotting down on the chart paper the relationship of the first ellipse’s center to the third. Repeat with the fourth only if needed.

Suggest to your students that you initialize the variable with the value of the first ellipse they chose. Stress that this is not what the value will always be, but it’s a useful starting place for us to test and make sure everything will stay the same before we start moving things.

Then, fill in the variable for the value of the first ellipse, and ask students what they think should happen with the second. If students say “it should be 80 more than the first one”, ask what that might look like with math. You should get this:

```
var circleY;
var circleX;

function setup() {
  createCanvas(800, 300);
  circleY = 60;
  circleX = 120;
}

function draw() {
	background(180);
	ellipse(circleX, circleY, 60, 60);
	ellipse(circleX+80, circleY, 60, 60);
	ellipse(280, circleY, 60, 60);
	ellipse(360, circleY, 60, 60);
	ellipse(440, circleY, 60, 60);
  
  //this is the original code for reference
	// ellipse(120, 60, 60, 60);
	// ellipse(200, 60, 60, 60);
	// ellipse(280, 60, 60, 60);
	// ellipse(360, 60, 60, 60);
	// ellipse(440, 60, 60, 60);
}
```

Be sure to run the program; students should notice that nothing happened, but that’s a good thing because it means the positions stayed the same even while using a variable.

Proceed with the next several ellipses - anticipate students also saying ‘80 pixels away’ for the third ellipse. Indulge their error and they should see ellipse 3 go missing - guide student thinking so they understand it’s not missing, but is just sitting on top of the second circle. Look at the original code to help correct this, reminding students that everything is in relation to the first ellipse.

Once you’ve finished (with students having numbers in increments of 80 added to each circle save the first), adjust the value circleX is starting with and notice that all circles are shifting together and staying the same distance apart.

The x coordinates should end up looking like:

```
circleX
circleX+80
circleX+160
circleX+240
circleX+320
```

### DeltaMath Variable Practice (Optional, 30-40 min)

On the [DeltaMath.com](https://www.deltamath.com) website, under Computer Science -> Pseudocode Exercises -> Setting Variable Values, there are problems that look like the following. You’ll want an assignment of 10-15 of them:

Determine what is printed by this code:

![Image shows a practice variab assignment question from DeltaMath.com](<../.gitbook/assets/Screen Shot 2021-10-14 at 10.24.58 AM.png>)

DeltaMath uses the pseudocode seen on the AP exam, so it’s not written in any actual language, but it does follow the same logic of running from top to bottom. It’s fairly intuitive, but we don’t want it to confuse any students. Before setting your students free, be sure they are aware of the following:

| DeltaMath Pseudocode |                       JavaScript                      |
| :------------------: | :---------------------------------------------------: |
|       **b ← 4**      | var b = 4 or b = 4 (if variable was already declared) |
|    **DISPLAY(b)**    |                   **console.log(b)**                  |

If students get them wrong, encourage them to use the next feature on DeltaMath to step through the code so they can understand their mistake.

### Wrap Up

You may want to bring students together to discuss successes and sticking points from the variable practice. DeltaMath does a roll up of accuracy and completion for each student, so you will have access to their data if you want to give a formative assignment grade or something similar.

### Student Assessment Guiding Questions

* What is a variable? How do you use it in your code? 
* What are the benefits of using variables? 
* How did you use variables in your project and why that way? 
* What was challenging when using variables?

### Extensions

As this lesson is mostly a code along, it is unlikely that students will race ahead of where the class is. If students are in a place to move forward, have them start trying to create their own designs, or utilize past designs such as their robot, that they can shift using variables for x and y while preserving the design itself. Creating designs that use triangles, quads, or shapes of their own creation are also useful and challenging.

You might also have them start experimenting with using mouseX and mouseY to move their design around.
