---
description: How can I manipulate an image in p5?
---

# U3LA3.2: Tint && Image Manipulation

### Overview && Teacher Feedback

In this learning activity, students load, display and manipulate image files of different formats, changing their placement, size, and tint color. They will discuss how tint can be used to create an illusion of depth.

This lesson allows a little more creative practice with images, rather than strictly practice with adding to the program folder & loading into arrays. Students will investigate tint and then apply some nested for loops to draw a grid of images. (Feel free to move away from the forestry theme if you see fit!)

Tint can be very overwhelming - if you add a strong tint, it can basically just turn a photo red or blue or green which, while sometimes exciting, doesn’t have a ton of practical application. The best strategy is to try to steer students towards thinking of tint like an Instagram filter; it slightly alters the colors in an image to help it to look better or blend better with other things happening in the program. It’s okay if students in your class haven’t developed the color or design sense to always understand why this is useful, just as long as they understand that they have this tool at their disposal.

### Objectives

Students will be able to:

* Use a for loop to draw multiple instances of an image&#x20;
* Use tint to alter the appearance of an image

### Suggested Duration

1-2 class periods (\~45 - 90 minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Abstraction**

* Give examples of specific patterns in something I can see, do or touch.

**Algorithms**

* Explain why I used specific instructions to complete a task.&#x20;
* Compare and contrast my instructions with other instructions that complete the same task.&#x20;
* Demonstrate the benefit of using an event, conditional or loop in my prototype.

**Prototype**

* Experiment with the commands of a programming language.

### **Vocabulary**

* tint == a colored overlay that adjusts the appearance of pictures. (think Instagram filters!)&#x20;
* Foreground ==elements at the front of a scene&#x20;
* Middleground == elements in the middle of a scene&#x20;
* Background == elements farthest away in the back of a scene

### **Planning Notes**

|                                                                                                                                                                     Planning Notes                                                                                                                                                                     |                                                                                               Materials Needed                                                                                               |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| <p>You will want to have some images easily at your disposal for the code along - pick some beforehand, or use the opportunity to review searching (esp for images with transparent backgrounds)/saving with students. <br><strong></strong>You can also share images with students if you don’t want them to waste time finding one of their own!</p> | No extra materials are required per se - but if you feel the need to be more hands-on/delve deeper into exploring fore/middle/background, you could definitely have some cut-out papers to assist with that. |

### Resources

* [Using Tint](https://youtu.be/RBv-84ToduA) (Youtube Video)
* [Sample Project](https://editor.p5js.org/cs4all/sketches/mk1PbEGqL)

### Assessments

**Formative:** Collect their final forest if you’d like!&#x20;

**Summative:** U3LA3 Mini Project: Vision Board

### Do Now/Warm Up (3-5 min)

Ask students the following:

You’ve just taken a picture that you want to share with the world. What are some things you might want to do it before you post it on social media?

_After students share ideas, relate some of these to computer science (adding text or mark up can be easily done in p5!) and explain that the idea of “filters” relates to what they will learn today._

### Load an Image & Play with Position, Size, and Tint (5 - 10 min)

Remind students again how to load an image into their project, make sure it has a usable name, etc etc. Once the image is there, review position and size, which students saw in U3LA3.1.

The new material for them involves applying tint to an image, which for our purposes we will think of like fill - but for images instead of drawn shapes. In that way, it's a bit like an image filter, which your students are probably very used to hearing about. The best way to explain it is to draw a lot of comparisons to filters they are familiar with from Instagram or other photo apps! The big difference here is that in p5 we have total control - so we can make overwhelming tints that essentially turn an entire image blue, or we can be subtle and just balance out the colors. Try to steer your students towards the latter (unless they want to read about brutalism and make some intense and purposeful design decisions).\
\
Tint is based on what color mode you are in - HSB or RGB - and will look like this (alpha being an optional 4th value like in fill): **tint(v1, v2, v3, \[alpha])**

In this activity, we are going to play with our image a bit. Just for fun, go find an image of some creature you find in nature - try to find one with a transparent background (most likely this will be a png file). When searching from Google Images, click Tools after your search, then click Colors -> Transparent to filter for images with a transparent background.

Once you load your image, it should look something like this:

_**NB**: Your code will vary from the examples as you are finding and uploading your own sample image with students. As such, your file may not be called birch.png, and your image may not even be of a tree!_

```
var tree 

function preload() {  
   tree = loadImage("tree.png")
}
 function setup() {  
   createCanvas(400, 400);
   colorMode(HSB)
}
 function draw() {  
   image(tree,200,300, 100, 200); 
} 
```

As we’ve seen before, the second and third parameters of the image function set its position on the canvas. In the sketch below, instead of drawing our image at the canvas origin as above, we are drawing it at (x,y) = (200, 300). If we were to add a fourth and fifth parameter, so it reads image(tree,200,300,100,200); we would be adjusting the width and height to 100px and 200px respectively.

If we choose to use tint, we call it _before_ the image function, similarly to how we call fill before the shape we wish to change. Tint causes the image to be drawn with a color fill, defined by RGB or HSB values depending on the current colorMode. Adding a fourth parameter for the alpha channel we could make the image transparent. In the example below the tint color uses HSB to create a slightly bluer version of our tree:

```
var tree
 function preload() {  
   tree = loadImage("tree.png")
}
 function setup() {  
   createCanvas(400, 400);
   colorMode(HSB)
}
 function draw() {  
   background(220);
   tint(180,70,60);
   image(tree,200,300,100,200);
 } 
```

When we change tint with high saturation and brightness, the results can be very overwhelming - however, if we are more subtle in our adjustments, they can work like Instagram filters and make images look better, or go better together.

### An Experiment in Opacity (5 - 10 min)

Let’s add another tree, and with this one, adjust the opacity. What do you notice?

```
var tree 

function preload() { 
 tree = loadImage("tree.png")
}

 function setup() {  
   createCanvas(400, 400);
   colorMode(HSB)
}

 function draw() {  
   background(220);
   tint(180,70,60); 
   image(tree,200,300,100,200); 
   tint(180,70,60,0.3); 
   image(tree,250,350,100,200);
} 
```

### Using Tint to Create Depth (5- 10 min)

Let's take a pause for a moment to discuss a little color theory; move away from the editor for just a moment so we can talk about how tint (and colors in general) can be used to create depth in a 2D design.\
\
From an art perspective, any scene you create has a foreground, a middle ground, and a background. Check out this classical example to understand each one:

![Image of a bucolic oil painitn gwith background, middle ground, and foreground labeled.](../.gitbook/assets/bg\_p5.png)

Generally, the **foreground has the warmest, most saturated colors**, because you are supposed to feel that it is close. **Warm colors** tend to be **reds** and **oranges**, but sometimes we see this effect with other colors that are just very saturated. The **middle ground** **has colors somewhere in the middle, while the background has the coolest, least saturated colors**. **Cool colors** are generally **blues, purples, and greens**, but this effect can be achieved with any unsaturated color. While it’s not true in this example, sometimes the background might be darker, as well, depending on the scene that is being created.

**If you are interested in doing a deep dive into art/design/color theory**, you could turn a good 20-40 minutes into just exploring this idea with colored paper cutouts and having students make a design with a defined fore/middle/background - but that is way above and beyond and not totally necessary to complete this project.

### Create a Forest Scene (7-10 min)

As a pair programming activity or on their own, have students find an image of a tree (or several trees) with a transparent background. Using several for loops, create ‘rows’ of trees to create a forest scene. Give each row a unique tint so that it creates the illusion of having a foreground, middle ground, and background.

**NB:** _Students could absolutely do this without for loops, but it would be a much less efficient way of solving this problem and would probably take a long time. If you have students who go this route (because combining the for loop and image skill may be confusing), be sure to talk about it with them (and the class, if necessary) to get more buy-in using a for loop._

_**Please view the sample project if you need guidance on the output!**_

### **Wrap Up (5 min)**

Students can share their creations or submit them for a grade; consider including some reflection questions about how they used tint and how they might find uses for this function in the future.

### **Extensions**

**Can you add the following to your project?**

* Add multiple tree images to an array, and select a random tree to draw each time.&#x20;
* Hide several creatures within your forest - play with opacity if you want them to be super camouflaged!&#x20;
* Increase the brightness of the tint on a row of trees if it is clicked on
