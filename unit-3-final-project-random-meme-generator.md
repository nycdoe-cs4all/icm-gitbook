---
description: How can memes be created by code?
---

# 🎨 🎨Unit 3 Final Project: Random Meme Generator

### Overview/Teacher Feedback

As the course progresses and students gain the skills to explore and create independently, the work becomes less and less lesson-focused and more and more project-focused. There have been _a lot_ of mini-projects over the course of this Unit; the goal of this project is to combine all of the skills students have been practicing somewhat discretely together into one program. However, if you feel that it is difficult to go from mini-project into final project, you are of course welcome to skip or alter this project to fit the needs of your classroom.

Additionally, this project involves the use of sound. If that is something that you did not cover in your classroom, or you feel students will unnecessarily struggle with, feel free to take it away or make it an extension as you see fit.

**To begin this project, you may want to have students think about the following:**

1. What is a meme?&#x20;
2. What purpose do they serve?&#x20;
3. How can memes support free expression?

As a class, you may want to review this [history of memes](https://www.nytimes.com/2022/01/26/crosswords/what-is-a-meme.html) or this video on [how memes shape politics.](https://www.youtube.com/watch?v=DazKys0gpHU\&ab\_channel=HuffPost)

**NB:** _As students try to get many images that can be different sizes to show up nicely on their canvas,_ [_consider sharing this resource on making images display proportionally._](https://editor.p5js.org/L05/sketches/o1a4f6XpE)__

### Prompt

In this project, you will create a random meme generator using the [macro image meme format](https://knowyourmeme.com/memes/image-macros)! This is your opportunity to make your peers and teacher laugh so get creative and silly (while staying classroom appropriate) with this project.

![Four differently commonly used meme images.](<.gitbook/assets/Screen Shot 2022-02-11 at 10.24.07 AM.png>)

#### Requirements

Create a random meme generator: pick a collection of images and a collection of phrases from an array. Each time you run your sketch, it should select one random image and one random text from the appropriate arrays, creating a (potential) meme displayed on the canvas. You have the option to either use objects to keep certain captions/fonts/images together, or simply organize in arrays and let chaos reign.

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

### Suggested Duration

3- 6 45-minute periods, depending on the pace of your class and the level of challenge your students attempt.

### Sample Output

![Sample meme](<.gitbook/assets/Screen Shot 2022-05-23 at 2.43.36 PM.png>) ![Sample meme](<.gitbook/assets/Screen Shot 2022-05-23 at 2.43.48 PM.png>) ![Sample meme](<.gitbook/assets/Screen Shot 2022-05-23 at 2.44.01 PM.png>) ![Sample meme](<.gitbook/assets/Screen Shot 2022-05-23 at 2.44.20 PM.png>)

[**Example Project Code**](https://editor.p5js.org/cmorgantywls/sketches/SOCouTm6G)****

### **Culturally Responsive Best Practices**

Within this design-based challenge, there are many prompts you can give students to make the project seem more relevant to them and the cultures of communities that they are a part of. _(Please recall that communities can refer to a lot of things, including just the culture of being a teen, a Minecraft player, or a KPop fan - be mindful that you are allowing students to explore choice in their creations in a way that is authentic to them!)_

**Possible CR-SE Prompts:**

1. Program a meme generator that outputs memes that are funny and relevant to your culture and lived experience. Use meme formats currently relevant on the internet
2. Focus your memes around a single theme or format that are funny and informative, teaching the user about something specific to your culture or lived experience.
3. Output memes that draw attention to/inform about a specific cultural or social justice issue.
4. META MEMES: Learn about the role memes play in popular culture. Create memes that will engage the viewer and teach them about the role memes play in our world, including stages like recent elections.. (Resources: [1](https://yp.scmp.com/news/features/article/107044/why-do-memes-matter-look-good-dank-and-viral) | [2](https://academic.oup.com/jcmc/article/18/3/362/4067545) | [3](https://www.theguardian.com/us-news/2016/nov/04/political-memes-2016-election-hillary-clinton-donald-trump) or do a quick google search of your own!)

### **Extensions**

Some possible extensions could be:

1. Create a meme from multiple random images and text. Each time the programs run it should make a new combination.
2. Add sound to your project
3. Find a way to make your meme generator interactive (through clicks/keys that 'reroll' or refresh the meme, or something that will allow the user to choose an image/caption/font).
