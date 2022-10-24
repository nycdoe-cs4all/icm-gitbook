---
description: How do the parameters of function effect positioning on the p5 canvas?
---

# U1LA1.2 Line Functions and Parameters

### Overview && Teacher Feedback

In this learning activity, students will create a visual composition using the p5 shape-drawing functions point() & line(). They will be introduced to functions, parameters, and then how to call them in p5.

Students should have already created an account and know how to login. If not, it would be good to model it before reviewing the editor. **The p5.js Editor is not like Google Classroom: it is strictly an online IDE for p5.js.**

This lesson will be the first time that many students will be coding along with the teacher; give students enough time to copy as they get accustomed to code-alongs. Giving students access to the slide deck will help with questions, sharing links and entry points for anyone who may have gotten off track or needs help.

### Objectives

Students should be able to:

* Understand the p5 canvas coordinate system
* Consult the p5 reference for documentation
* Create a line and point
* Change the grayscale value of a canvas
* Use lines to create a rectangle or a house

### Suggested Duration

\~1 period, 45 minutes

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Abstraction:</strong></p><ul><li>Give examples of specific patterns in something I can see, do or touch.</li><li>Describe different things I tried in order to achieve a goal.</li><li>Explain how I might help others identify patterns.</li></ul><p><strong>Algorithms:</strong></p><ul><li>Describe more than one set of instructions that might complete a task.</li><li>Explain why I used specific instructions to complete a task.</li><li>Compare and contrast my instructions with other instructions that complete the same task.</li></ul><p><strong>Programming:</strong></p><ul><li>Experiment with the commands of a programming language</li><li>Explain why I chose specific commands to communicate my instructions.</li><li>Discuss what can and cannot be done with a specific set of commands.</li></ul> |

### Vocabulary

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li><strong>IDE -</strong> Integrated development area or IDE is a software application that provides a place for computer programmers to develop code.</li><li><strong>function -</strong> Functions are lines of code that perform specific tasks.</li><li><strong>arguments -</strong> Are the values inside of parenthesis following the name of the function. These are used to change the outcome of a function</li></ul><p><strong>Pre-Req Vocab:</strong></p><ul><li><strong>width -</strong> Horizontal distance of a 2D shape</li><li><strong>height -</strong> Vertical distance of a 2D shape</li><li><strong>Cartesian (coordinate) plane -</strong> four-quadrant grid with an x &#x26;&#x26; y-axis, origin, etc.</li><li><strong>vertex -</strong> a point where two or more lines meet</li></ul> |

### Planning Notes

| Planning Notes                                                                                                                                                                                                                                                                                                                                                                                                                                    | Materials Needed                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| <ul><li>You’ll be using the p5 online IDE A LOT - make sure every code example linked in your modified lesson is updated and usable</li><li>Students should log-in to their account at the beginning of each class (build this as a routine in your classroom)</li><li><p>Students will need 3 tabs open for every lesson of this course</p><ul><li>p5 Editor or repl.it</li><li>Slide Decks (optional)</li><li>P5.js Reference Guide</li></ul></li></ul> | <ul><li>Computer or laptop</li><li>Pens/Pencils</li><li>Rulers</li></ul><p>Highlighters</p> |

### Resources

* [p5.js Reference Sheet](https://p5js.org/reference/)
* [Line Worksheet](https://docs.google.com/document/d/14mDvlCxeFW6elTAi1RMNdzJZv0ZZVKv3HXlK8hRfNOk/preview)
* [Basics of Drawing](https://youtu.be/D1ELEeIs0j8) (Youtube Video)
* (Optional) [Desmos Coordinate Grid Activity](https://teacher.desmos.com/activitybuilder/custom/5f73248eba4291305a86cf50)
* (Optional) [Desmos Coordinate Grid Tool](https://www.desmos.com/calculator/o75y8av9jw)

### Assessments

**Formative**: Grey Scale Practice, Line practice \
**Summative**: Students Share Out, Exit Slip, Student Robot Worksheet

### Do Now/Warm Up

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>This unplugged activity will help reinforce your student’s understanding of the p5.js coordinate plane. Students can work as groups, pairs or individually.<br></p><p><strong>Ask students to:</strong><br></p><ul><li>Take a <a href="https://docs.google.com/document/d/14mDvlCxeFW6elTAi1RMNdzJZv0ZZVKv3HXlK8hRfNOk/edit?usp=sharing">Line Worksheet</a></li><li>List the starting and ending points of each line using the p5 coordinate plane.</li><li>The first point is on the left and then the second is on the right.</li></ul><p><em><strong>Once students have finished the task, ask:</strong></em></p><ol><li>What would be different if these lines were to be drawn on a regular Cartesian plane?</li><li>What are the coordinates for lines 1 - 6?</li></ol> |

### Introduction (3 min)

Begin this lesson by having students think and list the difficulties of translating their paper drawings into “code”.

Show students the 3 final projects, or any other p5.js generated images for unit 1, and ask them what are some things they notice about these images. What might they need to learn to make them? What may be a challenge?

### p5.js Web Editor Overview (5-10 minutes)

It’s up to you if you would like to run this session as a code along, or if you would like to have students clamshell their computers and simply watch. Decide based on what you know of your class and their ability to pay attention! In either situation, if possible, provide steps on a slide deck for any student who may miss steps.

Begin by reviewing how to login and navigate the editor.

If you are working with the p5 editor, be sure to demo saving - always foreign to students who didn’t grow up with Clippy - and how to open saved files. For repl.it, all changes are automatically saved but do review how to create new repls and how to find existing ones.

Remind students that having a user account will allow them to save their projects and share them on the web.

Review the main parts of the interface. After you’re done, ask students to log-in to their accounts. You might have to walk them through again on how to log in.

Once students are logged in, continue to the next section.

### createCanvas() and background() (5 min)

Introducing functions, parameter and the canvas will be the students first code along, so some students may ask you to repeat a step or to zoom in on sections of code.

While explaining functions, remind students that is important to use the right vocabulary words and syntax when describing the parameters(and their specific values or arguments) of functions. It will help them communicate their code and thinking to others. This will also assist their independent learning and research skills while using the reference guide.

As you code discuss the following:

Not all functions take the same parameters.

Some parameters have different scales. For example, the background function by default accepts values 0-255 but in HSB mode it accepts values 0-360.

### Independent Exploration (5 min)

After discussing the background() function, ask students to do the following independently:

* Change the values in createCanvas() to the following:
  * 100, 20
  * 60, 300
* Adjust the values of background() to anything they’d like.

Ask students what they notice - what do they think values in createCanvas and background control? Once they have ideas, formalize their understanding - createCanvas controls the width and height of the canvas, and background() changes the color of the canvas. Make sure they understand that numbers lower than 0 and higher than 255 have no effect, as that is a common misconception!

The visual below can help students have a better understanding.

![A scale going from black (0) to white (255) with number values marked in between.](<../.gitbook/assets/Screen Shot 2021-10-01 at 10.19.53 AM.png>)

**Then, ask students:**

What would happen if you were to add multiple background functions with different values? Which of background color is prioritized? Why?

### Line && Point Function Code Along (5 min)

For this code-along it is important to spend time reviewing how the canvas works in p5 and its differences from a cartesian plane. Students can copy these functions and their definitions into a journal. A good practice is to hang posters around the classroom every time a new function is added. Recreate the following example ([p5 editor](https://editor.p5js.org/cs4all/sketches/HkLEZg4Em) | [repl.it](https://replit.com/@qrtnycs4all/U1LA12-Line-and-Point-Example#script.js)) with your students.

```
function setup() {
  createCanvas( 600,  120 );
}

function draw() {
  background ( 180 ) ;
  
  //Draw a point at x=110, and y=80
  point( 110,  80 );

  //Draw a line from point(300, 20) to (400, 100)
  line( 300,  20,  400,  100 );
}
```

As you code, go over the following:

* Create various examples of a point and line with different parameters. After some iterations students may want to remove some lines of code but not delete them, this is a good opportunity to introduce comments.
* Comments
  * Introduce and consistently model how to create and utilize comments so that students can build great habits of annotating their code.
  * This is a great practice for debugging, testing new code, temporarily blocking out old code and a great what to keep track of shapes and functions.
* Ask questions like:
  * What type of parameters does the line function accept? Make sure students know that it accepts a numerical value and not text (a “string”).
  * How many parameters does line() accept? Refer to [https://p5js.org/reference/#/p5/line](https://p5js.org/reference/#/p5/line) to show the arguments.
  * How can the use of comments help organize the different lines?

### Student Practice (10 min)

Ask students to complete the following exercises on the online editor and title it "LinesU1L1.2"

1. Code the lines they found on their worksheet, and then:
2. Draw a point near the top-right corner of the canvas.
3. Draw a point in the middle of the canvas.
4. Draw a point near the bottom-left.
5. Draw a horizontal line, a vertical line, a diagonal line.
6. Draw a line from the top-left corner to the bottom-right corner.

Use the wrap-up section to have display students' work and for peer feedback

### Wrap Up

Bring students together to discuss successes the sticking points from the line() and point() practice. Have students come up to the front and live code the lines that they deconstructed from the do now activity.

Remember:

Student share outs are a powerful way to build community and promote student ownership of learning. _One approach could be creating a “sharing calendar” where 1-2 students share daily on a rotation (once the whole class has gone, shares start over again)._

Students should share struggles or strengths, and can either a) ask the class for help when sharing or b) share something helpful they learned with the class. Aim to be a teacher facilitator and allow the class to coach itself.

Be sure to conference with students the day they share prior to sharing, even if its a quick check-in, so they don’t feel they are being put on the spot or punished.

### Extension && Remediation

_For students that finish early have them:_

* Check that their code has comments so that they can pick up their work from wherever they left off.
* Use multiple line functions to create a rectangle and a triangle so the lines create a house (pentagon).
* Add comments for each line position.

_**For classrooms in need of extra help**:_

Consider utilizing the optional Desmos activities to better familiarize students with the canvas.
