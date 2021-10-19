---
description: How can we use shape functions to create images?
---

# U1LA1.4 Various Shapes, Stroke, Weight, Fill

### Overview && Teacher Feedback

In this learning activity, students will explore the various p5 shape-drawing functions as pairs or in groups. The second focus of the lesson will be building research and collaboration skills so that students can have a successful time when programming in p5.js. Then they will continue to build on their understanding of functions and their parameters to recreate the robot from lesson 1.

* This lesson is an exploratory lesson meant to help empower students with the ability to troubleshoot problems when coding. They will be heavily using the p5 reference website, so make students are pair programming efficiently.
* The do-now offers great discussion questions around problem solving and collaboration.
* Some students will struggle with researching on their own so it is important to tell them that a programmer is not able to remember every function but should be able to read and use them.

### Objectives

Students should be able to:

* Consult the p5 reference for documentations
* Create triangles
* Create quadrilaterals
* Create arcs
* Create shapes defined by its vertices
* Use layering to create images

### **Suggested Duration**

\~1 period, 45 minutes

### Blueprint Foundational Student Outcomes

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p><strong>Abstraction:</strong><br></p><ul><li>Give examples of specific patterns in something I can see, do or touch.</li><li>Describe different things I tried in order to achieve a goal.</li><li>Explain why I chose to include the specific components of my prototype over others.</li><li>Explain how I might help others identify patterns.</li><li>Explain why using patterns is necessary when creating with a computer.</li></ul><p><strong>Algorithms:</strong><br></p><ul><li>Describe more than one set of instructions that might complete a task.</li><li>Explain why I used specific instructions to complete a task.</li><li>Compare and contrast my instructions with other instructions that complete the same task.</li></ul><p><strong>Programming:</strong><br></p><ul><li>Experiment with the commands of a programming language.</li><li>Describe three ways a development environment helps me create a project.</li><li>Explain why I chose specific commands to communicate my instructions.</li><li>Describe the changes I made after testing at least three parts of my program.</li><li>Discuss what can and cannot be done with a specific set of commands.</li></ul> |

### Vocabulary

* \*\*Function - \*\*Functions are lines of code that perform specific tasks.
* \*\*Parameters - \*\*Parameters are the values inside of parenthesis following the name of the function.
* **triangle()**
* **quad()**
* **openShape()**
* **arc()**

**Pre-Req Vocab:**

* \*\*Vertices - \*\*a corner or a point where lines meet.
* \*\*Quadrilateral - \*\*A four sided polygon.
* \*\*Triangle - \*\*Three sided polygon

### Planning Notes

| Planning Notes                                                                                                                                                                                                                                                                                                           | Materials Needed                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| <ul><li>Pairing or grouping students who have difficulty with literacy or difficulty reading the p5 reference with students who can assist in completing the task.</li><li><p>Students will need 3 tabs open or</p><ul><li>Alpha Editor</li><li>Slide Decks (optional)</li><li>P5.js Reference Guide</li></ul></li></ul> | <ul><li>Computer or laptop</li><li>Pens/Pencils</li><li>Rulers</li><li>Highlighters</li></ul> |

### Resources

* Video Tutorial: [1.4: Color - p5.js](https://youtu.be/9mucjcrhFcM)
* [Basic shape guide](https://drive.google.com/file/d/0Byk7AxhPkTEJWWdUeVFteXFrT2M/view?usp=sharing)
* [Blank Student Shape Guide](https://docs.google.com/document/d/1H-H5XI5pqNcyGtJsySNG20reEn-qQQWKyGGvXNS8PAM/edit?usp=sharing)
* [Using the Reference Sheet](https://youtu.be/waPAw\_Ndbdk) (Youtube Video)
* [Styling Shapes](https://youtu.be/4FQjGC5oHOM) (Youtube Video w/ Starter Code Activity)

### Assessments

\*\*Formative: \*\*Guided questions, code alongs, peer examples\
\*\*Summative: \*\*Student Share Out, Blank Student Shape Guide

### Do Now/Warm Up (4 -8 min)

* \_Having an open discussion on these questions is a good way to gauge the temperature of the classroom. Students should know that a programmer does not know everything but they have them collaborate and research skills to find creative solutions. \_
* \_Creating a poster from students' feedback can help create a successful and safe risk -aking culture in your classroom. \_
* _Interesting Video on Tech Culture: _[_https://www.youtube.com/watch?v=QW834PGYnYI_](https://www.youtube.com/watch?v=QW834PGYnYI)

Ask Students:

1. What do you do when you are stuck or confused on a problem?
2. How do you think a software engineer solves a problem when they are stuck or confused?
3. How does risk-taking play a role in problem-solving? Give examples using our classroom?

Optional Questions:

1. How can we promote self-advocacy?
2. What are successful peer collaboration skills?
3. What would help you as a student to be able to search for solutions?

### Intro (5 Min)

Tell students that this activity will have them problem solving and researching with their peer. Ask students what they do when feeling stuck? This question will open up the discussion on how students go about solving problems.

Prompt students to think about these questions when they feel stuck. You can have them copy it from a slide deck or create a poster.

* Ask yourself:
  * What was supposed to happen?
  * What happened instead?
* If there is an error message look at the line number and error description. If the error message has a suggestion try that first.
* Check for common errors working line by line from top to bottom
* Play with the code. Make one change at a time then hit run.
* Use teamwork. Compare your code to the code of someone next to you.
* Check out the p5.js online reference. [www.p5js.org/reference](http://www.p5js.org/reference) Model how to navigate the reference guide and then how to read the arguments a function takes.
* Attach a sticky note to the back of your laptop. Let your peers or teachers know that you need extra help.

Model how to navigate the reference guide and then how to read the arguments a function takes.

![Screenshot of the p5.js Reference Sheet](https://lh5.googleusercontent.com/j71sDwY4pf5jKT7LbtaYY192Nh4BYBp8c6L0IYb9gzNNEVg860uVlR7HgDeGgz56dyGFfKvV4yc5kw1SwmxXn5an-rZ7gqX7Vv17n\_M6vgG\_AB7AjoWKpFcMEt-Wv7HQ7k9RcLb2=s0)

### Draw Other Shapes and Navigate the p5.js Reference Sheet (\~15 min)

Explain the definition of fill(), stroke() and noStroke() to students, and then [code along](http://alpha.editor.p5js.org/SEP/sketches/rk6LV23EQ) to explain the difference between the 3 functions. Ensure students are adding comments to their code.

In pairs or groups of 3 ask students to complete the following [worksheet](https://docs.google.com/document/d/1H-H5XI5pqNcyGtJsySNG20reEn-qQQWKyGGvXNS8PAM/edit?usp=sharing) by filling in the missing blanks and using the [p5 reference](http://www.p5js.org/reference) to research information on each shape. Model how to complete the worksheet with the students.\
Students can use the following lines of code at the bottom of draw() to help them create these shapes:

```
//To help you find the right point positions, use this line:
  fill(0); //set the fill color to black
  noStroke(); //set the stroke to none
  text(mouseX + ", " + mouseY, 20, 20);
  //We will explain how it works later on.
```

After they are done with the worksheet, ask them to create one or more of the following shapes in the p5.js:

* Triangle using triangle() function
* Quadrilateral using quad() function
* Star using beginShape() function
* An arc using the arc() function.

Their sketches should include:

* Sketch name that matches the unit and lesson number. Make this a standard practice in your classroom.
* A canvas size of 600 pixels wide by 120 pixels high.
* Light gray background.

Examples of possible outputs:

![Four shapes on grey background, a triangle, a star-esque polygon, a quadrilateral, and a small arc.](https://lh3.googleusercontent.com/dGqIUpfi5c82eila\_zca\_VOhNxfCdp89lzjUxZgX7eLjayW2\_mVi\_lVl5IyxZnRwRIteQhuJPx8T1kWFizHaF-YE08YOQ-Qh44YYNGYjh1LcA4kbdQmTLDYhtdBz8sQxXhdbE2h6=s0)

[**Possible Solution**](http://alpha.editor.p5js.org/SEP/sketches/Byc6nmFEX)\*\* | \*\*[**Possible Solution with stroke() and fill()**](http://alpha.editor.p5js.org/SEP/sketches/SkiIEh3Nm)

Students do not have to recreate these shapes exactly. Circulate the room to ensure students are adding comments to their code to label each shape.

For students choosing to create the star shape or their own polygon, remind them that they can use the beginShape() function, and then add as many vertices as needed. Add endShape(CLOSE) at the end to close the shape.

Example:

![Image of a continous line forming a house on a grey background](https://lh3.googleusercontent.com/OHZu7dvRlWatG3joa3Og6nWpEkyw2bAGBbsACBak2NbIXVzV9Os4AOGnTXnK\_5DxbnXVJ0Kejbk2PCmNBX-efcqKJ3yWtykQ-\_Si1lQoffrRM0VO26il2QLpeniJl66AgCZnI9fs=s0)

Ask students and partners to explain the parameter of one new shape function and how their image aligns with the parameters. Teacher will circulate and and help clear confusion. Students should use the content from the reference to explain their answers.

![](https://lh3.googleusercontent.com/sLUbC17GhqVlqiYdSo22IVELtEG75TdaQKqvbtSzUsH9x0QWxojo37YNM75k-j621YHMB087dF8vtgABiThqwKJ0Bg159Iw-O0O2lUjURp\_OKMuEkPP6vTFoQt4NVHmqzgPejbzt=s0)

### **Wrap Up**

Ask 2-3 students (preferably that you have conferenced with) to share their answers to one of the shapes above. Students should share their project link with teacher prior to answering and explaining how they created their shapes.

**Ask Students:**

* What are the benefits of displaying mouseX and mouseY on the canvas? How can it be used for future projects?
* What was challenging when drawing more complex shapes?
* What are the things important when drawing more complex shapes?

### **Extension**

If time allows, spend some time reviewing the arc function, angle measuring units, and how its parameters work using this [p5 reference cheat sheet](https://drive.google.com/file/d/0Byk7AxhPkTEJWWdUeVFteXFrT2M/view?usp=sharing) and have the students compare their results in their groups. Then have them create this arc using the cheat sheet.

![](https://lh5.googleusercontent.com/CffIEEI4ZmAL6XdROcZieVmN2EDyWB8PfTi0Q2i-lNVIR9dvWaskAFq1UrpnEJozwKNffITy39azMaReCdeqKs6x0qXqZLRu09tVWig-cW4jnavF3XDGqIMQKWl6cdFWiKJ1DS4B=s0)

\
\
\\
