---
description: How can the map function help me control a range of values?
---

# U2LA1.5: The Map Function

### Overview && Teacher Feedback

This learning activity introduces the map function and applies it to changing a sketch\`s background color to grayscale, and RGB color ranges.

This lesson is primarily a code-along, followed by oodles of student exploration via pair programming.

Make sure students enlarge their canvas - it will make the map feature way more obvious. Some students will overthink the do now - it’s really just one line of code, so encourage them to think simply if their brains start swimming in the deep end of the pool.

### Objectives

Students should be able to:

* Explain the purpose and use of the map function&#x20;
* Apply the map function within their projects

### Suggested Duration

1 period (\~45 minutes)

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe different things I tried in order to achieve a goal.&#x20;
* Explain why I chose to include the specific components of my prototype over others.
* Explain characteristics or patterns that informed a function or an interface I created.

**Algorithms**

* Describe how instructions can have different outputs depending on inputs.
* Demonstrate the benefit of using an event, conditional or loop in my prototype.&#x20;
* Explain how a function I prototyped can be used by someone else.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.

### Vocabulary

**map**() - A built-in p5.js function that re-maps a number from one range to another.

### Planning Notes

|                                                                                             Planning Notes                                                                                             |                                                                                                                                                                  |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| This lesson is scheduled to take one period, but students may finish more quickly; if they do, it is meant to call back to the last learning activity. Give students s much time as they need to work! | Only a computer is required, but you may want pads of paper or other wireframing supplies to help students express their ideas if they are struggling with code. |

### Resources

* [The Map Function](https://youtu.be/B-wsiuuT-HM) (Youtube Video) | [Starter Code](https://editor.p5js.org/cmorgantywls/sketches/THA0wYUcU)
* Video tutorial: [2.4 The map() function ](https://www.youtube.com/watch?v=nicMAoW6u1g\&vl=en)| [Code](https://github.com/CodingTrain/website/blob/master/Tutorials/P5JS/p5.js/02/2.4\_p5.js\_map/sketch.js)

### Assessments

Assess the Do Now assignment. Check for the ability to demonstrate the benefit of using an event, conditional or loop in their prototype.

Assess the learning activity. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Apply the map function to their program&#x20;
* Discuss what can be done with the map function

### Do Now/Warm-Up (5 minutes)

Change your canvas to 800x600.

In 5 minutes, create a program where the background will change as you move your mouse left and right across the screen. It should be black when you are on the left and white only when you get to the far right - in between it should be shades of grey going from dark → light.

### Vary the Background with mouseX (15 - 20 minutes)

Discuss the issues that come up during the Do Now with students - they should notice that it’s black less than halfway across the canvas, which is not what we want. Prompt students to think about why this might be, by considering possible mouseX values. You can also print the text or console.log the values to show students what’s happening.

Use this to launch the map function, which will be a new concept for many students. Share [this starter code ](https://editor.p5js.org/cmorgantywls/sketches/THA0wYUcU)with students, then code along mapping mouseX from 0 to the width of the canvas, and run the program so students can see the difference. Your finished code should look like this (all in the draw function):

```
var bgColor = map(mouseX, 0, 800, 0, 255) 
//you can declare the variable globally (above the setup function) if it helps student understanding

background(bgColor)
```

Challenge students to determine how map could be used to make it so the canvas goes from white (on the left) to black (on the right) - allow them to work on this with their partners for \~2-4 minutes. (They should realize they will need to swap the final mapped values.)

Share out student responses (and test code as needed).

Once students have completed this task, draw their attention to the rest of the starter code, which has a pink rectangle and a series of challenges. Remind them that they will need to create a mapped variable for each to make it run correctly.

After another example, give students 10 minutes to pair program or independently complete the final challenges as listed in the starter code.

### Return to Draw with Mouse (15 - 20 minutes)

Ask students to return to their drawing application and find ways they can integrate map while still drawing.

Again, either find time to share code or ask students to post their links for others to see.

### Wrap-Up (5 - 10 min)

If students post links in Google Classroom, ask students to go through and look at student projects and post comments on 3-4 of them. When posting links, you can also encourage students to post:

* Project Link&#x20;
* One thing you are really proud of&#x20;
* One struggle you had or are still having&#x20;
* Any questions or advice you would like to get.

### Extensions

Students can take each step as far as they would like, as this is solely based on exploration.
