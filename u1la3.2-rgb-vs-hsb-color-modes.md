---
description: How can I represent colors in a mode other than RGB?
---

# U1LA3.2: RGB vs HSB Color Modes

### Overview && Teacher Feedback

In this learning activity students add color to any of their previous designs. Both the RGB (Red, green, blue) and HSB (Hue, Saturation, Brightness) color models are applied.

Students apply the programming concepts they learned in the previous unit (variables, randomness) to color manipulation, defining color ranges and palettes.

* This lecture is fairly direct. Plan to keep it short so that students can experiment and play, as that is how they will learn best.&#x20;
* It may be useful to create some type of note-catcher for your students, or be sure to plan on certain topics they should be getting into their notebooks.&#x20;
* You can demo with any colors you would like, just plan on giving a variety of demonstrations. You could even pick colors from around the room and have students try to describe them.&#x20;
* You may want to display the hue/saturation/value infographic during the color picker game, as students might need assistance visualizing the color wheel. You could even annotate the 360 in 90s to help students who are struggling.
* &#x20;For the CFU, It’s useful to have an estimate in mind for what is acceptable.&#x20;
* It’s unlikely any students will be able to name a shade exactly - but they should have an idea that bright colors have a high saturation, colors around 360 - 50 are reddish tones, etc etc.&#x20;
* During the practice, it’s useful to display instructions on a slide to avoid student confusion.

### Objectives

Students should be able to:

* Students will be able to explain and utilize the HSB color mode.&#x20;
* Students will understand the differences between RGB and HSB color modes.

### Suggested Duration

\~1 Period (45 minutes)

### Blueprint Foundational Student Outcomes

**Abstraction**

* Describe how I might use patterns to express an idea.&#x20;
* Explain why using patterns is necessary when creating with a computer.

**Algorithms**

* Describe more than one set of instructions that might complete a task.&#x20;
* Describe how instructions can have different outputs depending on inputs.&#x20;
* Explain why I used specific instructions to complete a task.

**Programming**

* Experiment with the commands of a programming language.&#x20;
* Explain why I chose specific commands to communicate my instructions.&#x20;
* Discuss what can and cannot be done with a specific set of commands.

### Vocabulary

* HSB Color Mode&#x20;
* Hue - the shade of a color&#x20;
* Saturation - the intensity or vividness of a color (sometimes referred to as chroma)&#x20;
* Brightness - the amount of white or black present in a color

### Planning Notes

|                                                                   Planning Notes                                                                   |             Materials Needed             |
| :------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------: |
| RGB is an important step to understanding how computers use color, but it should also pose a headache for students. Use this to launch the lesson! | No materials needed aside from computers |

### Resources

* Partner Color Guess Code ([Guesser](https://editor.p5js.org/cs4all/sketches/Hk-F\_ghXm) | [Judge](https://editor.p5js.org/cs4all/sketches/By4eFxnm7))&#x20;
* [Color Application Practice ](http://editor.p5js.org/cs4all/sketches/rJ31kZ3QQ)
* [HSB Color System ](https://learnui.design/blog/the-hsb-color-system-practicioners-primer.html)
* [HSB Color Mode](https://youtu.be/lt1lDp2aFLQ) (Youtube Video)

### Assessments

Color Application Practice & Reflection Questions

### Do Now/Warm Up (5 min)

Ask students:

1. What can be confusing about RGB color values?&#x20;
2. If you type three random numbers, can you always predict what the color will look like?

You may want to show students a very subtle color, like a lavender, and tell them you will hand over some \$$ (or another reward) who can perfectly match the color within 1-2 guesses using RGB values.

### HSB Color Space

Use the launch to introduce our new colorMode, which is changed in the setup function using colorMode(HSB). (This is demonstrated in the suggested game.)

![3D color wheel showing hue, saturation, and value shifts in color.](<.gitbook/assets/Screen Shot 2021-10-18 at 3.05.15 PM.png>)

* **Hue** is where the color falls on the rainbow spectrum (EX, a yellow, a red, a purple, etc).&#x20;
* **Saturation** refers to how vivid the color is, or how much of the color is present. (EX: Something that is REALLY yellow looks like a highlighter).&#x20;
* **Value** (Brightness) is the amount of white or amount of black present in a color.

Explain and demonstrate to students that this is method is helpful for choosing colors logically, as in the following examples:

![](<.gitbook/assets/Screen Shot 2021-10-18 at 3.07.15 PM.png>)

After the introduction, have students practice with the Color Picker Game linked in the resources. Students should complete this activity in pairs, but could also work in a group of three passing two computers (two students will judge at a time).

**Instructions**:

1. Have pairs sit opposite one another, their computers back to back.&#x20;
2. Player 1 is the Guesser and will [open this code](https://editor.p5js.org/cs4all/sketches/Hk-F\_ghXm) and press play for a random HSB color to appear, in numbers only, on the screen.&#x20;
3. The Guesser will read these numbers to Player 2 - the Judge - who will fill in their own code. The Guesser will then try to describe the color based on what they know about hue, saturation, and brightness.&#x20;
4. The Judge will guide the Guesser as to if they are close or not and give hints as necessary. Once the Guesser has gotten close, the Guesser and Judge will swap computers and roles and play again.

You may want to display the hue/saturation/value infographic during this game, as students might need assistance visualizing the color wheel. You could even annotate the 360 in 90s to help students who are struggling.

After 10-15 minutes of practice, you might want to do a CFU to assess student learning:

* Display a color on the board OR pick a color from somewhere in the room, and ask students to record their best estimate of the HSB color on a post it.&#x20;
* Collect post-its to assess where students are. (You could even ask students to name the HSB color of their post-it if you have fun colors).&#x20;
* It’s useful to have an estimate in mind for what is acceptable. It’s unlikely any students will be able to name a shade exactly - but they should have an idea that bright colors have a high saturation, colors around 360 - 50 are reddish tones, etc etc.

Then, regroup and have students should switch partners so they are now working with the person next to them. They will complete this [color practice](http://alpha.editor.p5js.org/SEP/sketches/rJ31kZ3QQ), which will look familiar from the previous lesson.

Ask the student pairs to do the following:

* First navigator to create a neon rainbow with fill and a pastel rainbow in the stroke.&#x20;
* Second navigator will create a muted rainbow in the fill and a dark rainbow in the stroke.

### Wrap Up

Pick any assortment of the assessment questions above and put them in a Google Form where you can collect student answers and code links. A best practice is to also get links of student partners!

* Describe hue, saturation, and brightness and what each one controls.&#x20;
* What is your best guess as to what (HSB COLOR) would look like?&#x20;
* Describe how you would make a muted magenta in HSB.&#x20;
* How do you change to HSB in your p5 projects?

### Extensions

1. Using what they learned in Make it Vary, ask students to create different variables to generate different the background colors whenever you press play on the sketch. [Possible Solution ](http://editor.p5js.org/cs4all/sketches/rJJiKCnVm)
2. Use the color wheel to generate a random shades of colors. (e.g. shades of red, blue or green)
