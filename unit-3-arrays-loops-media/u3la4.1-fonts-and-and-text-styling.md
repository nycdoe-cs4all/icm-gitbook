---
description: How can I use custom fonts and text to enhance my programs?
---

# U3LA4.1 Fonts && Text Styling

### Overview && Teacher Feedback

In this learning activity, students draw text with different fonts (both system fonts and custom ones), manipulating their placement, size, and color.

The only new code introduced in this lesson are commands that control text styling - everything else is really about using custom fonts, which involves a little hopping in and out of the HTML. It's VERY IMPORTANT, as with images, that students are extra mindful of making sure they type (and capitalize, and space) everything correctly in their font names, as this is a common way that students will run into errors.&#x20;

This is a really fun time for kids, so enjoy it!

### Objectives

Students will be able to...

* Apply basic typographic principles when adding text to their programs&#x20;
* Add custom fonts from websites like Google Fonts to their programs&#x20;
* Create and style text in p5.js

### Suggested Duration

1 - 2 Periods (\~45 - 90 minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.7** Design or remix a program that utilizes a data structure to maintain changes to related pieces of data.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

\[FILL]

### Vocabulary

* **Font**: A font is a set of printable or displayable text character s in a specific style and size.&#x20;
* **Serif**: Serifs are semi-structural details or small decorative flourishes on the ends of some of the strokes that make up letters and symbols. An example would be the Times New Roman font.&#x20;
* **Sans-serif**: Sans serif does not have these details or flourishes. An example would be the Arial font.

### Resources

* [Finding and Adding Fonts ](https://youtu.be/JIv8J-CrSoA)(Youtube Video)
* [Using Custom Fonts](https://youtu.be/4B21lABmmKU) (Youtube Video)
* [Using Fonts Practice Starter Code](https://editor.p5js.org/cmorgantywls/sketches/TSVIWvEX2)
* [What is a font?](https://whatis.techtarget.com/definition/font)&#x20;
* [Google Font Pairings Examples](https://femmebot.github.io/google-type/)
* [Font Pairings Tool ](https://fontpair.co)
* [What is HTML and CSS? ](https://drive.google.com/open?id=13Git94LR3TgbAf1jQ3AHdOXCXjOqLSIU)(4 min video)&#x20;
* [Papyrus](https://drive.google.com/open?id=0BzEvNJib39cVdmc3SXpoQVBxOFE) (SNL Skit)&#x20;
* [The Rise and Fall of Comic Sans](https://www.greatbigstory.com/stories/the-rise-and-fall-of-comic-sans) (3 min video)&#x20;
* [Why You Hate Comic Sans](https://drive.google.com/open?id=1jNppnkxxvwwXEWqCSsW5RNoBYLh0BD6G)

### Do Now/Warm Up

![Three stop signs each with STOP in a different font.](../.gitbook/assets/fontSign.jpeg)

_Ask students to explain:_

How would you react to seeing each of these signs **in the wild?** Which do you think would be most likely to elicit the intended response of stopping? Why?

### Text & Fonts in p5.js

As we've seen, we can create text using the text() function. It must be given a string (the text it will display) as well as an x and y location for the text. (There are other optional values that will allow you to create a 'box' that the text will wrap in, kind of like how text naturally drops to the next line when you are typing in the editor or a word processor.)&#x20;

But there is a lot more to text, including a lot of things y'all have been asking about - you can change the size, the color (both stroke and fill, just like with shapes), and the **font** which we know has been something that everyone has been waiting for!

We've been saving fonts because in the world of design - and p5 - there is a lot to know about them, and we want to make sure that y'all have that down before we start playing.

### Not all Fonts Are Created Equal

First, let's review some background on fonts before we get into it on the computer. Although there are all kinds of crazy fonts out there - fonts that look like handwriting, fonts that look like big boxy letters - the readable fonts you would typically type large chunks of text in fall into two main categories:

![Image showing the difference between sans sand serif fonts.](<../.gitbook/assets/Screen Shot 2022-01-25 at 1.26.19 PM.png>)

'Serif' fonts just have that little extra foot on the letters, highlighted in red, and 'sans' or 'sans serif' fonts do not. (Sans is an old French and middle English word that literally means 'without.') As we start to take a look at fonts online, you will see that they are broken down into these categories.

There are so many other issues that typographers and designers are concerned with when they add text to projects. These are not issues we will be focusing on in this lesson, but it is worth noting that things like the space between characters (kerning), the maximum height of characters, and even the angle of certain parts of the letters are all things professional designers think about.

While we won't go too deep into all of that - which would be a class all on its own - we will keep a few things in the back of our mind as general rules for working with type:

1. Keep the number of fonts used to a minimum.&#x20;
2. Big chunks of text should be in standard fonts (a serif or sans-serif).&#x20;
3. Limit line length.&#x20;
4. Make sure your typeface looks good in various sizes!&#x20;
5. Use fonts with distinguishable letters.&#x20;
6. AVOID ALL CAPS EVERYTHING, IT IS ANNOYING AND LOSES IMPACT.&#x20;
7. Don’t minimize spacing between lines of text.&#x20;
8. Make sure you have sufficient color contrast if you expect something to be readable.&#x20;
9. Avoid coloring text in red and green (because of color blindness)&#x20;
10. Avoid using blinking text when possible (so you don’t trigger seizures)

It’s also worth knowing that some fonts come with a lot of baggage from the design community - fonts like Papyrus and Comic Sans give people a lot of strong feelings! Tread carefully if you choose to use them. Teachers, feel free to use the videos below to take a silly moment before you dive into the code explanations, or skip if you do not feel they would land well with your class:

* [Papyrus ](https://drive.google.com/open?id=0BzEvNJib39cVdmc3SXpoQVBxOFE)(SNL Skit)&#x20;
* [The Rise and Fall of Comic Sans](https://www.greatbigstory.com/stories/the-rise-and-fall-of-comic-sans) (3 min video)

![Screenshot of an old Kanye West tweet that reads "Sometimes I get emotional over fonts"](<../.gitbook/assets/Screen Shot 2022-01-26 at 10.45.35 AM.png>)

### Use a Web Font

Fonts on the web are downloaded from a server upon request. There are some fonts that all computers know and can access easily; common examples are "Arial", “Courier,” “Courier New,” “Georgia,” “Helvetica,” “Palatino,” “Times New Roman,” “Trebuchet MS,” and “Verdana”. Other fonts, computers need to be pointed towards either by having the downloaded font as part of our project, or by linking to the location of the font in our HTML.

Many options for finding fonts are available, often for free, on websites like [Google Fonts](https://fonts.google.com) and [Open Font library](https://fontlibrary.org).

In Google Fonts, you will need to click the fonts you would like (note that you an search by different categories or font names, and once you view a font you can retype the sample text to preview) and then click **+Select Font Family.** You can select one or multiple fonts at a time, but they will all show up in a selected fonts side panel. Once you've selected your font, you want to EMBED the font in the HTML using a code snippet that looks like this (font names will vary based on selection):&#x20;

```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Neonderthaw&display=swap" rel="stylesheet">
```

![Google Fonts Example](<../.gitbook/assets/Screen Shot 2022-01-26 at 11.22.39 AM.png>) ![Open Font Library Example](<../.gitbook/assets/Screen Shot 2022-01-26 at 11.23.03 AM.png>)

We then paste the embed link into the head section of our sketches' index.html file:

![HTML code from a project showing how the embed font code would be utilized.](<../.gitbook/assets/Screen Shot 2022-01-26 at 11.27.28 AM.png>)

From there, we can use this font in our code like so:

```
textFont("Font Name") //typed EXACTLY as it is in the documentation!
textSize(34)
text("This is the text that will be in your font", 0, 0)
```

(**NB**: _we also changed the size of our text. This is VERY similar to how you change font sizes when writing in Google Docs/Slides/etc! We could, if we wanted to, also change the stroke and fill of our text just the way we do with shapes, but note that not every font has a stroke, and not every font has a fill. You may need to experiment!_)

### Use a Downloaded Font

**NOTE:** _It is perfectly okay to skip doing this section full-class and instead save it on a need-to-know basis if kids find fonts they would like to download. In fact, it's what many teachers choose to do to avoid extra chaos when learning new skills!_

Maybe the sites that host web fonts don’t have what you’re looking for - that’s okay! You can download font files directly to your computer and upload them into your program so they can be used and seen everywhere.

The steps to include a downloaded font in our sketch are similar to those we took to include an image in the previous learning activity. We copy the file into our sketch folder (p5 supports the TTF and OTF file formats), load it into a variable preload using loadFont, and then set our text to it using textFont.

```
var font;

function preload() {
  font = loadFont("source-code-pro-regular.ttf");
}

function setup() {
  createCanvas(600, 120);
  textFont(font);
}

function draw() {
  background(255, 255, 0);
  textSize(28);
  text("pls no boop DO NOT", 110, 60);
  textSize(14);
  text("pls no boop DO NOT", 170, 90);
}
```

### Practice: Build Your Font Library!

Open [**this starter code**](https://editor.p5js.org/cmorgantywls/sketches/TSVIWvEX2) of boring sentences that you will be styling. Before you can begin, you will need to build your font library. Go forth onto Google Fonts (or Open Font Library) and find the following to add to your program and slide into that array:

* 3 Serif Fonts&#x20;
* 3 Sans Serif Fonts&#x20;
* 2 Display Fonts&#x20;
* 2 Handwriting Fonts

Then, give each sentence:

* It's on unique font
* A specific size
* A fill/stroke color.

### Extension

The extension options here are all extras that students can choose to engage with if they wish (or that you can integrate to extend the lesson):

1. **Using line breaks:** including \n within a string (like "hello\nworld") will insert a line break. See if you can break up the sentences in interesting ways without using a second text() call!
2. **Define boxes for text:** We can constrain a text to be drawn within a box by adding x, y, width, and height parameters to the call to text:

```
function setup() {
  createCanvas(600, 120);
  textFont("Gloria Hallelujah");
}

function draw() {
  background(255, 255, 0);
  textSize(32);
  text("pls no boop DO NOT", 110, 60);
  textSize(14);
  //text will wrap within a 200 by 50 box with it’s top corner at (170,90)
  text("pls no boop DO NOT", 170, 90,200,50);
}
```



