---
description: How can arrays help us simplify code?
---

# U3LA2.3: Loops and Arrays

### Overview && Teacher Feedback

In this lesson, students will be introduced to the usage of loops to iterate through arrays. They will also explore how they can add items to an array using a loop, and practice placing objects into arrays.\
\
Iterating through an array is an important concept to know when working on this units final project. It would be a good idea for students to share out their solutions to the exercises so that you can clear up any misconceptions.

### Objectives

Students should be able to:

* Explain how a loop can be used to iterate through an array&#x20;
* Retrieve information from arrays using for loops
* Populate an array using a loop
* Utilize objects located within an array

### Suggested Duration

1-2 Periods (\~45-90 minutes)

### Blueprint Foundations Student Outcomes

**Abstraction**

* Give examples of specific patterns in something I can see, do or touch.&#x20;
* Describe different things I tried in order to achieve a goal.

**Algorithms**

* Explain why I used specific instructions to complete a task.&#x20;
* Compare and contrast my instructions with other instructions that complete the same task.&#x20;
* Demonstrate the benefit of using an event, conditional or loop in my prototype.

**Prototype**

* Experiment with the commands of a programming language.&#x20;
* Explain why I chose specific commands to communicate my instructions.

### **Vocabulary**

* Array - an ordered series of data&#x20;
* Index - a position within an array&#x20;
* Element - a piece of data in an array&#x20;
* Zero-Indexed - The first element of an array has an index of 0, not 1&#x20;
* For loop - loops through a block of code a number of times&#x20;
* Iterate - go through elements one by one

### **Planning Notes**

|                                                      Planning Notes                                                     |        Materials Needed        |
| :---------------------------------------------------------------------------------------------------------------------: | :----------------------------: |
| _There are no specific planning notes for this lesson, but it is the first lesson students will be using media - whoo!_ | _No special materials needed._ |

### **Resources**

* [7.2 Arrays and Loops](https://www.youtube.com/watch?v=RXWO3mFuW-I) | [Code](https://github.com/CodingRainbow/Rainbow-Code/tree/master/p5.js) (6.2)&#x20;
* [Learning Processing:](http://learningprocessing.com/examples/) Chapter 9. Arrays&#x20;
* [Getting Started With p5.js: ](https://p5js.org/books/)Chapter 4. Variables (Section: Repetition)

### **Assessments**

Assess the Do Now assignment. Check for the ability to:

* Create a program that pulls parameter values from an array to set location and color for multiple ellipses.

Assess the learning activity. Check for the ability to:

* Use for loops to iterate through the index of an array. Use for loops to iterate through the index of multiple arrays and pull values for different parameters.

Assess the Wrap Up assignment. Check for the ability to:

* Describe how iterating through an array works.

### **Do Now/Warm-Up (5 min)**

Ask students to create an array and fill it with 5 different colors. Then create 5 ellipses with fills using each element from all 5 indexes.

_Check to see if students can create and use arrays. Have students share their solutions with the class. Students should be able to call elements from an array._

### **Looping with Arrays**

Ask a student or two to share their solution - the first thing you'll want to check for is their array, making sure that they added elements correctly, and the second is their code. Ask students if they notice repetition - they should! They are repeating both the fill, with only the number of the element they are calling changing, as well as the ellipse itself.

Can we make this better? We certainly can! We want to repeat the same process with slight changes each time - aka an _iteration._ That calls for a for loop.

Ensure all students have a working array - for ease, you may want to norm what you all have named the array - and then code along the following for loop in the draw function:

```
for(i = 0; i < yourArray.length; i++){
  fill(yourArray[i])
  ellipse(i*50, 200, 50, 50)
}
```

**NB:** _If you haven't covered it yet, i++ is the same as saying i+=1, or i = i + 1. This is not essential knowledge if you think it will confuse your students, but it's sure short and easy to write!_

Walk through this loop with your students once you hit play, focusing on what is happening in each loop. The first time it runs, the fill is going to be whatever color is in index 0 of the array - then index 1 for the next ellipse, etc. The ellipses themselves should form a row 50 units apart, because you are multiplying each i value by 0. (First 0\*50, then 1\*50, then 2\*50, etc). The y and sizes stay the same. If needed, adjust values with kids to demonstrate what all the numbers are controlling!

You may also need to spend some time explaining < **yourArray.length.** This is making sure that we make it through the entire array, getting to every value, without going past the end of the list.

Now, what students should see is they were once again able to go from a lot of lines of code down to 4 - and that's pretty cool. But we still have some repetition here in sizes - and what if we wanted them to be different sizes? Or what if we wanted them to not be in a row, but be in positions all over the screen?

### **Objects in Arrays**

Back in Unit 2, we discussed that **object literals** can hold lots of properties to keep us from repeating ourselves with many different variables. That's still true - and we can even put object literals _inside_ of arrays so that we can loop through and access many properties from a single array!

Let's explore that now. We are going to imagine that each object will represent one ellipse. For now, let's give each a color, a y value, and a width and height. We will code one and a half together and then y'all will add another 5 objects to your array!

```
newArray = [
 {theColor: color(255,255,0), y:200, w: 50, h: 10}, 
 {theColor: color(0,0,255), y:100, w: 50, h: 50}
]
```

**NB:** Notice that we have spread this array to make it easier to read. The square brackets are on different lines as are each object, but they are still separated by commas, as all elements in an array always are, regardless of type.

### Generating Arrays with Loops

