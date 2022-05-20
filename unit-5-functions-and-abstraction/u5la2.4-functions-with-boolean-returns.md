---
description: How can I create functions that return boolean values for use in my programs?
---

# U5LA2.4: Functions with Boolean Returns

### Overview & Teacher Feedback

In the past several lessons, students have engaged with functions in a way that helps their computational thinking skills, but may not be wildly applicable to projects they have made or will be making using p5.js. That all changes in this lesson, when students will create their own function to decide if the mouse is touching various shapes.

Please note that if you taught the collide2D Library instead of standard collision detection, this can still be useful, as you are essentially teaching them a basic version of what is happening behind the scenes in the collide2D Library.

### Objectives

Students will be able to...

* Write a function that returns a boolean value&#x20;
* Utilize this function in their program

### Suggested Duration

45 minutes (1 class period)

**NB**: _This could be stretched to two class periods if you would like to have them spend a period redoing a project that utilizes collision detection with the function they created. This can be great practice and can drive home the importance of functions, but is not a requirement._

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.5** Modify a function or procedure in a program to perform its computation in a different way over the same inputs, while preserving the result of the overall program.

**9-12-CT.9** Systematically test and refine programs using a range of test cases, based on anticipating common errors and user behavior.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundation Student Outcomes

**Abstraction**, **Decomposition** Ideas, problems, or projects are broken down into component parts to set the stage for deeper analysis.

**Abstraction, Pattern Recognition** Decomposed component parts are examined to find patterns like similarities, repetition, conditional relationships, or nested relationships.

**Abstraction, Generalization && Detail Removal** Component parts are grouped by general characteristics, and unnecessary details filtered out.

**Abstraction, Modularity** A process that completes a single task is more useful when it can be chained together with other processes to accomplish something more complex.

### Vocabulary

_No new vocabulary words are presented in this unit_

### Planning Notes

|                                                                   Planning Notes                                                                  |                                    Materials Needed                                   |
| :-----------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------: |
| This lesson is fairly straight forward - a brief code along followed by some student code exploration. It’s a quick and easy way to end the unit! | There are no special materials needed for this beyond computers and the starter code. |

### Resources

* Lesson Starter Code ([p5 editor](https://editor.p5js.org/cs4all/sketches/jKVdiYMg8) | [repl.it](https://replit.com/@qrtnycs4all/U5LA24-Functions-that-Return-Boolean-Values-Starter-Code#script.js))

### Assessments

Function Activity (formative)

### Do Now/Warm Up (\~3-5 Minutes)

**Display on board:** Think back to some of your past projects. What code did you find yourself repeating the most?

_Facilitate a brief share out and consider making a list on chart paper somewhere students can see - this may help them as they remix projects later in the unit. Please also encourage students to think of specific algorithms they were writing, not just ‘ellipse’ or ‘rect.’_

### Class Code Along (\~15-18 minutes)

Distribute the link to the starter code to students and explain that you are going to make two functions: one that will determine if the mouse is on an ellipse, and another that will determine if the mouse is on a rectangle. You are going to code and test the ellipse function together, and then students will work on the rectangle function on their own.

Ask students what they recall about collision with a mouse and an ellipse. Try to get a series of steps that you can leave in comments at the bottom of your code as a reference. If students are unsure or don’t remember, give them time to look through past projects. (This is a great time to reinforce the importance of commenting code!)

Once you have the steps, build the following function, asking students for assistance along the way. (They should understand what values are being taken in as inputs - these are the things that will change from ellipse to ellipse - and what the desired return value is.)

```
function isMouseOnEllipse(x, y, d){
   var distFromCenter = dist(x, y, mouseX, mouseY)

  if(distFromCenter < d/2){
     console.log("mouse on ellipse")
     return true
  }
  else{
     return false
  }
}
```

Once students have created the function, demonstrate how they could use the function in their program. Create a variable to control something about one of the ellipses on the page, utilize the variable, and then create a conditional so you have something that looks like:

```
if(isMouseOnEllipse(50, 125, 50)){
  circColor1 = color(255, 255,0)
}
else{
  circColor1 = color(0,255,255)
}
```

Ask students to reflect on if this function would have assisted in past programs, then have them try using it for the two other ellipses on the page. Consider having a student share out to demonstrate what they changed and how they used the function. It may also be useful to have students brainstorm ways they could improve this function or use it with another function (built in or of their own creation).

### Student Practice (\~10-12 minutes)

Explain to students that they will now be repeating this process, but this time making a function to determine isMouseOnRect(). They must first define the function, and then they wil use the three rectangles on the page to test it. Encourage students to once again reference past work to look for patterns that will help them to create this function.

This was not built as a pair programming activity, but students should be encouraged to collaborate and discuss with each other as they go. Once students have completed the activity, bring them together to share out their solutions and implementation.

### Wrap Up

Be sure to leave time for a student share and to revisit their original question: what other functions could they make that would improve their past or future programs? Give students time to contemplate after this activity and brainstorm if there are any ideas they would like to add to the list.

### Extensions

_This is a quick lesson, but for students who have zoomed ahead, have them start creating their own list or function library that they can use to remix past programs or improve future ones!_

One simple extension that students can pursue on their own (or as a class) is the idea of [optional and default values](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default\_parameters). Right now, their functions will break if not fed the correct information. However, having values that are optional or have default settings can help. Ask students to research and adapt their functions accordingly, and to start thinking about situations where this could be most useful.
