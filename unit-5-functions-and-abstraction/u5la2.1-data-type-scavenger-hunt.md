---
description: What are the different types of data used in JavaScript?
---

# U5LA2.1: Data Type Scavenger Hunt

### Overview & Teacher Feedback

While students have been working with data types throughout the whole unit (and have probably intuited when to use quotation marks and when they are not needed), there has been no solid, formal lesson that explores data types. This is there chance to discuss and explore the types of data being used and their purpose before they start engaging with and creating functions that will return data rather than simply performing actions on the canvas.

### Objectives

Students will be able to:

* List common datatypes used in JavaScript&#x20;
* Test and identify the types of different pieces of data

### Suggested Duration

1 Period (\~45 minutes)

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundations Student Outcomes

**Data, Data Abstraction & Storage:** Data is represented in computers as binary, but humans save and use data on computers as lists, databases, key-value pairs, etc.

**Programming, Syntax:** All programming languages have a set of commands or reserved words and grammar rules that must be followed.

### Vocabulary

* **Data Types**&#x20;
* **String**: characters enclosed in “ “, ‘ ‘, or \`\`.&#x20;
* **Number**: numeric values not enclosed in “ “, ‘ ‘, or . They can be further broken down into integers (positive values, negative values, and zero without decimal places) and floats (values with decimal places), but it is not necessary to make this distinction in JavaScript.&#x20;
* **Boolean**: a data type with only two value options often seen as “true” or “false”
* **Object**: a standalone entity, with a type and the option to have many distinct properties. A good example is a sneaker - while it may always follow the same design, it can come in different colors, sizes, types of laces, etc. This would be one object with its own properties.

### Planning Notes

|                                                                                                                                                                                Planning Notes                                                                                                                                                                               |                                                      Materials Needed                                                     |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------: |
| <p>This lesson is largely driven by student exploration and it can feel as if it goes by quite quickly - however, while the actual task is brief, it is meant to lead into a discussion to deepen student understanding.</p><p></p><p>Students should be prepared to identify data types and start thinking about when data types are useful by the end of this lesson.</p> | Scavenger Hunt Starter Code && Document (_This can all be digital, but consider options if you think you need to print!)_ |

### Resources

* [Scavenger Hunt Worksheet](https://docs.google.com/document/d/1fW3VMQtDPbq8\_OsERONbMW8Qu1zKVXCUsg-E-I0oaAY/copy) (Google Doc)
* [Scavenger Hunt Starter Code](https://editor.p5js.org/cs4all/sketches/W\_fQXjB6b) (p5.js Sketch)
* [Data Types in JavaScript](https://youtu.be/4JgIcc3E-cI) (Youtube Video)

### Assessments

* Data Type Scavenger Hunt Worksheet (formative)&#x20;
* Exit Slip (formative)

### Do Now/Warm Up (2-3 Minutes)

**Display on board:** Why won’t this code work?

```
ellipse(“fifty”, 100, 25)
```

### Discussion & Scavenger Hunt Instructions (\~7-10 minutes)

After allowing students time to think through the do now and write down their responses, ask for some shares - many students will recognize that “fifty” is what breaks the code, despite the fact that we understand “fifty” to be a number.

Use this to launch into a conversation about data types in computer science generally, and JavaScript specifically. Be sure to review the names and definitions of these data types (some of which students may remember):

* **Strings**&#x20;
* **Numbers** (you can discuss floats and ints if students have a background in other languages, or will progress from this class to a class run in another language)&#x20;
* **Booleans**&#x20;
* **Objects** (object literals, but arrays are also a type of object!)

Explain that there are many other data types, but JavaScript is a lightly typed language, so it is pretty kind about moving between them. Make sure students understand that we are focusing on data types today because they are about to start focusing on functions that pass data rather than conduct an action like drawing a design, and it’s important that they understand the different types of data that they can pass.

### Data Type Scavenger Hunt (\~10 - 15 minutes)

Distribute and explain the data type scavenger hunt to students based on the worksheet instructions, and then let them begin working. Be sure to circulate, as some students may need assistance to make sure they are removing/adding quotation marks when necessary and recording data types AND the actual data that gets printed in the correct locations.

This activity can be completed individually, in pairs, or in small groups. Best suggestion is to ask students to each complete their own activity, but compare answers within a small group.

### Wrap Up

Once students have completed their scavenger hunts, gather them to review answers - if not to all the data, to some of the trickier ones. Ask students to explain where possible and fill in any gaps or misconceptions they may have.

**Ask**:

* What are things you noticed when doing this activity?&#x20;
* Did any of the answers surprise or confuse you?&#x20;
* What happened when you tested the data type of variables?

Make sure students understand that EVERY piece of data in their code has a type, and variables simply hold onto a piece of data and take the type of that piece.

You may choose to give a prolonged exit slip where students try to determine data types without computers. Consider leveling the data so you ask questions as follows:

* What is the data type of “Rebecca”? (MILD)&#x20;
* What is the data type of 4519000? (MILD)&#x20;
* What is the data type of “Cat” != “Dog”? (MEDIUM)&#x20;
* What is the data type of \[“cs”, “is”, “the”, “best”]? (MEDIUM)&#x20;
* What is the data type of the variable mouseIsPressed? (SPICY)

For any and all, feel free to ask students for an explanation of how they know. You can choose to have students answer all questions or a mix depending on in-class performance.

### Extensions

**Ask students to dig more deeply into data.** Challenge them to try to create their own pieces of data, predict the type, and then see what comes up.

You may also want students to start understanding that the data type of **object** represents a whole set - such as an entire array - while each item in that set, or array, still maintains its own type. Consider asking them to save an array (or even an object!) to a variable and try to call individual items to see what comes up.
