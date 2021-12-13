---
description: How can sounds, images, and fonts be combined and manipulated with code?
---

# 🗃 🗃U3LA1 Mini Project: Wallpaper Design

### Prompt

You recently have been hired by Microsoft’s design team to create 2 new wallpapers for their new line laptops. In order to boost sales and reach out to many different audiences, Microsoft would like these wallpapers to have some different color themes and use repetition. Be as creative and original as possible!

**Task**:

Create 2 variations of a desktop background using repeated elements. The design should be easily altered by changing the values in the for loop to create variations in the design.

**Requirements**:

1. Your canvas size should be (800 x 450)&#x20;
2. The program should include at least one for loop.&#x20;
3. The for loop(s) should be used to increment values such as width, height, or color. Variations should result from changing different values in the loop.&#x20;
4. The designs should not only vary in color. Play with size, number of repetitions etc.&#x20;
5. Save three different variations of the same design.

**Writing Prompt:**

Write a paragraph explaining what your wallpaper means to you and why it should be added to a new line of laptops by Apple or Microsoft.

### Sample Output

![Example of three outputs with colorful geometric designs made up of several shapes.](<../.gitbook/assets/Screen Shot 2021-12-13 at 11.39.57 AM.png>)

Students can right-click to save their design from the editor.&#x20;

**OPTIONAL:** _Alternately, you are welcome to briefly teach students how to program in a save option using the_ [_built in saveCanvas() function_](https://p5js.org/reference/#/p5/saveCanvas) _or_ [_save function_](https://p5js.org/reference/#/p5/save)_. The former requires the canvas to be stored in a variable, but the latter will just save an image of the canvas by default. If you choose to introduce this to students, they should use them in a major callback function outside of the draw function to avoid repetition, such as mousePressed or keyPressed, like so:_

```
// Option 1 - mousePressed major callback
//mousePressed happens outside of and after draw (built in event listener for p5.js)

function mousePressed(){
   save("myCanvas.jpg")
}
```

```
// Option 2 - keyPressed major callback
//keyPressed happens outside and after draw (built in event listener in p5.js)

function keyPressed(){
  if(key==='s'){
    save("myCanvas.jpg")
  }
}
```

### Extensions

**Randomize your wallpaper**

* Use the random function to generate variations of your wallpaper.&#x20;
* It should randomize the size of the shapes or color while still keeping the same shapes and design in place.
* Additionally, play with using mouseX and mouseY to vary your loop output!

### Teacher Notes

This is a brief, fun project that students usually complete in 1-2 days. It's very visually appealing and the usually enjoy what the make! Consider ending the mini project with a gallery walk or other feedback cycle so students can show off their work and get feedback.

If you collect student work with Google Forms, you can designate that a question be answered with a file so students can easily upload their saved canvas images. (Click the question type option - multiple choice by default - and select 'file upload.' It will aggregate them to a single Drive Folder.)

**If you download this folder, you can use it as your computer background and have your computer rotate through the different images during the day.** Students really like seeing their work on your screen - consider sharing with the rest of your school staff so the kids know you brag about their work outside of the computer science room!
