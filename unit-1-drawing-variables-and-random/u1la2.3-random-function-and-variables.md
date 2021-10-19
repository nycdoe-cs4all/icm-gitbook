---
description: How can we use the random function to generate different designs?
---

# U1LA2.3 Random Function & Variables

### Overview && Teacher Feedback

In this learning activity, students will understand the concept of functions in a different way because unlike other functions we have been using (i.g. ellipse and rect) random will return a value. Rect() “returns” an image by generating it onto the canvas. The random() function will be one of many functions that will be used in future units in order to make sketches more complex and interactive.

In this lesson we will introduce students to the random() function to randomize the starting positions of shapes. This lesson will reinforce the custom variable concept and offer a culminating practice to variable scope.

The do-now introduces the random function in a way that will have students read and understand how it works without being given an explanation. Expect students to struggle; very few will have completely accurate results, but some of them may “feel” that they have succeeded by having something that is centered-ish. It will be normal to see students struggle with this practice at first.

At this point students should have a basic understanding of variables and how to use them as parameters for a function. Students should be using console.log() to keep track of the numeric value of the random() function.

### Objectives

Students should be able to:

* Use random() to generate different positioning, sizing and grayscale fill
* Assign random() to a function 
* Use random() in the correct scope

### Suggested Duration

1 period (45 minutes)

### Blueprint Foundational Student Outcomes

**Abstraction:**

* Describe how I might use patterns to express an idea. 
* Describe different things I tried in order to achieve a goal. 
* Explain why using patterns is necessary when creating with a computer.

**Algorithms:**

* Describe more than one set of instructions that might complete a task. 
* Describe how instructions can have different outputs depending on inputs. 
* Explain why I used specific instructions to complete a task. 
* Compare and contrast my instructions with other instructions that complete the same task.

**Programming**

* Experiment with the commands of a programming language. 
* Explain why I chose specific commands to communicate my instructions. 
* Discuss what can and cannot be done with a specific set of commands. 
* Teach another person how to use a development environment and the basics of programming.

### Vocabulary

* **random() **- A function that returns a number in a given interval 
* **int() **- A mathematical function that converts the value into an integer.

**Pre-req vocab:**

**Integers** - All positive and negative whole numbers including zero (0).

### Planning Notes

|                                                                                               Planning Notes                                                                                              |          Materials          |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------: |
| Ensure students have access to the link or slide deck for quicker access to links. Students will need 3 tabs open for every lesson of this course:  Editor, Slide Decks (optional), P5.js Reference Guide | No extra materials required |

### Resources

* Video tutorial: [2.5 The random() function](https://youtu.be/nfmV2kuQKwA) | [Code](https://github.com/CodingTrain/website/blob/master/Tutorials/P5JS/p5.js/02/2.5\_p5.js_random/sketch.js) 
* [Random Review with Variables](https://youtu.be/I1Y0EE1ENU4) (Youtube Video)

### **Assessments**

* Formative Assessment: If you feel it is necessary, you can collect student code from any of the explorations via Google Forms or have them post links in Google Classroom. 
* Informal Assessments: Have students reflect on their problem solving process during exploration by journaling in a google doc or on paper.
* Summative Assessment: Random Emoji Project (to be completed as a mini-project at the end of LA2)

### Do Now/Warm Up (3-5 Minutes)

**Share students on **[**this sample code**](http://editor.p5js.org/cs4all/sketches/HJG9QHAmQ)**.**

Instruct students to play their code and then try to constrain the ellipse that to only half of the canvas. If students complete this task early, ask them to modify the code so that the ellipse can be placed in random position of the canvas.

While students struggle, circulate and identify one or two students who have completed the task to share their work. Plug their computer into the smartboard (or otherwise display their code).

**Ask students:** Why was this process frustrating? Why are you mad that we hit play again? Which line of code is a test that helps the user find the position of the ellipse. Students should realize it was frustrating guessing the center and that hitting play again changed their design.

### Place Elements at Random Positions (15 min)

Explain the definition of the random function and its difference from rect() and ellipse(). Then have the students code along to show how random returns different values based on the parameters it accepts.

```
random(50, 100) //returns a number between 50 and 100
random(1, 5) // returns a number between 1 and 5
random(100) // returns a number between 0 and 100
random(5) // returns a number between 0 and 5
```

Students will need to deduce what the value the random function returns. To assist them with this, your code along should show an example of how to console-log values, such as:

```
var x;
function setup() {
  createCanvas(400, 400);
  x = random(0,400);
}

function draw() {
  console.log(x)
}
```

Students will see these values print in the console, but it will not affect anything on the screen. We will use console.log() frequently to debug and test sketches.

If students do not point out that random() returns a decimal and not an integer then show them what random() returns using console.log().

If students would like to return whole number we recommend introducing the int() function as seen in the example below. The concept of wrapping/nesting functions around one another may be new, tell students that the most inner function in called fist and then it works it way to the outer functions similar to how order of operations works.

x = int(random(0, 400))

Once students are comfortable, set them several pair-programming tasks for them to practice before moving on to the next section. For example, you might have them:

Make an ellipse that is…

* Begins at a random location anywhere on the canvas after pressing play 
* Add a second ellipse that begins with a random size 
* Add a rectangle that begins with a random grey fill

Teachers should circulate and make notes of struggling students for conferencing or remediation. Students should be adding comments to their code to differentiate each shape they are making and where it -should- be appearing.

After students are done with practicing using the random function have them code along initialize the random() function inside the draw function. They will notice the that the ellipse does not stop moving its position. Make sure to point out that console.log is always updating.

```
var y;
function setup() {
  createCanvas(400, 400);
}
function draw() {
  background(220);
  x = random(0,width);
  ellipse( x, 100 , 100, 100 )
  console.log(x)
}
```

**Ask Students**:

* Why is the ellipse doesn’t stay in one place? 
* Explain how the draw function works and how it affects the location of the ellipse. 
* Where would be the best place to initialize the random function?

### Wrap Up (5 Min)

Display several examples of student work with successes in changing colors and sizes. You will also want to choose and display several examples of students who attempted to get a triangle to move with the random function.

If your class struggled, base your discussion around problems they encountered rather than a tutorial. If they are close to finding a solution and you have extra time, you can walk them through in a code-along, but do not anticipate or force getting to that place.

**Student Assessment Guiding Questions:**

* Why is difficult to move the entire triangle together using random()? 
* How can we use custom variable to help us move shapes? 
* How can we use the random function to create games in the future?

### **Extensions**

1. Ask students to work with a partner to try and create a triangle using variables and the random function to appear anywhere on the canvas while staying the same size. 
2. Use the random function to create a random canvas size every time play is pressed while having an ellipse staying in the center of the canvas no matter the canvas size. (Hint: use custom variables)
