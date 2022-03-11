---
description: How can I use cosine to create circular motion?
---

# U4LA3.2: Cosine & Circular Motion

### Overview && Teacher Feedback

In this learning activity we create cyclic motion: our ellipse oscillates up and down, moves on a circle, and finally on a spiral. To do this, we use trigonometry: sine and cosine values are calculated for an angle that grows with each frame, and mapped to the position of the ellipse.

This lesson is similar to the sine lesson and builds on what students learned there. While it requires the same level of understanding as to what cosine is as students should currently have of what sine is, it is more mathematically complex to understand why they need to use both sine and cosine to create circular motion.

This lesson, like many in this unit, is primarily conducted through student play and code commenting rather than full on teacher lecture. The main things to watch out for is that they understand that someone built this program from scratch - outside of the sin() and cos() functions, there is nothing magical or built-in about it, including the variables and their naming conventions.

This is also the last lesson before the final project, so it is an excellent time to work out any last kinks or questions.

### Objectives

Students will be able to:

* Use cosine and sine to create circular motion&#x20;
* Turn circular motion into a spiral shape&#x20;
* Understand that sine and cosine produce different values based on the ratios of angles they are finding

### Planning Notes

|                                                        Planning Notes                                                        |                                                                                                         Materials Needed                                                                                                         |
| :--------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Be sure to review things marked Teacher’s Notes in this lesson as they can help you hit key points in a complicated concept! | While there are no required materials, it may be handy to have access to a surface you can draw on such as a whiteboard or chart paper when explaining some concepts to students, or reviewing things such as the brain starter. |

### Suggested Duration

1 Period (\~45 minutes)

### Blueprint Foundations Student Outcomes

\[COMING SOON]

### Vocabulary

* **Cosine** - Another trig ratio - it also moves in a cycle between -1 and 1, but it moves slightly differently. We can use sine and cosine together to create interesting patterns of motion.&#x20;
* **cos()** - a function that calculates the cosine of an angle. It takes into account the current angleMode. Values are returned in the range -1 to 1.

### Resources

* [Circular Motion Exploration](https://editor.p5js.org/cmorgantywls/sketches/X42BnepRa) (Starter Code)
* [Sine && Cosine from CCFest LA](http://dexterjshepherd.com/ccfestla2018/#/5)
* [Ken Chung Sine && Cosine in p5](https://editor.p5js.org/kchung/sketches/SyTz42l87)
* [Cosine and Circular Motion](https://youtu.be/JrMeqBx8igs) (Youtube Video)

### Assessments

This is primarily an exploration of pre-written code and a chance for students to play by making it their own. Rather than collecting a finished product, consider collecting the pre-built code with student comments and using it to assess understanding instead.

### Do Now/Warm Up

In your notebooks, draw a quick coordinate plane. Then, draw a circle with a center on the origin. As you draw, consider: What is happening to the x and y values as I draw? What is the highest x value? The lowest x value? What is the highest y value? The lowest y value?

**NB:** _Everyone will most likely draw slightly different circles, but it’s fairly common for students to establish a circle center on the origin. With this example it is easy to see that the highest and lowest x values are opposite values - for example, the lowest x value might be -3 and the highest would be 3. The diagrams below show this relationship. It can be difficult for students to understand how the y and x change independently but simultaneously when moving in a circular direction, so it may help to utilize a white board/chart paper to draw this out together and isolate variables on specific axes._

_A big takeaway in this problem is that at each point, the y and x have different values and are changing at slightly different rates, but they are both oscillating between two opposite numbers, much the way sine oscillates between -1 and 1. In order to create circular movement, you cannot just use sine, as a sine for y and x would just make a motion with a rate of change of 1 that moves at a diagonal. If students struggle with this later, demo in p5._

![Graphs of circles on a coordinate plane explaining increasing/decreasing x/y values](<../.gitbook/assets/Screen Shot 2022-03-11 at 1.03.35 PM.png>)

### Cosine and Sine

**Cosine** is another trig ratio - it also moves in a cycle between -1 and 1, but it moves slightly differently. When sin() and cos() are used together, they can produce circular motion. The **cos()** values provide the x coordinates, and the sin() values provide the y coordinates.&#x20;

**cos()** calculates the cosine of an angle. This function takes into account the current angleMode. Values are returned in the range -1 to 1.

![Cosine graph](https://lh6.googleusercontent.com/zYQ7XsoaU6N5AS9AcNiNCBMHe1Wd01pVQIssdW2hayCufhqQPbzuYJBtecM-jR32BblRMgFTFDpE6OVGqHTmdltYuu--1KfUZy7BpjXBydR6ItSZb-mnn9HRX47v5GVKrGaR4NTU)

Cosine is similar, but different, to sine, as it is technically the ratio between the adjacent side and the hypotenuse of a right triangle given an angle. It is not important for students to fully understand this difference, but they should grasp - especially later in the lesson - that cosine and sine produce different values for given angles. This allows you to create circular motion and is best illustrated in the graph below:

![Graph displaying sine and cosine in different colors](https://lh6.googleusercontent.com/8pzmzhlvtquCMCuzsgVQmm-0qyJzwfo7r11mgJRoX88oI3v3jcnhMjAPotLtwn7EtERZYQSqglHNgZK3xOKqGhZnaxQRHYNIqOSXwolqY5hx-LHG46sgRY-pfCBGxnACJyMpFJj0)

If students struggle to understand why this is necessary, at the end of Exercise #1, consider trying to draw the circle using sine to control both the x and y position and take a look at what happens. (It should create movement in a straight but diagonal line, as an identical change in y over an identical change in x results in an overall change/slope of 1)

### Exercise: Exploring Circular Motion

Share students on [this starter code](https://editor.p5js.org/cmorgantywls/sketches/X42BnepRa) and ask them to duplicate.

```
var circ1 = {
  x:0,
  y:0,
  angle:0.0,
  offset:50,
  scalar:20,
  speed:3
}

function setup() {
  createCanvas(600, 420);
  background(204);
  angleMode(DEGREES)
}

function draw() {
  circ1.x = circ1.offset + cos(circ1.angle) * circ1.scalar
  circ1.y = circ1.offset + sin(circ1.angle) * circ1.scalar
  
  ellipse( circ1.x, circ1.y, 40, 40);
  circ1.angle += circ1.speed;
}
```

**Look at the example and do the following:**

1. Adjust the starting value of the variable offset. What does it control? What would be another good name for this variable? Leave a comment. Where is it used in the program?&#x20;
2. Adjust the starting value of the variable scalar. What does it control? What would be another good name for this variable? Leave a comment. Where is it used in the program?&#x20;
3. Adjust the other values as you see fit!&#x20;
4. Right now, the angle variable gets bigger each frame. Identify where this happens in the program.&#x20;
5. Make your canvas bigger and your ellipse smaller.&#x20;
6. Make the scalar variable also get bigger each frame. What happens when you run the program? What would happen if you made the offset variable get bigger each frame?

As in past explorations, this could be done as an independent or pair-programmed activity. The most important part is that students are able to work their way through these questions and leave quality comments in the code as they go! An optional assessment is to have students submit commented code and grade their answers based on the comments.

An important piece to look for here is the alternate variable names in questions 1a and 2a. Students sometimes think offset and scalar are magical words that always must be used, or worse, are built-in variables that they do not need to declare and debunking this early is a very useful practice. (You may want to check in and ensure they do not think this about angle and speed, as well!)

### **Exercise: Make a Spiral**

By making the scalar value grow with each frame, we can create a spiral:

```
var circ1 = {
  x:0,
  y:0,
  angle:0.0,
  offset:50,
  scalar:20,
  speed:3
}

function setup() {
  createCanvas(600, 420);
  background(204);
  angleMode(DEGREES)
}

function draw() {
  circ1.x = circ1.offset + cos(circ1.angle) * circ1.scalar
  circ1.y = circ1.offset + sin(circ1.angle) * circ1.scalar
  
  ellipse( circ1.x, circ1.y, 40, 40);
  circ1.angle += circ1.speed;
  circ1.scalar += circ1.speed;
}
```

Ask the students to do one or more of the following modifications to an existing sketch:

1. Make multiple circles and/or spirals at different places on your canvas?&#x20;
2. Use random to control a part of your design? (Size, position, the spiral itself, etc)&#x20;
3. Make a circle draw and move left/right or up/down across the screen by incrementing the variable for offset?&#x20;
4. Create a design (emoji or otherwise) and make it move in a circle or spiral?

Remind students that they can add a background if they don’t want to see the path of the circle.

### Wrap Up

Ask students to share their discoveries or creations with the class. Alternatively, you might have them post links and comment in Google Classroom, or collect their links via Google Form for teacher analysis.

### Extensions

At this point in the curriculum, students have access to a huge array of tools to help them create whatever they can imagine. Rather than providing general extensions, ask students to think back to their own work and where this could be integrated. Making the emoji project roll its eyes, perhaps?
