---
description: How can memes be created by code?
---

# 🎨 🎨Unit 3 Final Project: Random Meme Generator

### Overview/Teacher Feedback

As the course progresses and students gain the skills to explore and create independently, the work becomes less and less lesson-focused and more and more project-focused. There have been _a lot_ of mini-projects over the course of this Unit; the goal of this project is to combine all of the skills students have been practicing somewhat discretely together into one program. However, if you feel that it is difficult to go from mini-project into final project, you are of course welcome to skip or alter this project to fit the needs of your classroom.

Additionally, this project involves the use of sound. If that is something that you did not cover in your classroom, or you feel students will unnecessarily struggle with, feel free to take it away or make it an extension as you see fit.

**NB:** _As students try to get many images that can be different sizes to show up nicely on their canvas,_ [_consider sharing this resource on making images display proportionally._](https://editor.p5js.org/L05/sketches/o1a4f6XpE)__

### Prompt

In this project, you will create a random meme generator! This is your opportunity to make your peers and teacher laugh so get creative and silly (while staying classroom appropriate) with this project.

![Four differently commonly used meme images.](<.gitbook/assets/Screen Shot 2022-02-11 at 10.24.07 AM.png>)

#### Requirements

Create a random meme generator: pick a collection of images and a collection of phrases from an array. Each time you run your sketch, it should select one random image and one random text, creating a (potential) meme. You have the option to either use objects to keep certain captions/fonts/images together, or simply organize in arrays and let chaos reign.

Think about what fonts and images you may want to use and how you will source them. As an extra challenge, you can make a sound play when the meme loads. Consider how you could find these things!

#### Your Sketch Should Have:

* A random() function&#x20;
* At least 5 images stored in an array&#x20;
* At least 5 phrases or strings stored in an array
* At least 5 fonts
* A data structure to organize your program. (This could be arrays, objects, an array of objects, etc.)
* The text has to show up on top of the image.
* If using sound, you should find at least 3.

#### Suggested Steps:

1. **Gather resources.** Find all of your images/fonts/sounds and write out the captions you plan to use.
2. **Load into program.** Get your images/sounds in your program. Then, make data structures (most likely arrays) that will hold all the image names, all the font names, all the captions, etc.
3. **In the preload function, pick a random value (or several) and load the image/sounds and fonts and captions directly into an object literal.** This will help keep you organized!
4. **Use the information from your data structure to get the image and styled caption (and possibly sound) on the screen.** Adjust as needed!
5. **Run the program and make any tweaks/changes.**

### Sample Output

![Two sample memes](<.gitbook/assets/Screen Shot 2022-02-11 at 11.50.21 AM.png>)

[**Example Project Code**](https://editor.p5js.org/cmorgantywls/sketches/SOCouTm6G)****

### **Extensions**

Some possible extensions could be:

1. Create a meme from multiple random images and text. Each time the programs run it should make a new combination.
2. Add sound to your project
3. Find a way to make your meme generator interactive (through clicks/keys that 'reroll' or refresh the meme, or something that will allow the user to choose an image/caption/font).
