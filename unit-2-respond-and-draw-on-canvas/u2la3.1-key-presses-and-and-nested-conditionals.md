---
description: How can I use key presses to control elements of my program?
---

# U2LA3.1: Key Presses && Nested Conditionals

### Overview && Teacher Feedback

In this learning activity, students learn to incorporate keyboard interactions into their sketches, responding to key presses and drawing letters on the canvas. Students learn to wrap conditionals so that they can create many color options with key presses.

This is a great chance to challenge student creativity and have them consider what they can control in a program. Push that as far as you can!

A common misconception is that students will call keyIsPressed in multiple if statements; this will sometimes make their program messy. A better solution is to have one ‘parent’ conditional that checks for any key being pressed, with every subsequent specific key condition nested inside of it.

This pair programming experience is very open-ended - try to encourage students to talk together about features for their program, rather than each person deciding for the group when it is their turn to navigate.

Push students to think about the user experience in leaving their feedback: did they know which keys to press without reading the code? How could this be improved?

### Objectives

Students should be able to:

Integrate key presses to control aspects of their program

### Suggested Duration

1 Period (\~45 Minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.8** Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

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

* **Key press** - p5 can register the most recently pressed key and whether a key is currently pressed&#x20;
* **Event Handlers** - alter the normal flow of a program when an action such as a key press or mouse movement takes place.&#x20;
* **keyIsPressed** - The system variable keyIsPressed is true if a key is pressed and is false if not

### Planning Notes

|                                                                                                         Planning Notes                                                                                                        |           Materials Needed          |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------: |
| This lesson is fairly straightforward programmatically but is an excellent time to challenge your students to think about user experience, especially when dealing with button presses (which are not visible like a button). | No materials other than a computer! |

### Resources

* [Key Presses in p5.js ](https://youtu.be/U7LsNnJH7C4)(Youtube Video) | [Starter Code ](https://editor.p5js.org/cmorgantywls/sketches/ZP31L3Dx4)
* [Keycode Info ](https://keycode.info)
* [Getting started with p5 Example 5-15: Tap a Key](https://books.google.com/books?id=iP3GCgAAQBAJ\&pg=PT92\&lpg=PT92\&dq=keyispressed+p5.js\&source=bl\&ots=4tsPcbUqAm\&sig=As7TQTro1qdt6uqILJ67mM29Kps\&hl=en\&sa=X\&ved=0ahUKEwjZvcvY5YvUAhUG8IMKHVxxD5oQ6AEITzAH#v=onepage\&q=keyispressed%20p5.js\&f=false)

### Assessments

Assess the Do Now assignment. Check for the ability to identify changeable values of an ellipse.

Assess the learning activity. Check for the ability to:

* Experiment with the commands of a programming language.&#x20;
* Create a program that can have different outputs based on different key inputs
* Demonstrate the benefit of using nested conditionals in their program

Assess the Wrap Up assignment. Check for the ability to:

* Describe how instructions can have different outputs depending on inputs.&#x20;
* Describe the benefit of using a nested conditional.

### Do-Now/Warm Up (3-5 minutes)

Ask students to draw an ellipse in the center of their screen with a size of 50. Then, they should leave comments for as many aspects of this ellipse as possible that they may want to change.

### **Press A Specific Key**

Ask students to share out some things they may want to change - remind them that this list could be long, and making buttons for everything might not make sense. Some things can change with a key press.

Code along with students; suggest that you all change the size of the circle together. Take notes in code that you want the circle to get bigger when you press b and smaller when you press s. Be sure to demonstrate that because size will change, it needs a new variable to control it. **Explain that you will be changing many different attributes of this circle eventually, so even though you are just changing one thing for now, you are going to set up your code using an object, like so:**

```
var theCircle;

function setup(){
 createCanvas(400,400)

 theCircle = {
  size: 200
 }
}

function draw(){
 ellipse(200,200, theCircle.size, theCircle.size)
}
```

After the variable and base code has been set up, demonstrate using keyIsPressed in an if statement but do not specify a key yet. Ask students to press b - the circle should get larger. Then ask them to press s or any other key and ask what the problem is:

```
if(keyIsPressed){
 theCircle.size += 5 //alternately, theCircle.size = theCircle.size + 5
}
```

Students should notice that all keys currently cause the circle to grow. This is your cue to begin discussing nested if statements, specifically ones that will check if the key is the same as a specific letter. With your students, set up “b” and “s” and then ask them to play again and determine what is wrong.

```
if(keyIsPressed){
 if(key == 'b'){
  theCircle.size += 5 //alternately, theCircle.size = theCircle.size + 5
 }
 else if (key == 's'){
  theCircle.size -= 5 //alternately, theCircle.size = theCircle.size - 5
 }
}
```

Students should notice that after a point, the circle gets too small and the key values ‘swap.’ This is because numbers have become negative and the computer is trying to react. Still, with the whole group, demonstrate how you could use && operators to safeguard against the circle getting too small or too large.

```
if(keyIsPressed){
 if(key == 'b' && circSize < width){
  theCircle.size += 5 //alternately, theCircle.size = theCircle.size + 5
 }
 else if (key == 's' && circSize > 0){
  theCircle.size -= 5 //alternately, theCircle.size = theCircle.size - 5
 }
}
```

From there, send students to pair program. With their partners, they should decide on six additional features & keys to add to the program that will change the circle or any other element they’d like to add, swapping off driver and navigator as they add each one.

**OPTIONAL BUT ENCOURAGED**: Much like with mouseIsPressed/mousePressed, there is a keyPressed callback function that students may choose to explore along with other keyboard based events in the p5 reference sheet. Depending on your students’ comfort levels, you may choose to review this with them, leave it as a general statement, or ignore it entirely.

### keyCode

Students may want to use keys outside of letters, which is possible but works a bit differently. Instead of saying ‘if (key===) ‘, they can say ‘if (keyCode ===) ‘ and use this website to identify keycodes: [http://keycode.info/](http://keycode.info)

For more information on where key codes come from, students can look into the Unicode system, which will be useful in AP CSP. [https://en.wikipedia.org/wiki/Unicode](https://en.wikipedia.org/wiki/Unicode)

### Wrap Up

Ask students to post their project links in a forum such as Slack or the Google Classroom. Then, have them view and comment on two other projects, leaving a glow and grow for each

**Guiding questions:**

* How does wrapping conditionals help our drawing app?&#x20;
* Which function would you use to change the size of the text?&#x20;
* What was challenging about wrapping one conditional inside another?

### **Extensions**

Give students specific and logically challenging tasks for their key presses, such as:

* Make your circle change color, but only to shades of yellow.&#x20;
* Make the stroke change color but never be the same as the circle color.&#x20;
* Make the strokeWidth change, but ensure that it will never be the same thickness as the circleSize.
