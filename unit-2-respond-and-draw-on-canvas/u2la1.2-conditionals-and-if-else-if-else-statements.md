---
description: How can we write multiple conditions to our code?
---

# U2LA1.2 - Conditionals and if, else if, else statements

### Overview && Teacher Feedback

This learning activity builds on the students’ knowledge of conditional statements. They will use conditional statements to create a sketch of a traffic light in future lessons that changes colors based on the mouse position, and this prepares them for that activity

Students should have a solid understanding of conditionals and how it is satisfied through a boolean. This lesson will focus heavily on creating more complex algorithms through the use of conditionals. Therefore it is important that students add comments to keep track of the sketches control flow. Students will also benefit greatly from peer programming because they can model their thinking behind their code.

During the Do Now students will review if statements through a debugging activity, it is an activity that addresses some of the common misconceptions students have when writing if statements. Modify the code to meet your students' needs.

Be sure to remind students often that most errors will stem from missing brackets { } or (). Have the review the console often to find their bugs.

The practice and play section is meant to be purposefully a bit challenging as well as to push student creativity - many students have a difficult time with which conditional is being executed based on the algorithm. Model how to test code whenever a new condition is written to help develop a student's best practice.

### Objectives

Students should be able to:

* Use an if-then statement&#x20;
* Use else if and else statements&#x20;
* Create conditions statements (event handlers)&#x20;
* Elaborate on how to satisfy a condition.

### Suggested Duration

\~2 Periods (\~90 minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create ac omputer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe different things I tried in order to achieve a goal.&#x20;
* Explain why I chose to include the specific components of my prototype over others.&#x20;
* Explain characteristics or patterns that informed a function or an interface I created.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.&#x20;
* Demonstrate the benefit of using an event, conditional or loop in my prototype.&#x20;
* Explain how a function I prototyped can be used by someone else.&#x20;
* Suggest changes to an algorithm that impacts my family or my community.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.&#x20;
* Describe how I used community research to make technical decisions in the creation of my prototype.

### **Vocabulary**

* Conditional statements - is a set of rules performed if a certain condition is met&#x20;
* Else - the second half of a conditional statement covers every outcome not specified in “if”&#x20;
* Boolean expressions - is a logical statement that is either TRUE or FALSE
* Expression - is a group of terms (the terms are separated by + or − signs)&#x20;
* Relational operators - < , > , >=, <=, && (and), || (or)

### **Planning Notes**

|                                                                                                                                                             Planning Notes                                                                                                                                                            |                                  Materials Needed                                 |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: |
| <p>Some of the examples might be too much from some students to copy so have some way students can access the links to your projects. </p><p></p><p>You’ll be using the p5 website A LOT - make sure everything linked in the lesson is unblocked and usable.</p><p> </p><p>You can assign the video tutorial as H.W. or prework.</p> | <p>Pens/Pencils</p><p></p><p>Index Cards/Half Sheets for Exit Slip (optional)</p> |

### **Resources**

* Video tutorial: [Else, and else if, AND and OR ](https://www.youtube.com/watch?v=r2S7j54I68c)
* [Else If Off the Canvas](https://youtu.be/If5VtjKP1xI) (Youtube Video) | Starter Code ([p5 editor](https://editor.p5js.org/cmorgantywls/sketches/QxTcBSExe) | [repl.it](https://replit.com/@qrtnycs4all/U2LA12-Else-If-Off-Canvas-Starter-Code#script.js))
* [Conditionals On the Canvas ](https://youtu.be/IsJ4D-2TR8c)(Youtube Video) | Starter Code  ([p5 editor](https://editor.p5js.org/cmorgantywls/sketches/B0KjtW4yo) | [repl.it](https://replit.com/@qrtnycs4all/U2LA12-Conditionals-on-the-Canvas#script.js))
* [Do now Code](http://editor.p5js.org/cs4all/sketches/S1MhAWCVX) ([p5 editor](https://editor.p5js.org/cs4all/sketches/S1MhAWCVX) | [repl.it](https://replit.com/@qrtnycs4all/U2LA12-Do-Now-Code#script.js))

### **Assessments**

**Formative Assessment:** Do now, Google form, Padlet\
**Summative Assessment:** Coding exercises, Guiding questions, code walkthrough

Assess the Do Now assignment. Check for the ability to: Identify bugs in a program and modify the code to fix them.

Assess the learning activity. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Demonstrate the benefits of using a conditional in their code.

Assess the wrap up responses. Check for the ability to:

* Define Boolean statements.&#x20;
* Define conditional statements.&#x20;
* Describe how they would use conditional statements in their programs.

### **Do Now/Warm Up (7 - 10 minutes)**

Find the bug and add comments explaining what the solution. http://editor.p5js.org/cs4all/sketches/S1MhAWCVX

Ask students to debug the sketch in order to change the color of the rectangle. There are 2 bugs 1) if statement is missing a curly bracket { 2) rect() must be written after the if statement.

Note: Bug number 2 is an error that will come up often for students who have difficulty with the control flow of a program. Control flow is an essential Computer science concept that students will need to master to create algorithms.

Ask Students to share out their solutions and explanations.

* Why does the rect() function have to come after the if statement?&#x20;
* How can we check for syntax errors**?**

### Else-If Off the Canvas (20 - 30 minutes)

This section follows the code-along youtube video linked under resources. Ask students to open and duplicate [this starter code](https://editor.p5js.org/cmorgantywls/sketches/QxTcBSExe) so they can save it into their p5.js accounts. Explain to students the existence of the ‘else if’ statement and its purpose in a program. We can use "else if" to add more possible outcomes to our sketches. Since there are often more than two possible conditions that we want to work with, we can instruct the program to perform different tasks based on a range of conditions.

I might want to tell someone that if it's cold they should wear a coat, but I also may want to say:

* "if it's freezing, wear a coat,&#x20;
* if it's cold, wear a jacket,&#x20;
* otherwise just wear a sweater."&#x20;
* We can do this by adding "else if" to our conditionals between "if" and "else."

![](<../.gitbook/assets/Screen Shot 2021-11-15 at 12.04.49 PM.png>)

The program will test each condition in order. As soon as one condition evaluates to true, the code inside those brackets is executed and the program continues after the statement.

Then code along with them a conditional to check the variable movie. If movie is ‘Ratatouille’, say ‘that movie is about a rat.’ Else if the movie is ‘Tangled’, say ‘That movie is about some hair.’ Otherwise, say ‘I don’t know that movie.’

The finished result of the code along should look like this:

```
if(movie=="Ratatouille"){
 console.log("That movie is about a rat.")
}
else if(movie=="Tangled"){
 console.log("That movie is about some hair.")
}
else{
  console.log("I don't know that movie.")
}
```

Once students have completed this, test by changing the value of the variable to get different outcomes. Then, explain that you can have many else if conditions. Then, ask students to complete one large conditional that will tell the user when their birthday is based on their sign. (They should plan for EVERY sign!)

Control flow is very important here because else if will check for multiple conditions but will only execute the first condition that is satisfied and stop then stop checking unless a new if statement is written. Using console.log() to debug and test the conditionals. Commenting is vital for this part. The traffic light problem will help reinforce this idea.

### Else If Lesson (20 - 30 minutes)

Next, students will move to working with conditionals on the canvas. This should be an easy extension to what they were doing before, except now the variables they make will change values to adjust what is happening on the canvas. [Ask students to duplicate this starter code](https://editor.p5js.org/cmorgantywls/sketches/B0KjtW4yo). (This will also follow the associated Youtube video tutorial!)

Walk students through how to create a variable to control the fill of their circle, and then write a conditional that will change the value of that variable based on mouse position. Once you are done, the conditional for this section should look like the following:

```
if(mouseX > 200){
  circleColor=color(255, 255,0)
  console.log("mouse on right")
}
else if(mouseX < 200){
  circleColor=color(255,0,255)
  console.log("mouse on left")
}
else{
  circleColor=color(0,255,255)
  console.log("exact middle")
}
```

Once students are done, ask them to repeat this process for the rectangle using mouseY. Circulate to help solve problems as students work, and if time permits, ask students to share their solutions at the end.

As you code along through the other conditional examples ensure that students are:

* Commenting their code.&#x20;
* Using variables in the correct scope.&#x20;
* Using console.log() to debug and test&#x20;
* Saving their sketches with appropriate and clear titles.

### Wrap Up

1. Students can submit code via a Google Form if you would like to collect it. If not, have students come back together for a discussion on what struggles they encountered in this activity.&#x20;
2. Students can also lead code alongs or walk through their code with the class.

**Guiding Assessment Questions:**

* What is a boolean statement?&#x20;
* What are the two responses I can get from a boolean statement?&#x20;
* What is a conditional statement and how can I use it in programming?&#x20;
* What was challenging about creating an interactive sketch with boolean and conditional statements? Why? How did you solve the challenge? What was easy?

### Extensions

Have students duplicate and modify their emojis sketches to do the following.

* Change the size of the eyes by moving the mouse to the right side of the canvas else
* The color should change if a second condition is met.&#x20;
* Add comments explaining the purpose of the conditions.
