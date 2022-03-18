---
description: How can we utilize p5.js system variables?
---

# U1LA2.1 Intro to Variables - System Variables

### Overview && Teacher Feedback

In this learning activity, students will understand the concept of built in variables and place shapes on the canvas using the variables width , height, mouseX, mouseY. They are also introduced to rectMode() to change the location from which shapes are placed. They will create a visual composition using these built in variables that will remain consistent when the canvas size is changed to demonstrate the concept of design systems.

This learning activity is split into three parts:

System variables\
Custom variables\
Use of random() function

In lesson 1, we will introduce students to the concept of console.log() to display variable values and will introduce system variables that can be used in their design. This lesson is meant to be a straightforward introduction to variable use.

The do-now introduces a headache to make students care about the built in width and height variables. Expect students to struggle; very few will have completely accurate results, but some of them may \~feel\~ that they have succeeded by having something that is centered-ish. Accept that since you’re going to rain on their parade anyway.

Note: we have chosen to use console.log() over print(), as print() is more unique to the p5 library and console.log() is more universal across javascript.

Paired programming should always have equal number of “at bats” for each student.

Many students will struggle with getting a triangle to move together - expect many to either have their triangle reduced to a point (because they make every argument either mouseX or mouseY) or have just one vertice drag with the mouse. It is not anticipated that most students will succeed, but it lays good groundwork for the final mini-project students will do at the end of the learning activity.

If you attempt to tackle the triangle solution with your students, you might ask students to come up to the board and code out a solution, with one student making a change to an argument before passing it to someone else.

### Objectives

**Students should be able to:**

* Use width and height
* Use mouseX and mouseY to move a shape
* Use system variables as parameters for functions.

### **Suggested Duration**

\~1 period, 45 minutes

### Blueprint Foundational Student Outcomes

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Abstraction:</strong><br></p><ul><li>Describe different things I tried in order to achieve a goal.</li></ul><p><strong>Algorithms:</strong><br></p><ul><li>Describe more than one set of instructions that might complete a task.</li><li>Describe how instructions can have different outputs depending on inputs.</li><li>Explain why I used specific instructions to complete a task.</li></ul><p><strong>Programming:</strong><br></p><ul><li>Experiment with the commands of a programming language.</li><li>Describe three ways a development environment helps me create a project.</li><li>Discuss what can and cannot be done with a specific set of commands.</li></ul> |

### Vocabulary

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li><strong>Variables -</strong> in CS, variables hold an assigned value or data of a specific type, they can also hold arrays of values which will be introduced later.</li><li><strong>width -</strong> system variable that holds width of canvas as declared in set up</li><li><strong>height -</strong> system variable that holds height of canvas as declared in setup</li><li><strong>mouseX -</strong> system variable that holds the current x-position of the mouse</li><li><strong>mouseY -</strong> system variable that holds the current y-position of the mouse</li><li><strong>console.log() -</strong> a function that logs a value to the console when the program is run.</li></ul><p><strong>Pre-Req Vocab:</strong><br></p><ul><li><strong>Width -</strong> Horizontal distance of a 2D shape</li><li><strong>Height -</strong> Vertical distance of a 2D shape</li></ul> |

### **Planning Notes**

|                                                                                                                                 Planning Notes                                                                                                                                |                   Materials Needed                   |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------: |
| <ul><li>Ensure students have access to the link or slide deck for quicker access to links.</li><li><p>Students will need 3 tabs open for every lesson of this course</p><ul><li>Alpha Editor</li><li>Slide Decks (optional)</li><li>P5.js Reference Guide</li></ul></li></ul> | _No extra materials required outside of a computer._ |

### Resources

* [2.1 Variables in p5.js](https://www.youtube.com/watch?v=diGjw5tghYU)
* [2.2 Variables in p5.js (Make your own)](https://youtu.be/Bn\_B3T\_Vbxs)
* [mouseX, mouseY, intro to random()](https://youtu.be/EgDvu4itXRQ) (Youtube Video w/ Coding Activity)

### Assessments

**Formative Assessment:** If you feel it is necessary, you can collect student code from any of the explorations via Google Forms or have them post links in Google Classroom.

**Informal Assessments:** Have students reflect on their problem-solving process during exploration by journaling in a google doc or on paper.\
\
**Summative Assessment:** Emoji Project (to be completed as a mini-project at the end of LA1)

### Do Now/Warm Up (\~4 - 8 min)

Share students on [this sample](http://editor.p5js.org/cs4all/sketches/S1eQDQRXX) code.

Instruct students to play with their code and then try to create an ellipse that is perfectly centered in their canvas. If students complete this task early, ask them to make the ellipse large enough so that the ellipse touches each edge of the canvas (if their canvas is square - if it comes out as a rectangle, touching the top and bottom will suffice).

[Click Here - Center the ellipse challenge code](http://editor.p5js.org/cs4all/sketches/S1eQDQRXX)

While students struggle, teachers will circulate and identify one or two students who have completed the task to share their work. Plug their computer into the smartboard (or otherwise display their code) - hit play again and the canvas values should reroll, creating a new canvas in which the circle is not necessarily centered.

Ask students: Why was this process frustrating? Why are you mad that we hit play again?

Students should realize it was frustrating guessing the center and that hitting play again changed their design, thus ruining all of their hard work.

### **Center Elements With Built-In Variables Width and Height (10 min)**

Explain the definition of variables to students, and then code along to have students perfectly center their ellipse using width and height as parameters for the x and y values.\
\
Students will need to deduce that they need to divide these numbers in half to achieve a centered look. To assist them with this, your code along should show an example of how to console-log values, such as:

```
console.log(width)
console.log(width/2)
```

Students will see these values print in the console, but it will not affect anything on the screen. We will use console.log() frequently to debug and test variables.

Once students are comfortable, set them several pair-programming tasks for them to practice before moving on to the next section. For example, you might have them:

Make an ellipse that is…

* ⅓ of the way across the screen
* ¼ of the way across the screen
* ⅔ of the way across the screen
* ¾ of the way across the screen

Teachers should circulate and make notes of struggling students for conferencing or remediation. Students should be adding comments to their code to differentiate each shape they are making and where it -should- be appearing.

### mouseX, mouseY (10 min)

Students should come back together to discuss what other system variables exist (answer - many). Show students the line of code below and ask them to explain why it was useful:

```
function setup() { 
	createCanvas(600, 120);
}

function draw() { 
	background(100);
	text(mouseX + ", " + mouseY, 20, 20);
}
```

Explain to students that we can also use mouseX and mouseY in our functions as parameters to change our shape based on the position of the mouse, or make shapes follow the mouse. With students, code along an ellipse that follows the mouse.

Then, ask students to make a rectangle with their partner that follows the mouse. After 1-2 minutes, ask students to come back together and explain what is different between the ellipse and the rectangle. Students should recognize that the ellipse “attaches” to the mouse at its center, while the rectangle follows the upper left corner.

Use this as a launch to explain rectMode() and how it can be used to help position rectangles if students want them centered. Sometimes if students are doing calculations based around a point, rectMode on the center might make things a bit more difficult.

Once students are comfortable with using mouseX and mouseY with the position of the shape then have them…

* Use mouse X and/or mouseY to change the height or width of a rectangle
* Use mouse X and/or mouseY to change the height or width of a ellipse
* Use mouse X and/or mouseY to change shade of the canvas
* Use mouse X and mouseY to change the fill of a rectangle or ellipse

### Wrap Up (5 min)

Display several examples of student work with successes in changing colors and sizes. You will also want to choose and display several examples of students who attempted to get a triangle to move with the cursor - don’t plan on picking perfect triangles (if students did succeed, pick them last).

If your class struggled, base your discussion around problems they encountered rather than a tutorial. If they are close to finding a solution and you have extra time, you can walk them through in a code-along, but do not anticipate or force getting to that place.

**Ask Students:**

1. **How does math play a role in our p5.js sketches ?**
2. **What are the way we can use system variables in our sketches?**
3. **How can comments help us out when using variables?**

### Extension

After students have a rectangle with their cursor, ask them to work with a partner to try and create a triangle that follows the mouse. [Possible Solution](http://editor.p5js.org/cs4all/sketches/H1-8b6nN7)

Many students will struggle with getting a triangle to move together - expect many to either have their triangle reduced to a point (because they make every argument either mouseX or mouseY) or have just one vertice drag with the mouse.\
It’s not anticipated that most students will be successful, but if they are, challenge them to use something like quad() or beginShape() (see p5 reference sheet) that will travel with the mouse.

\\
