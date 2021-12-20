---
description: How can arrays help us simplify code?
---

# U3LA.2.2: Arrays with floor() and random()

### Overview && Teacher Feedback

In this lesson, students will be introduced to the idea of randomly choosing elements from arrays. This lesson is also a soft launch into the next mini project!

Selecting a random element from an array is an important concept to know when working on this units final project. It would be a good idea for students to share out their solutions to the exercises so that you can clear up any misconceptions.

### Objectives

Students should be able to:

* Explain how the random() function serves to return a random number&#x20;
* Explain how the floor() function returns the input, rounded down&#x20;
* Use the combination of random() and floor() to select random elements from arrays

### Suggested Duration

45 minutes (\~1 class period)

### Blueprint Foundations Student Outcomes

**Abstraction**

* Give examples of specific patterns in something I can see, do or touch.

**Algorithms:**

* Explain why I used specific instructions to complete a task.&#x20;
* Compare and contrast my instructions with other instructions that complete the same task.

**Prototype**

* Experiment with the commands of a programming language.&#x20;
* Explain why I chose specific commands to communicate my instructions.

### Vocabulary

* Array - an ordered series of data&#x20;
* Index - a position within an array&#x20;
* Element - a piece of data in an array&#x20;
* **Zero-Indexed** - The first element of an array has an index of 0, not 1&#x20;
* **random()** - a function that will return a random number in between its two parameters

### Planning Notes

|                                                     Planning Notes                                                    |       Materials Needed       |
| :-------------------------------------------------------------------------------------------------------------------: | :--------------------------: |
| There are no specific planning notes for this lesson, but it is the first lesson students will be using media - whoo! | No special materials needed. |

### Resources

* [Choosing Random Values from an Array](https://youtu.be/ga6TCJdzy3k) (Youtube Video)
* [7.1 What is an Array?](https://www.youtube.com/watch?v=cnRD9o6odjk\&t=500s) | Code (6.1)&#x20;
* [Learning Processing:](http://learningprocessing.com/examples/) Chapter 9. Arrays&#x20;
* [Getting Started With p5.js:](https://p5js.org/books/) Chapter 4. Variables (Section: Repetition)

### Assessments

Assess the Do Now assignment. Check for the ability to:

* Create a program that pulls parameter values from an array to set location and color for multiple ellipses.

Assess the learning activity. Check for the ability to:

* Understand how to use the .length method in conjunction with console.log to print the total number of elements in an array.&#x20;
* Use the random() and floor() function to pull random elements from an array.

Assess the Wrap Up assignment. Check for the ability to:

* Describe how the random and floor functions work with arrays.

### Do Now/Warm Up (5-8 min)

Open a blank editor and using whatever color-choosing application you like, create an array of at least 10 different colors. (If you have time, continue adding colors.)

_Students should use their work from the previous lesson as reference - as they begin this warm-up activity, circulate to ensure that you can help them troubleshoot any errors as they get used to both arrays and storing this particular data type in arrays._

### random() & floor() functions

Explain to students that today, they are going to build a program with shapes that change color randomly whenever the program is run. This should feel familiar - they've done it before - but they've never done it by pulling random values from the array. And since that can be a little tricky, that will be the focus!

random() was introduced way back in Unit 1 (and likely used in Unit 2), so this should be familiar to students. If you think it's needed, feel free to take some time and review the following:

* random() is a different sort of function than something like ellipse() - it does something called _returning a value_ rather than making something happen on the screen, like an ellipse does
* It returns a random value based on a maximum (like random(100), which would be any number between 0-100) or a range (like random(5,50) which would be any number between 5-50).
* We can use this anywhere we would use a number, or even call it to stash our random value in a variable, as has been our best practice.
* The value will be randomized each time the random() function is called.

Ask students to put a shape somewhere on their canvas and explain we will be giving this shape a random fill from our array.

The first attempt might look something like this, and will certainly end in an error:

```
var palette1;
var randomColor;

function setup(){
 createCanvas(400,400)
 
 palette1 = [color(252,214,202), color(217,138,124), 
 color(240,101,89), color(219,117,116), color(255,28,82)]
 
 randomColor = random(5) //5 is the length of the array
}

function draw(){
  background(220)
  
  fill(pallete1[randomColor])
  ellipse(200,200,100)
}
```

So, why did this end in an error? Well, if we comment out the fill line and add this in the setup after line 10:

```
console.log(randomNumber)
```

We should see that we are getting random numbers, but they are not random numbers that exist in our array. Things like 3.1415903 aren't values that are in our array - so we need to make sure that our program is rounding down to the nearest whole integer.

Why round down? Our ellipse goes 0 - 4 even though there are 5 items - if we rounded up (as you can with the p5 function int()), we would need to make some adjustments later. Which is fine, just a choice that can be made!

Show students this adjustment that can be made to the code:

```
var palette1;
var randomColor;

function setup(){
 createCanvas(400,400)
 
 palette1 = [color(252,214,202), color(217,138,124), 
 color(240,101,89), color(219,117,116), color(255,28,82)]
 
 randomColor = floor(random(5)) 
 //floor takes the random value and rounds it down
 //5 is the length of the array
 
 console.log(randomColor)
}

function draw(){
  background(220)
  
  fill(pallete1[randomColor])
  ellipse(200,200,100)
}
```

We should now not only see numbers being logged that are within our array, but we should also be able to get an ellipse with a random fill and no error messages. Hoorah!

There's just one more thing we need to fix before we go off to play with this idea. Notice how right now, we are taking saying random(5) because the array is 5 items long? That could become a problem later if I were to add colors but forget to update this piece of code. Or what if I was making a program where users could add their favorite colors and the program would draw with them? &#x20;

Right now, the 5 **** in our random function is what we call a **hardcoded value.** Things that are **hardcoded** will always be the same in a program - and there are plenty of things we would want to be hardcoded, such as the score of a game starting at 0, or the timer for a soccer match half starting at 45, for example. But in this instance, we want to make sure that the value in random is **dynamic** so that if we make changes to our ray, the rest of our program is taken care of.

Remember that **.length** property we learned about in the last lesson? This is where it can come into play, like so:

```
randomNumber = floor(random(pallete1.length))
```

By changing the value to the length of the list, we will ensure that even if our lists gets longer (or shorter), the code will always work correctly. This kind of thinking is a best practice as we continue to make our programs more and more complicated. Always be asking yourself: what can I do to make sure this won't break in the future?

### Student Practice

Ask students to create a design where at least 5 shapes change randomly using colors from the array. _All_ shapes in their design should pull colors from the array, to practice calling array elements again, but they do not all need to be randomized.

### Wrap Up

Ask students to post their project links in a forum such as Slack or the Google Classroom. Then, have them view and comment on two other projects, leaving a glow and grow for each

Guiding questions:

* How can we use the random function to select a random element in the array?&#x20;
* What would happen if we did not use the floor function?

### Extensions

There are several ways that students can push their understanding of arrays:

* Ask students to create a button that will 'reroll' the randomly chosen colors.
* Have students create an array to hold the random values they generate. They can explore using [.push() ](https://www.w3schools.com/jsref/jsref\_push.asp)to add values to an array, and then call the values of that array for each shape. (This won't be as neat as it could be, yet, since they have not yet explored for loops and arrays.)
* Which goes to say - could they create a for loop to work through some of the array stuff? Advanced exploration!
* Learn about the [createColorPicker()](https://p5js.org/reference/#/p5/createColorPicker) function and use that to .push() values to the palette array. (.value will allow them to access the actual color selected by the picker.)
