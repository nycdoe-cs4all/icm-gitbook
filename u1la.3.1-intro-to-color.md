---
description: How do computers mix colors?
---

# U1LA.3.1 Intro to Color

### Overview && Teacher Feedback

In this learning activity students add color to any of their previous designs. They learn to apply the background(), fill(), and stroke() functions (used in scales of gray until now), to define colors and add transparency. The RGB (Red, green, blue) color model is applied.

Students apply the programming concepts they learned in the previous unit (variables, randomness) to color manipulation, defining color ranges and palettes.

The first part of this lesson encourages students to think critically about color mixing and the differences between subtractive mixing (which they probably have some familiarity with) and the additive mixing done on computer screens. Giving students this background requires a full period before they get to computer practice; if you are short on time or have students with a strong arts background who you do not think will benefit from this exploration, you can abbreviate the introduction in order to get to computers more quickly.

In the “Do Now”, you can provide students with a worksheet if making a grid will be too time consuming.

Students will not use computers for the first half of this activity. You are looking for them to recreate something similar to this:

![Image of three circles overlapping in a triangular shape.](<.gitbook/assets/Screen Shot 2021-10-18 at 10.14.13 AM (1).png>)

Anticipate that many students may struggle with the idea of opacity/transparency. Anticipated responses include ‘brightness,’ ‘shade,’ ‘tone,’ etc. These are great return points for when you introduce HSB color mode.

There are many wonderful examples of color theory at work in our world. A useful one to for this topic is Olafur Eliasson’s A Room for One Color, in which the artist uses additive mixing to make every object in the room appear a uniform grey.

![This image is not edited in any way! This is from the phenomenology art movement for anyone with curious students](<.gitbook/assets/Screen Shot 2021-10-18 at 10.15.08 AM.png>)

If you have students who are struggling with fill() and the drawing order, you may want to act out the code with a colored marker.

Ex. A student says “make stroke red” you pick up a red marker, draw a circle when told, and do not put down the red marker. Students should realize they need a cue to tell you to switch to another color. This is also a great time to review that code runs from the top down - many students will try to add the fill after the shape.

### Objectives

Students should be able to:

* Describe the process by which computers mix colors (additive mixing)
* Use fill() to change the color of shapes in RGB color mode.

### Suggested Duration

1-2 Periods (45 minutes each)

### Blueprint Foundational Student Outcomes

Abstraction:

* Describe how I might use patterns to express an idea.&#x20;
* Explain why using patterns is necessary when creating with a computer.

Algorithms:

* Describe more than one set of instructions that might complete a task.
* Describe how instructions can have different outputs depending on inputs.&#x20;
* Explain why I used specific instructions to complete a task.

Programming:

* Experiment with the commands of a programming language.&#x20;
* Explain why I chose specific commands to communicate my instructions.
* Discuss what can and cannot be done with a specific set of commands.

### Vocabulary

* fill() function - Sets the color used to fill shapes.This color is either specified in terms of the RGB or HSB color depending on the current colorMode()&#x20;
* Subtractive Mixing - the mixing you are used to seeing with paint - paint tints absorb different lights from around them to create the visual color you see.&#x20;
* Additive Mixing - mixing done with light - adding lights to create the different colors you see.&#x20;
* RGB - Red, Green, Blue color mode, the default in p5.js&#x20;
* Opacity/Transparency - how see-through or not a shape is. Make sure students understand opaque to be solid and transparent to be closer to clear.

### Planning Notes

|                                                                                                                                                                                       Planning Notes                                                                                                                                                                                       |                                                                                                                                                                                                                                                               Materials Needed                                                                                                                                                                                                                                                              |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <p>The optional unplugged provides a deeper understanding of color mixing and the difference between mixing colors with art media vs. with light. It could be greatly abbreviated for time, or if you have students with a strong visual arts background. </p><p></p><p>Be aware of places in the lesson where students are required to make predictions - don’t give away the answer!</p> | <p>For optional launch: paint, colored pencils, construction paper, colored transparencies (like <a href="https://www.amazon.com/12-Pack-Overlays-Transparency-Correction/dp/B0759MGNH7/ref=sr_1_3?ie=UTF8&#x26;qid=1531354411&#x26;sr=8-3&#x26;keywords=colored+transparencies&#x26;dpID=41LY-BeWE4L&#x26;preST=_SY300_QL70_&#x26;dpSrc=srch">these</a> - transparent folders work as well!) and any other media you can think of. </p><p>Additive Mixing Sample Code </p><p>fill() practice code </p><p>Student note taking materials</p> |

### Resources

* Additive Mixing [Sample Code ](https://editor.p5js.org/cs4all/sketches/H1y6f957X)
* fill([) Practice Code - RGB Color Mode ](https://editor.p5js.org/cs4all/sketches/SJjuB99Xm)
* [Working with Color](https://youtu.be/3aHWKQCqP-M) (Youtube Video)

### Assessments

**Formative Assessment:** Student Share-Out, Fill() Practice Code, Optional Exit Slip&#x20;

**Summative Assessment:** End of Unit Project (Abstract Album Art)

### Do Now/Warm Up (5 min)

Ask students to draw a p5.js grid in their notebook (or on the paper provided) that makes a 300x300 canvas (count by 10’s!). Then, draw the following:

```
ellipse(100, 100, 100, 100);
ellipse(170, 100, 100, 100);
ellipse(145, 150, 100, 100);
```

You can provide students with a worksheet if making a grid will be too time consuming.

You are looking for this (-ish):

![](<.gitbook/assets/Screen Shot 2021-10-18 at 10.14.13 AM.png>)

After brainstarter, have students partner check (high-five their partner if they both have matching answers!) to see if they are correct.

Prompt students through a similar thinking to Unit 1, Lesson 1 - where did you get the X position from? Y position? Radius? Etc.

### RGB Color Intro and fill()

Introduce fill as accepting 3+ arguments and the idea of RGB.

![](<.gitbook/assets/Screen Shot 2021-10-18 at 10.32.01 AM.png>)

**Ask Students:**

* What do you think the R, G, and B stand for in this color system?&#x20;
* Most students will get to red, blue, green pretty instantly. Based on where the 255 is, what color might this make?&#x20;
* What if the 255 was somewhere else?

Once students are more comfortable, introduce the 4th and final (optional) argument for fill:

![](<.gitbook/assets/Screen Shot 2021-10-18 at 10.33.17 AM.png>)

Be prepared to explain opacity - students may need visual examples, and having transparent overlays in different colors is very helpful for this.

Anticipate that many students may struggle with the idea of opacity/transparency. Their responses might include ‘brightness,’ ‘shade,’ ‘tone,’ etc. These are great return points for when you introduce HSB color mode.

Once RGB has been introduced, ask students to type their code from the “do now” into the web editor and update it with what they learned about fill(). They should add a fill() function for each individual ellipse, like so:

```
fill(255, 0, 0);
ellipse(100, 100, 100, 100);

fill(0, 255, 0);
ellipse(170, 100, 100, 100);

fill(0, 0, 255);
ellipse(145, 150, 100, 100);
```

After students add the new lines of code to their sketch, ask them the following questions centered around analyzing code and making prediction:

1. What is a fill(0)? fill(255)? fill(100)?&#x20;
2. What do you think the R, G, and B stand for in this color system?&#x20;
3. For each fill function, based on where the 255 is, what color might this make? What if the 255 was somewhere else?

### Optional Unplugged: RGB Color, Additive vs. Subtractive Mixing

In this optional exercise we’ll explore the 4th argument (opacity), make predictions and understand the basics of color mixing.

Students should predict what would happen if one were to add opacity to each fill function. How would this affect the colors on screen? Does drawing order matter when you’re using opacity? To assist students in making predictions, allow them time to play with traditional media to add fill to the drawing they created during the “do now”.

Provide them with paint or other media to assist - you may have them all use the same media, or have different groups work in different mediums. This is an optional step - if students do not have access to this media, you can rely on prior knowledge and ask them to make predictions as if they had paint, etc.

```
fill(255, 0, 0, ?);
ellipse(100, 100, 100, 100);

fill(0, 255, 0, ?);
ellipse(170, 100, 100, 100);

fill(0, 0, 255, ?);
ellipse(145, 150, 100, 100);

```

You may have all students use paint (you’ll need red, green, and blue), or you can split students into groups and have each group use a different media. For example, one group might paint, another might use colored pencils, another might use construction paper - giving you a great chance to re-explain opacity.

At the end of the activity, ask students if the results matched their prediction. Then, ask them if they expect the computer program to behave the same way. Many students will mention the computer might make it look better, or make colors look crisper.

Present and run the [introToColor project,](https://editor.p5js.org/cs4all/sketches/H1y6f957X) and then ask students to discuss with their partner.

1. What did you expect to happen? Did it happen?&#x20;
2. What might have caused the difference?

After allowing time for discussion, introduce the following ideas:

* **Additive Mixing**: Mixing with lights, such as on a computer, adds colors to create what you see.&#x20;
* **Subtractive Mixing**: mixing with paints or other media suck up the light around it, creating what you see.

### RGB Color - Student Practice

To allow student practice, share with them[ the following sample code](https://editor.p5js.org/cs4all/sketches/SJjuB99Xm). Students will pair-program to create a colorful design. Assign a driver and navigator to begin the exploration.

First, ask students to set a fill() and stroke() before the first ellipse with their partner (each should be a different color). Then, ask what happened and why they think that took place. Students should notice that all circles now have this fill and stroke color.

Instruct students that they need to figure out how to make all ellipses have a different fill and stroke color. After completing the first five, the driver and navigator will switch.

Be sure to circulate and confirm that drivers are directing navigators. The navigators should not be working on their own!

### Wrap Up

If you’d like, you can collect student code and names of both partners through a Google Form or similar. You may want to include the following questions, or ask them to ask some of them as an exit slip if you aren’t interested in code collection:

* What does RGB stand for?&#x20;
* How does mixing on a computer differ from mixing with paints?&#x20;
* A student wants only the second color in their project to be red, but with this code, everything is red! Why? (Show sample code that would make this situation true)&#x20;
* A student successfully changes the color of their shapes, but their stroke is still black. What would they need to do to fix it? (Show code that matches this situation, with no stroke() call to change the color of the stroke.)&#x20;
* What do you enjoy about working with color so far? What is frustrating about RGB colors?

### Extension

Ask students to try to create a ROYGBIV rainbow with stroke and fill in different shades. Students should struggle greatly trying to mix additively.

