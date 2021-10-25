---
description: How can logical operations make conditional more interactive?
---

# U2LA1.3 - Logical Operators And/Or

### Overview && Teacher Feedback

This learning activity builds on conditional statements using the Logical Operators && and ||. Students create a changing background color using a grid for guidance. They will use these concepts as they build a traffic light in the next project.

Students should have a solid understanding of conditionals and how it is satisfied through a boolean. This lesson will focus heavily on creating more complex algorithms through the use of conditionals. Therefore it is important that students add comments to keep track of the sketches control flow. Students will also benefit greatly from peer programming because they can model their thinking behind their code.

During the Do Now students will be introduced to logical operators. This can be confusing at first but with some examples and the logical operator chart it students can understand the use of &&, and ||. This do now may take a bit longer to complete but it will be very helpful when creating the buttons.

Have chart paper or use a whiteboard to visually draw the conditions needed for each section of the canvas.

Be sure to remind students often that most errors will stem from missing brackets { } or (). Have them review the console often to find their bugs.

The practice and play section is meant to be purposefully a bit challenging as well as to push student creativity - many students have a difficult time with which conditional is being executed based on the algorithm. Model how to test code whenever a new condition is written to help develop a student's best practice.

### Objectives

Students should be able to:

* Use if, else if and else statements in conjunction with &&, and ||&#x20;
* Create conditional statements (event handlers)&#x20;
* Elaborate on how to satisfy a condition.

### Suggested Duration

1 period (\~45 minutes)

### Blueprint Foundations Student Outcomes

**Abstraction**

* Describe different things I tried in order to achieve a goal.&#x20;
* Describe how I might use patterns to express an idea.&#x20;
* Explain characteristics or patterns that informed a function or an interface I created.

**Algorithms**

* Demonstrate the benefit of using an event, conditional or loop in my prototype.
* Compare and contrast how conditionals or loops were used in classmates’ prototypes.

**Programming**

* Discuss what can and cannot be done with a specific set of commands.&#x20;
* Describe the changes I made after testing at least three parts of my program.

### **Vocabularly**

* Conditional statements - a set of rules performed if a certain condition is met&#x20;
* Boolean expressions - a logical statement that is either TRUE or FALSE&#x20;
* && - AND - joins two statements to make sure they are both true before the whole statement is true
* || - OR - joins two statements so that if one is true, the whole statement is true

**Pre-Pre Vocabulary**

* Expression - is a group of terms (the terms are separated by + or − signs)&#x20;
* Relational operators - < , > , >=, <=, && (and), || (or)

### **Planning Notes**

|                                                                                                                                                      Planning Notes                                                                                                                                                     |                              Materials Needed                              |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------: |
| <p>Some of the examples might be too much from some students to copy so have some way students can access the links to your projects. </p><p>You’ll be using the p5 website A LOT - make sure everything linked in the lesson is unblocked and usable. </p><p>You can assign the video tutorial as H.W. or prework.</p> | <p>Pens/Pencils</p><p>Index Cards/Half Sheets for Exit Slip (optional)</p> |

### **Resources**

* [And/Or In Code ](https://youtu.be/8TGpiFZ5gsY)(Youtube Video) | [Starter Code ](https://editor.p5js.org/cmorgantywls/sketches/6Ta8mC-DJ)
* Video tutorial: [Else, and else if, AND and OR](https://www.youtube.com/watch?v=r2S7j54I68c)

### **Assessments**

Formative Assessment: Do now, Google form, Padlet\
Summative Assessment: Coding exercises, Guiding questions, code walkthrough

**Assess the learning activity. Check for the ability to:**

* Experiment with the commands of a programming language.&#x20;
* Demonstrate the benefits of using && and || in their code.

**Assess the wrap-up activity. Check for the ability to: **Describe the difference between && and || operators.

### Do Now/Warm-Up (5-10 minutes)

Ask students to look at both image 1 and image 2. They have to explain how Jose can eat ice cream with the given logical operator. Then explain the difference between both images.

![Image demonstrating the 'AND' operator](<../.gitbook/assets/Screen Shot 2021-10-25 at 10.03.50 AM.png>)

![Image demonstrating the 'OR' operator](<../.gitbook/assets/Screen Shot 2021-10-25 at 10.03.58 AM.png>)

Note: Creating a chart like the one below may help some students better understand logical operators. Use the images above and the chart in conjunction to explain &&, and or.

![Image showing tables of outcomes for values of a/b using and/or](<../.gitbook/assets/Screen Shot 2021-10-25 at 10.06.20 AM.png>)

Ask students:

* What is the difference between both images?&#x20;
* How is and, and or different?

If students still do not grasp this concept (or if you would just like them to have more practice), have them create their own conditions and explain it to a peer or the class.

### And/Or Lesson (20-30 minutes)

The “do now” should give students a solid understanding of AND, and OR. Inform students that they will be using this to make different and specific regions of their canvas cause reactions. This is the starter baby step for figuring out making rectangular ‘buttons,’ which some may solidify as they move into the traffic light project.

For this code along be sure to explain the purpose of each expression that is written between &&, and ||. This will model thinking behind using logical operators to create buttons. Refer to the chart to show how each condition can be satisfied. **This follows the youtube video on And/Or Code, if you need a reference.**

Ask students to [make a copy of this starter code](https://editor.p5js.org/cmorgantywls/sketches/6Ta8mC-DJ). Students will be writing conditionals to change the background color when the mouse is in each different quadrant; note that the entire background will be changing, and not each individual quadrant, which can be a sticking point for students. Begin by asking students to explore the canvas, specifically moving their mouse into each quadrant and reporting what they notice about the x and y values when they are in each area.

You will be coding along the bottom right quadrant because it is the furthest from where the mouse starts when students hit play. Ask students what they notice about values in this quadrant specifically - they should recognize that all x values are greater than 200, and all y values are also greater than 200 (the lines represent the exact centers of each axis). Together, create the following code (you will need to make the bgColor variable):

```
if(mouseX > 200 && mouseY > 200){
  bgColor = color(255,0,255)
}
```

From there, ask students to create else if conditionals for every other quadrant and an else statement to handle if the mouse is in the exact center of the screen. This can be a pair programming activity or done independently, based on the needs of your students. You can also have them complete work independently and then swap to read for comments/bugs/etc with a partner.

As students begin working, circulate to ensure:

* Commenting their code.&#x20;
* Using variables in the correct scope.&#x20;
* Using console.log() to debug and test&#x20;
* Saving their sketches with appropriate and clear titles.

### Wrap Up (5-10 min)

1. Students can submit code via a Google Form if you would like to collect it. If not, have students come back together for a discussion on what struggles they encountered in this activity.&#x20;
2. Students can also lead code-alongs or walk through their code with the class.

**Guiding Questions for Assessment:**

* What is the difference between the && and || operators?&#x20;
* What was challenging about creating a hover button? Why was it challenging?&#x20;
* What was easy**?**

### Extensions

Have students create 4 rectangles in each corner of the canvas that will change a feature of an ellipse in the center of the canvas when the mouse is on top of them:

* Color&#x20;
* Size&#x20;
* X position&#x20;
* Y position

[Possible Solution](http://editor.p5js.org/cs4all/sketches/r1FVPE0NX)
