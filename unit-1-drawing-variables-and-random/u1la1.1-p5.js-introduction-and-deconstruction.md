---
description: How can we break down a robot into basic shapes in p5.js?
---

# U1LA1.1 p5.js Introduction & Deconstruction

### Teacher Feedback and Overview

This lesson is an unplugged activity that has students drawing a robot using shapes and that they will then use abstraction to code in the alpha editor. It is a great way to introduce p5.js before coding.

In this lesson, students will be introduced to the p5.js canvas and coordinate system. It is one of the most important concepts that students will need to master in order to be successful when coding in p5.js. This lesson is an unplugged activity in which students will draw a robot using shapes and then use abstraction decompose and code in the alpha editor. It is a great way to introduce p5.js before coding. Students will practice abstraction (definition below) when they are decomposing the robots shapes. Abstraction is an important CS practice that is used to reduce complexity and increase efficiency.

### Objectives

Students should be able to...

* Create an account on [https://editor.p5js.org/signup](https://editor.p5js.org/signup)
* Explain what p5.js is
* Describe things you can create on p5.js
* Understand the p5 canvas coordinate system

### Suggested Duration

1 Period \~45 Minutes

### Blueprint Foundational Student Outcomes

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p><strong>Abstraction:</strong><br></p><ul><li><strong>Give examples of specific patterns in something I can see, do or touch.</strong></li><li><strong>Describe different things I tried in order to achieve a goal.</strong></li><li><strong>Explain how I might help others identify patterns.</strong></li></ul><p><strong>Algorithms:</strong><br></p><ul><li><strong>Explain why I used specific instructions to complete a task.</strong></li><li><strong>Compare and contrast my instructions with other instructions that complete the same task.</strong></li></ul> |

### **Vocabulary**

* **Computational Media** - The practice of using programming to build expressive and interactive computer applications and media.
* **p5.js** - An open-source Javascript library that allows people to make web pages animated and interactive.
* **IDE** - Integrated development area is a software application that provides a place for computer programmers to develop code.
* **Unplugged Activity** - an activity that can be conducted without the use of computers or electronic equipment.
* **Abstraction** - Abstraction is the process of taking away or removing characteristics from something in order to reduce it to a set of essential characteristics

**Pre-Req Vocab:**

* **Width** - Horizontal distance of a 2D shape
* **Height** - Vertical distance of a 2D shape
* **Radius** - distance from the center to edge of a circle
* **Diameter** - distance from edge to edge of a circle passing through the center point
* **Cartesian (Coordinate) Plane** - four quadrant grid with an x & y axis, origin, etc.

### Planning Notes

| Planning Notes                                                                                                                                                                                                                                                                                                                                                         | Materials                                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <ul><li>This example is based off of the robot worksheet and example. If you or your class hate robots, plan on making a secondary example.</li><li>Preview shape functions - be prepared to differentiate between radius &#x26; diameter.</li><li>You’ll be using the p5 website A LOT - make sure everything linked in the lesson is unblocked and usable.</li></ul> | <ul><li><a href="https://drive.google.com/file/d/1CFJLhiHEBTQPxqTaNxESPxpc7F0Yto4D/preview">Robot Worksheet Handout</a></li><li>Pens/Pencils</li><li>Rulers</li><li>Highlighters</li></ul> |

### Resources

* [Robot Worksheet](https://drive.google.com/file/d/1CFJLhiHEBTQPxqTaNxESPxpc7F0Yto4D/preview)
* [Intro to Editor && Hello Ellipse](https://youtu.be/5PLmJPPTr88) (Youtube Video)
* (Optional) [Desmos p5 Coordinate Grid Activity](https://teacher.desmos.com/activitybuilder/custom/5f73248eba4291305a86cf50)
* (Optional) [Desmos p5 Coordinate Grid Tool](https://www.desmos.com/calculator/o75y8av9jw)

### Assessments

**Formative**: Peer reflection, Exit Slip\
**Summative**: Students Share Out, Student Robot Worksheet Review

### Do Now/Warm Up (5 min)

Have your students sign up for a p5.js editor account here:

[http://editor.p5js.org/signup](http://alpha.editor.p5js.org/signup)

They can easily create with these options:

* Google account
* Github
* Email

**NB**: The editor is not a p5.js online tool to manage and collect student work. It is strictly an online IDE - students will need to submit their project links to you through a Learning Management System such as Google Classroom, or another method such as Google Forms or Airtable.

After they’re done signing up, ask them to close their laptops or turn around with their attention to you (if in a lab).

### Intro: What is p5.js? (10 min)

Start the lesson by explaining what is the main programming language of this course. After watching the video ask students the following suggested questions: [Video](http://hello.p5js.org)

Note: The video is interactive so move the mouse around when prompted to show students how interactive p5.js can be

1. What did you see in the video?
2. What things do you think you can make with p5?
3. How is it similar or different to other programming languages?

Show some final project student examples to give your classroom a sense of what is possible with p5.

* [\*\*Emoji \*\*](https://alpha.editor.p5js.org/SEP/sketches/HylwiSZXQ)
* [**Paint Tool**](https://alpha.editor.p5js.org/dcanizares/sketches/HklghoFlf)

### Unplugged Activity: Draw A Robot (10 - 15 minutes)

Distribute the Robot Worksheet to students and explain that p5.js works on a coordinate system - it’s just a little different than the one they are used to seeing. Ask students to identify what looks different from math class, and students should notice the origin (0,0) is in the top left corner.

Explain to students that they will be creating robots on their paper using only RECTANGLES and ELLIPSES (circles/ovals). Rectangles must follow the grid-lines and ellipses must have a clear center. Inform students that they will need to find information about their shapes once they are done drawing, so be sure to follow the rules.

During the first part:

* Distribute Robot Worksheets and ask students to draw their robot consisting of only rectangles and ellipses
* They can use as many or as few as they want, but should try to use both shape
* Let them draw! (Having colored drawing implements on hand can be very useful for this step)

**After the drawing**:

* Model how to deconstruct robot shapes and how to log information onto the worksheet - students need to know that the important information about an ellipse is the radius and center point, and important information about a rectangle are coordinates of the top left corner, the width, and the height. Demo as needed.
* Tell students to keep in mind the p5 coordinate system with the origin in the upper left corner.
* Ask students to work with their partners to complete the activity.
* Students will take turns “driving” (recording answers on their page based on their partner’s findings) and “navigating” (finding answers based on their partner’s drawing) until they have completed the worksheet. Students should swap after each question.

After they complete the activity, either collect the student worksheets or ask them to save it for the next lesson.

### Student Assessment Guiding Questions

Ask the following questions and collect answers as a class summary or check for understanding (you can complete on a post-it for quick collection or aloud for a discussion):

1. Share one new thing that you learned.
2. What was challenging? Why?
3. Which features would you like to add?

### Wrap Up (5 Min)

Watch the “wrap up” space for suggestions on how to end your class for the day. Sometimes it will be a summary, a share out, a data collection, and other times it might be a look ahead to future lessons. Today, no data is needed, end your class in a way that is meaningful to you.

Show students the drawing below:

![Sample Robot on p5.js Coordinate Plane](<../.gitbook/assets/Screen Shot 2021-09-30 at 3.29.22 PM.png>)

**Let's unpack this drawing together:**

* How many shapes can you identify?
* What is the location of the mouth of the robot?
* How big are the eyes?

### **Optional Implementation #1:**

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Ask 2-3 students (preferably that you have conferenced with) to share their answers to one of the three questions above.</strong><br></p><ul><li><strong>Student share outs are a powerful way to build community and promote student ownership of learning. One approach could be creating a “sharing calendar” where 1-2 students share daily on a rotation (once the whole class has gone, shares start over again).</strong></li></ul><p><strong>Try to call on students whether they have the right or wrong answer and prompt the class to coach students through errors - this can begin to build a culture of celebrating errors as learning moments. Shares work best if you make them a consistent part of your routine.</strong><br></p><ul><li><strong>Students should share struggles or strengths, and can either a) ask the class for help when sharing or b) share something helpful they learned with the class. Aim to be a teacher facilitator and allow the class to coach itself.</strong></li><li><strong>Be sure to conference with students the day they share, even if its a quick check-in, so they don’t feel that they are being put on the spot or punished.</strong></li></ul> |

### Optional Implementation #2:

If you are more interested in data collection and have other structures in place for culture building, consider having students answer the three questions on an index card or other half sheet of paper that you can easily collect/grade/return.

### Ex**tensions**

**For the Robot Itself:**\
Add a hat or another element to the robot:\\

1. Using rectangles and ellipses.
2. Find a partner and add one feature to their robot and have then them deconstruct the position and size of the new feature.

Have students take turns adding to their robot and identifying sizes/coordinates as needed. “Driver” adds shapes, “navigator” finds information, then switch.\
\
**For the lesson generally:**\
In this lesson or the future lessons, if you think your students need more 'at-bats' to familiarize themselves with the p5 coordinate system, consider taking an extra period to complete the Desmos activity linked under resources.

\\
