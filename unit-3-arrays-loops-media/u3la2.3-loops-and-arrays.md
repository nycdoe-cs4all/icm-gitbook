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

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.7** Design or remix a program that utilizes a data structure to maintain changes to related pieces of data.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

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
* [Property Accessor ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property\_accessors)- provide access to an object's properties by using the dot notation or the bracket notation.
* [Variable Scope](https://www.w3schools.com/js/js\_scope.asp) - the places within a program where variables can be accessed. Scope can either be global (available through the entire program) or local (available only in a specific function).

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

### **Looping with Arrays (\~5 - 10 minutes)**

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

Walkthrough this loop with your students once you hit play, focusing on what is happening in each loop. The first time it runs, the fill is going to be whatever color is in index 0 of the array - then index 1 for the next ellipse, etc. The ellipses themselves should form a row 50 units apart, because you are multiplying each i value by 0. (First 0\*50, then 1\*50, then 2\*50, etc). The y and sizes stay the same. If needed, adjust values with kids to demonstrate what all the numbers are controlling!

You may also need to spend some time explaining < **yourArray.length.** This is making sure that we make it through the entire array, getting to every value, without going past the end of the list.

Now, what students should see is they were once again able to go from a lot of lines of code down to 4 - and that's pretty cool. But we still have some repetition here in sizes - and what if we wanted them to be different sizes? Or what if we wanted them to not be in a row, but be in positions all over the screen?

### **Objects in Arrays (\~10 - 15 minutes)**

Back in Unit 2, we discussed that **object literals** can hold lots of properties to keep us from repeating ourselves with many different variables. That's still true - and we can even put object literals _inside_ of arrays so that we can loop through and access many properties from a single array!

Let's explore that now. We are going to imagine that each object will represent one ellipse. For now, let's give each a color, a y value, and a width and height. We will code one and a half together and then y'all will add another 5 objects to your array!

```
newArray = [
 {theColor: color(255,255,0), y:200, w: 50, h: 10}, 
 {theColor: color(0,0,255), y:100, w: 50, h: 50}
]
```

**NB:** Notice that we have spread this array to make it easier to read. The square brackets are on different lines as are each object, but they are still separated by commas, as all elements in an array always are, regardless of type.

Following the conventions we set, ask students to add their next five objects to the array, then show them how they would use this new array in the for loop they had in their draw function, like so:

```
for(i = 0; i < newArray.length; i++){
  fill(newArray[i].theColor)
  ellipse(i*50, newArray[i].y, newArray[i].w, newArray[i].h)
}
```

Here, we access the object from the array by using the index value of the object in the array. (That's the newArray\[i] part, which we have seen before!) Now that will get us information about the ENTIRE OBJECT - you can console.log() the information if you want to see it live - but that won't work to plug into our p5 functions, we need the specific values. So as we've seen before with objects, we call them with the .property notation. So saying: newArray\[i].theColor, would access the value for theColor for the object in index position i. Pretty cool, right?

Now, this allowed us to store a lot of information and loop through a lot of information, but right now our output always looks pretty much the same. And that's fine - but what if I wanted it to be different each time my program was run? What if I wanted to use some random values here? You might be tempted to try changing some of the objects to something like this:

```
newArray = [
 {theColor: color(random(255),255,0), y:random(height), w: 50, h: random(10,20)}, 
 {theColor: color(0,0,255), y:100, w: 50, h: 50}
]
```

What you'll notice is that while this does get random values, they're doing the flashy thing all over the screen, which isn't always what we want. But if we put the for loop in the setup function (so it only runs once), we will have to move the background, and there is just potential for it to be a whole big thing.

So: how can we make sure that we are able to make objects with random values that maintain those random values?

### Generating with Loops (\~15 minutes)

The answer is that we need to use a loop to make our objects and populate them into the list before we ever draw with them - and good news is, that's easier than it sounds!

First, we are going to start off with an empty list at the top of our program, before the setup or draw function. (This makes it a GLOBAL variable, which means we can access it in both setup and draw.) Like so:

```
anotherArray = []
```

When we set up an empty list like this, it tells the program that anotherArray is in fact an array and can do array things - and it basically primes it to be set up like a shopping list. In our mind, let's imagine a long, blank list - there are lots of lines, maybe some check boxes, but nothing written. That's exactly what this empty array looks like - it's empty and waiting to have things added! So let's add them in setup, using a for loop:

```
anotherArray = []

function setup(){
  createCanvas(400,400)
  
  for(i = 0; i < 10; i++){
    anotherArray[i] = {theColor: color(random(255),255,0), y:random(height), w: 50, h: random(10,20)}
  }
}
```

Now, here's what we should be asking (and as a teacher, you should pose these to students first before clarifying):

* **What exactly is happening on line 6?** Well, we made a for loop. It starts at 0, and it is going to run until is 10 or higher, and each time it will increase i by one. Because this loop is adding an object to our array, this means it will add 10 objects to that array. (If you change this number, you can get more/less objects - try it!)
* **What about the whole thing with line 7?** So glad you asked - remember how our array is empty? This line is saying that at an empty index value - whichever empty index value i has landed us on in that moment - take it from being empty to set the element of that index value to be this object.
* **Aren't all our objects the same?** Not at all! See how we used random in several places in that object? (And you could of course alter how/where the randomness is being used, as you see fit.) It's going to 'reroll' those random values each time, creating new, unique objects.
* **What if I don't trust this process?** Pop a console.log(anotherArray) at the end of your setup function, after the for loop, and let's see what we get once the for loop has run. It should be an array of objects - demonstrate how you can click through the arrow levels to display the different objects - each with their own random values for different properties. And if we run the program again, we will get NEW random objects in our array!

So, how would you use this? Great question - if you go back to your draw function, you would make a for loop very much like what you had before, just using this new, randomly generated array. It will then draw each ellipse on the screen with properties from the objects, and those objects will change without you ever having to lift a finger.

### Mini Practice (\~10 minutes)

Randomly generate another array of objects that include properties for rectangles, and then draw the rectangles on the screen.

**NB:** _Students will get more practice with this in the next mini project, which is really just an extended practice for this activity. As students gain more and more skills, the mini-projects become more abundant because their confidence level means the practice does not need to be as prescriptive!_

### Wrap Up

Ask students to post their project links in a forum such as Slack or the Google Classroom. Then, have them view and comment on two other projects, leaving a glow and grow for each&#x20;

Guiding questions:&#x20;

* Explain how loops and arrays together can make our code more efficient.
* How do you populate an array with random values? Why is this useful?

### Extensions

Students can absolutely use this skill to go back and redesign their wallpaper if they are looking for a creative challenge.

For students looking for a concept challenge, have them look into vectors in the p5 library, as they will be useful in the next mini project.
