---
description: How can I use my skills in p5 to create a drawing application?
---

# 🎨 🎨 Unit 2 Final Project: Interactive Drawing App

![Image of MS Paint circa 2001](<../.gitbook/assets/Screen Shot 2021-11-04 at 11.54.58 AM.png>)

### Prompt

Remember the days of Microsoft Paint? When you could click a start bar, open a program that came preloaded on the computer, and just create? Those days were good. Those days were simple. Those days were internet free and possibly came with very little in the way of design sense.

We are better today; we have the tools needed to build our very own, p5 Microsoft Paint that looks better than ever before. And so that’s what we are going to do!

**Requirements**:

1. Create a program that allows you to draw with the mouse.&#x20;
2. Create at least 4 buttons that will control different aspects of the program, such as color changes.&#x20;
3. Create at least 4 key press reactions that will control different aspects of the program, such as brush type.&#x20;
4. Utilize objects to control multiple attributes of the same element (such as the drawing tool), or the same attribute of multiple elements (such as the button colors).
5. Make sure the user understands how to use your program!
6. **BONUS REQUIREMENT**: Make your canvas saveable by following the instructions under the extension!

**Writing Prompt:**

Write a sales pitch for your program that includes instructions on how to use it and persuasive reasoning behind why you made your specific design choices.

### **Sample Output**

![](<../.gitbook/assets/Screen Shot 2021-11-04 at 11.55.17 AM.png>)

### **Extensions**

|        Mild        |                                                                             Medium                                                                            |                                                                                                                          Spicy                                                                                                                         |
| :----------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Meets requirements | <p>At least 5 buttons</p><p><br>Create a drawing pen using the mouse ONLY when the mouse is being pressed </p><p></p><p>Have one button be a random color</p> | <p>All medium requirements plus the following… </p><p></p><p>Make an eraser Make a way to clear the canvas </p><p></p><p>Make complex brush types, beyond just drawing with different shapes </p><p></p><p>Create a website to house your creation</p> |

#### OPTIONAL EXTENSION: Make Your Canvas a Saved Image

_You are welcome to briefly teach students how to program in a save option using the_ [_built in saveCanvas() function_](https://p5js.org/reference/#/p5/saveCanvas) _or_ [_save function_](https://p5js.org/reference/#/p5/save)_. The former requires the canvas to be stored in a variable, but the latter will just save an image of the canvas by default. If you choose to introduce this to students, they should use them in a major callback function outside of the draw function to avoid repetition, such as mousePressed or keyPressed, like so:_

```
/// Option 1 - mousePressed major callback
//mousePressed happens outside of and after draw (built in event listener for p5.js)

function mousePressed(){
   save("myCanvas.jpg")
}
```

```
// Option 2 - keyPressed major callback
//keyPressed happens outside and after draw (built in event listener in p5.js)

function keyPressed(){
  if(key==='s'){
    save("myCanvas.jpg")
  }
}
```

### Overview && Teacher Feedback

This culminating project of Unit 2 challenges students to make an interactive application that will allow a user to draw (and change their drawing tool in a variety of ways). Some students will approach this head on and make very obvious drawing applications, and some will enjoy an opportunity to flex and explore their design skills. Both are fantastic approaches to this project.

This is a complex project, and students will need to carefully manage their code to avoid getting lost. Encourage them to use comments as often as possible to keep things straight!

This will be the most challenging project students have encountered so far, as it requires combining many skills and dealing with a complex control flow. Students may need help ‘chunking’ their project so they do not become overwhelmed and try to do everything at once.

Suggestions for this are available in the Project Introduction, but you can also create worksheets or other resources if you think it will help your students navigate the creation of their drawing application.

### Objectives

Students should be able to:

* Showcase skills learned in Unit 2&#x20;
* Create a drawing application with button and key press reactions that allows the user to draw with the mouse

### Suggested Duration

1-2 45 minute periods for launch & Planning&#x20;

3-4 45 minute periods for work time

_This is all quite subjective; in early projects, you should adjust pace to suit your students so they can make something they are proud of. But this project should take about a week._

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe different things I tried in order to achieve a goal.&#x20;
* Explain why I chose to include the specific components of my prototype over others.
* Explain characteristics or patterns that informed a function or an interface I created.
* Explain why using patterns is necessary when creating with a computer.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.
* Demonstrate the benefit of using an event, conditional or loop in my prototype.&#x20;
* Explain how a function I prototyped can be used by someone else.&#x20;
* Suggest changes to an algorithm that impacts my family or my community.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.

### **Planning Notes**

|                                                                                        Planning Notes                                                                                        |                                              Materials Needed                                              |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------: |
| See above for timing - students should be held accountable for getting things done each day through a series of check ins, but they also need a chance to make something meaningful to them. | **No extra materials required, but you may want extra paper or coloring materials for planning purposes.** |

### **Assessments**

_**This project serves as the final summative Assessment for Unit 2.**_&#x20;

Assess the final project. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Create a program that can has different outputs based on different key and/or mouse inputs&#x20;
* Create a creative drawing program.

Assess wrap ups and progress. Check for the ability to:

* Describe different things they tried in order to achieve a goal.&#x20;
* Explain why they chose to include the specific components of their prototype over others.&#x20;
* Explain how their prototyped can be used by someone else.

### Do-Now/Warm Up

Ask students to go back to the good ol’ days and think about MS Paint (or any other drawing application). What could you do with it? What couldn’t you do?

### Prompt Intro Guidance

This is a big project as there is a lot of control-flow happening here beyond just drawing order. It is useful to ask students to consider an MVP - minimum viable product - before beginning, and plan around that. You can do this easily with planning worksheets.&#x20;

To keep track of student progress, ask them to take a piece of paper and fold it into thirds. Label each one ‘NOW,’ ‘SOON,’ and ‘LATER.’ Students should write on post its what they need to do to complete their MVPs and put in appropriate columns. Things the finish from now will be removed from the paper, and then items from soon and later will move up. It is recommended to have students complete this or some sort of planning activity before they begin!

### Wrap-Up

A good practice, especially during long term projects, is to have students share their progress. You can do this through volunteers, or as is my preference, through random selection.&#x20;

This share out method can be used outside of project time, as well. Use a calendar to sign up 1-2 students per day, working your way through your roster (and then repeating once you reach the end). Each day, be sure to conference or check in with students who will share so they are aware they are sharing and also know what they will talk about. Students can share successes or struggles - if they share a success, they should focus on what they did to make it happen (so the class can learn). If they share a struggle, they should ask questions that the class can then assist them. Allow about 5 minutes for both shares.
