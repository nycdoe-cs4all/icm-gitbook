---
description: How can we add conditional statements to make our programs more interactive?
---

# U2LA1.1 - Conditionals and if statements

### Overview & Teacher Feedback

This learning activity introduces booleans and conditional statements. Before students begin making conditionals to control visual parts of the canvas, they take a moment to think about the logic of coding off-canvas. Students will then create an interactive sketch that includes a visual element that changes based on a condition.

This is one of the first lessons that takes a trip off the canvas for students to practice JavaScript syntax and logic. While it may be frustrating or seem dull to not be making creative coding pieces, it is useful for long-term student understanding for them to have the practice without the stress of getting everything to look just right. If you are teaching this curriculum to students with significant coding experience, please feel free to skip or speed up these sections as needed.

At this point, students have seen mouseX and mouseY and should understand that they hold a changing value. Students may wonder why conditions are important tell them that now it is time to make our sketches interactive and “intelligent” by adding a decision-making condition.

During the “Do Now” students will begin to understand how conditions can be satisfied in everyday life. You might have to refer to this example throughout the lesson so students can see what it takes for a condition to be true.

The practice and play section is meant to be purposefully a bit confusing as well as to push student creativity - many students have a difficult time divorcing that color changes are made by the PROGRAMMER, and are not automatic just because they wrote “if statements”. Having reactions occur on different hovers is a terrific stretch. Add steps as needed -this can easily be scaled up or scaled-down. Students should add clear comments explaining how the condition can be stratified. In order to build best practices be sure to model that in every example.

### Objectives

Students should be able to:

* Use an if-then statement&#x20;
* Create conditional statements (event handlers)

### Suggested Duration

\~2-3 periods (90 - 135 minutes)

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe how I might use patterns to express an idea.&#x20;
* Explain characteristics or patterns that informed a function or an interface I created.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.&#x20;
* Demonstrate the benefit of using an event, conditional or loop in my prototype.

**Programming**

* Experiment with the commands of a programming language.&#x20;
* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.

### Vocabulary

**Conditional statements** - is a set of rules performed if a certain condition is met&#x20;

**Boolean expressions** - is a logical statement that is either TRUE or FALSE

**Prereq Vocab:**

1. Expression - is a group of terms (the terms are separated by + or − signs)&#x20;
2. Relational operators - < , > , >=, <=, && (and), || (or)

### Planning Notes

|                                                                                                                                                                                 Planning Notes                                                                                                                                                                                |                                  Materials Needed                                 |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: |
| <p>Some of the examples might be too much for some students to copy so have some way students can have direct access to your project links. </p><p></p><p>You’ll be using the p5 editor website A LOT - make sure everything linked in the lesson is unblocked and usable. </p><p></p><p>You can assign the video tutorial (“Conditional Statements”) as H.W. or prework.</p> | <p>Pens/Pencils</p><p></p><p>Index Cards/Half Sheets for Exit Slip (optional)</p> |

### Resources

Video tutorial: [Conditional Statements](https://www.youtube.com/watch?v=1Osb\_iGDdjk)&#x20;

[Pseudocode Conditionals Worksheet ](https://docs.google.com/document/d/1YPoLb9IEiLTQLOl2bu2JtVLNOOg0KTbmq\_x0g64UHPc/copy)

[Pseudocode Conditionals](https://youtu.be/1CJaGL9dQBA) (Youtube Video)&#x20;

[Conditionals Off-Canvas](https://youtu.be/28BONkrInyY) (Youtube Video) | [Starter Code](https://editor.p5js.org/cmorgantywls/sketches/FZDxLCBiS)

### **Assessments**

Formative Assessment: Google form&#x20;

Summative Assessment: Guiding questions, code walkthrough

Assess the learning activity. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Use conditional statements to add different potential outputs to their code.

**Assess the wrap-up responses. Check for the ability to:**

* Define conditional statements.&#x20;
* Describe how they would use conditional statements in their programs.

### **Day One Do Now/Warm Up (7 - 12 Minutes)**

Distribute the [Pseudocode Conditional Worksheet](https://docs.google.com/document/d/1YPoLb9IEiLTQLOl2bu2JtVLNOOg0KTbmq\_x0g64UHPc/copy) to students. Ask them to fill out just the first column, and if necessary, offer suggestions for the first example to get them started. The rest they should be able to complete on their own. Ask them to, for now, ignore the second column.

After students have had time (\~3-5 minutes) to work on the first column, ask for some student shares, and then explain how you complete the second column by putting the plain English conditionals they’ve written into pseudocode.

Give students another \~5 minutes to complete the second column after you’ve given an example, and then review briefly before using this to launch into the coding portion of the lesson. For example:

|                    Action                    |                                         If/Else Statement                                        |                                                               Pseudocode                                                               |
| :------------------------------------------: | :----------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------: |
| **ACTION**: Go to the park with your friends | If (the weather is nice), then (I go to the park with my friends), else (I watch netflix inside) | <p>if(the weather is nice){ </p><p>I go to the park with my friends </p><p>} </p><p>else { </p><p>I watch Netflix inside. </p><p>}</p> |

Give students another \~5 minutes to complete the second column after you’ve given an example, and then review briefly before using this to launch into the coding portion of the lesson.

It is important that students understand that an expression will evaluate to true or false. Then the computer will perform an action based on the given condition. Some students may ask where the words true and false words actually appear but tell them that the words are actually activation signals that the computer can only see. Much like a light’s ON and OFF switch, when the light is flicked on because it is on the On position the condition is met but the word ON is not actually seen. Students may need more examples so refer to the do now for more.

We want the computer to look at an expression and evaluate whether it is true or false, if it's true do one thing, and if it's false do another. Let's take a look at some expressions and evaluate them as true or false.

* 26>5 → 26 is greater than 5. Let's read that as a question. Is 26 greater than 5? Yes it is. This expression evaluates to "true."&#x20;
* 10=14 → Since 10 is not equal to 14. This expression evaluates to "false"&#x20;
* 4>210 → This expression is also "false"&#x20;
* 2=2 → "true"

These "greater than" or "less than" signs are relational operators - they compare two numbers, which is what we're going to do in our first conditional statement.

The boolean expression inside the parentheses is the expression being evaluated. If the expression is true, then the computer will execute the code inside the curly brackets. If it evaluates to false, the code is not run and the program will continue with the code that follows the expression.

![](<../.gitbook/assets/Screen Shot 2021-11-10 at 9.54.03 AM.png>)

### **Conditionals Off Canvas (20-30 Minutes)**

Share students on this [starter ](https://editor.p5js.org/cmorgantywls/sketches/FZDxLCBiS)[code](https://editor.p5js.org/cmorgantywls/sketches/FZDxLCBiS) and direct them to make a copy so they can save it to their p5.js editor accounts. This tutorial follows the instructional Youtube video linked under resources if you would prefer to use that to help you prepare for the lesson.

Explain that this starter code will not use the canvas and will run entirely behind the scenes, in the console. There are already some variables created with values as well as prompts for what students will be doing. Complete the noted code along with students to create code that will say ‘I love your music!” if theName says Beyonce and for all others will say ‘Nice to meet you!’ The finished result should look like this:

```
if(theName == "Beyonce"){
 console.log("I love your music!")
}
else{
 console.log("Nice to meet you.")
}
```

After, review with students the meaning of the == and that there are other comparative operators they can be using. Additionally, ensure they are aware that while we put strings - what they are currently seeing as words - in quotes, we do not for numbers.

* \== the same as&#x20;
* != not the same as
* **<** greater than&#x20;
* <= greater than or equal to&#x20;
* < less than&#x20;
* <= less than or equal to

Then, ask students to complete the remaining prompts while you circulate and assist. If you’d like, this could be an opportunity for pair programming or other collaboration.

Consider collecting this activity from students at the end so you can review before their second day of this content.

### Second Half OR Day Two Launch (5-10 minutes)

Based on student work from the previous day, display code that contains a common mistake (or mistakes) on the board. It may be helpful to also say ‘This code has # of mistakes… can you identify them?’

Ask students to identify AND determine fixes for the mistakes before you continue on.

### Boolean and Conditional Lesson (30 min)

Review with students that it is important that students understand that a boolean expression in a conditional statement will evaluate to true or false. Then the computer will perform an action based on the given condition. Some students may ask where the words true and false words actually appear but tell them that the words are actually activation signals that the computer can only see, unless you’re using console.log. Much like a light’s ON and OFF switch, when the light is flicked on because it is on the On position the condition is met but the word ON is not actually seen. Students may need more examples so refer to the do now for more.

Bring students back for the code along. Create a shape on the screen with a variable to hold its color - remind students how to declare, initialize, and use a variable, and then how to change the color variable in a conditional. Create a change so that when the mouse is on one side of the screen, the color changes, and then changes back to the original. Use console.log(mouseX) so that students can see how the condition in the if statement is satisfied. Move the mouse back and forth a few times so that the shape changes color when mouseX increases and decreases: our sketch is now interactive and responsive to the user moving the mouse! At the end of the code along, you should have created something to the effect of:

```
function setup(){
  createCanvas(400,400)
  circSize = 100
}

function draw(){
  background(220)
  ellipse(200,200,circSize,circSize)

  if(mouseX>200){
    circSize = 200
  }
  else{
    circSize = 100
  }
}
```

As you code along through the other conditional examples ensure that students are:

* Commenting on their code. (Model examples for students as needed)&#x20;
* Using variables in the correct scope.&#x20;
* Using console.log() to debug and test&#x20;
* Saving their sketches with appropriate and clear titles.

Once they are done, ask students what else they could change about this shape or other things in the sketch, such as the background. Have them create variables and use them to change values of the shape itself when the mouse is in different positions, or create different shapes and variables to change with conditionals.

### Wrap Up (10 minutes)

Students can submit code via a Google Form if you would like to collect it. If not, have students come back together for a discussion on what struggles they encountered in this activity.&#x20;

Students can also lead code-alongs or walk through their code with the class.

Guiding Questions

* What is a boolean statement?&#x20;
* What are the two responses I can get from a boolean statement?&#x20;
* What is a conditional statement and how can I use it in programming?&#x20;
* What was challenging about creating an interactive sketch with boolean and conditional statements? Why? How did you solve the challenge? What was easy?

### Extensions

If students have a good grasp of algorithms then they should be able to complete the extension.

Directions:

Create a condition that will change the fill of a rectangle if the mouse is hovering over the rectangle. Hint: You could use && (and) to combine conditions

Adapt a previous sketch to add interactivity to it.
