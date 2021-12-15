---
description: How can arrays help us simplify code?
---

# U3LA2.1: Introduction to Arrays

### Overview && Teacher Feedback

In this lesson, students will be introduced to the concept of arrays.

Arrays are an important and useful concept in computer science as they allow us to easily store a lot of information in an orderly fashion. (And they will be used in many future lessons!) Arrays can be confusing to students when it comes to calling index values to access elements of the array. It would be good to create multiple array examples and then have students call the elements with either hard coding the number or using a variable. Students will have an opportunity to integrate through a list using a for loop in a later lesson.

### Objectives

Students should be able to:

* Explain how an array can be used instead of multiple variables&#x20;
* Create arrays&#x20;
* Retrieve information from arrays

### Suggested Duration

1-2 periods (\~45-90 minutes)

### Blueprint Foundations Student Outcomes

Abstraction:

Give examples of specific patterns in something I can see, do or touch.

### Vocabulary

* **Array** - an ordered series of data&#x20;
* **Index** - a position within an array&#x20;
* **Element** - a piece of data in an array&#x20;
* **Zero-Indexed** - The first element of an array has an index of 0, not 1

### Planning Notes

|                                                     Planning Notes                                                    |       Materials Needed       |
| :-------------------------------------------------------------------------------------------------------------------: | :--------------------------: |
| There are no specific planning notes for this lesson, but it is the first lesson students will be using media - whoo! | No special materials needed. |

### Resources

* [Introduction to Arrays](https://youtu.be/qq6rsfemYYA) (Youtube Video)
* [Colors in Arrays](https://youtu.be/O-gAiUNtZ3Q) (Youtube Video) | [Starter Code](https://editor.p5js.org/cmorgantywls/sketches/tBzRpplfn)
* [7.1 What is an Array?](https://youtu.be/VIQoUghHSxU) | Code (6.1)&#x20;
* [Learning Processing:](http://learningprocessing.com/examples/) Chapter 9. Arrays&#x20;
* [Getting Started With p5.js:](https://p5js.org/books/) Chapter 4. Variables (Section: Repetition)&#x20;
* [Arrays information - Code.org](https://youtu.be/seBDTeZmb-k) (Youtube Video)

### Assessments

Assess the **Do Now** assignment. Check for the ability to:

* Connect real-world concepts with computer sciences.&#x20;
* Discuss the benefits of data structures.

Assess the **learning activity.** Check for the ability to:

* Understand arrays as a new data structure.&#x20;
* Identify data types that can be stored in arrays.&#x20;
* Pull values from array elements.&#x20;
* Use arrays to prepopulate parameter values for a design.

Assess the **Wrap Up** assignment. Check for the ability to:

* Describe how arrays work.&#x20;
* Explain the benefits of using arrays in p5.js.

### Do Now/Warm-Up (\~3-5 min)

Ask students to describe what makes lists useful in everyday life.

* What makes a list useful?&#x20;
* How would lists be useful in programming?&#x20;
* How can we use lists in p5.js?

Discuss with students possible answers:

* Lists help us organize information.&#x20;
* Lists help us collect all the relevant information in one place.&#x20;
* Lists show that a lot of ideas are related.&#x20;
* Lists help us order or prioritize ideas.&#x20;
* Lists help us think about the big picture

Tell students that we will be creating and using arrays which are the same concepts of lists in real life.

### What are Arrays? Grocery Store Example (15 min)

Computer scientists spend a lot of time thinking about information. After all, computers are just tools to manipulate pieces of information in certain ways. Before computers were around, humans invented lots of different ways to store information. The library was given the Dewey Decimal system, in which numbers were associated with the information in certain books. That’s a pretty complicated way of storing information.

But one way of storing information that you’ve definitely used before is a list. Maybe you’ve made a list of people to invite to your birthday. Maybe you made a list of things to buy at the grocery store. Something useful about lists is that they’re one object themselves: you don’t have to carry around a lot of different scraps of paper containing the name of everything you want to get at the store. You can just carry the list. And lists can change - you can cross something off a list, add something to a list, or replace one element with another. So how can we translate the efficiency and usefulness of a list to coding? Simple: we use an array.

**Ask students to take thirty seconds to write down a few items they want to buy at the grocery store (or at Target, if you want more options). Then, ask students to share out a few while you make a list on chart paper/white board.** Aim for the list to be \~10 items long. Title the chart paper **groceryList** and then explain to students that this is essentially an array - it's a list of objects that, paper permitting, could be as long as the want it to be, and have a certain and specific order.

Explain to students that this groceryList has an order that is defined by something called an _index_ value, or the number we give to each element. Computers are interesting in that they start indexing at **zero** instead of **one**, like we may be used to. **On the chart paper, number each item 0 - however many items you have.** Then give this scenario to students: _You're shopping with a parent and have a lot to get - they could hand you the list, or tell you 'go get bread,' but they could also say 'Go get item 2. Go get item 0' etc. If I asked you to go get item 1, what would you come back with? What about item 4?_

Ask a few rounds of these questions, taking student answers and asking them to explain. Using 1 and 0 may trip up students which is perfectly natural - just review and make sure they understand the numbering system used in JavaScript!

Once students have done a little practice, it's time to turn this example into code before moving to example 2. Ask students to open a blank editor and code along the following, using whatever you wrote on your chart paper as a model:

```
var groceryList = ["bread", "orange juice", "pasta", "rice", "beans",
"pizza", "bananas", "coconut", "potatoes", "spinach"]
```

Explain the pieces needed to make this array. By now, you should understand what a variable is. It’s a name that you give to a piece of data or information. You can change the value of the variable, but the name will always stay the same. With arrays, we can store many separate values in one variable name. To indicate that a variable holds an array, we put all of the items inside square brackets, with each element separated by a comma.

Please note for students: the elements in this array are strings, or letter characters all put together, which is why they are in quotation marks. If we were storing numbers, p5.js colors, or other specific data types, the quotations wouldn't be needed!

Once the array is in your code, review with students how you can **call** items of an array using the **array name** and the **index value.** You can do this either with console.log() or text(), depending on your preference and what works best for your classroom.

```
var groceryList = ["bread", "orange juice", "pasta", "rice", "beans",
"pizza", "bananas", "coconut", "potatoes", "spinach"]

function setup() {
  createCanvas(400, 400);
  console.log(groceryList[0]) //console.log option
}

function draw() {
  background(220);
  text(groceryList[3], 200,200) //text function option
}
```

Run a few times, changing out the index value each time. Before running, always ask students to predict what will display. Once they feel comfortable, it's time to hit them with another example!

### What are arrays? Building Example (15 min)

Since arrays are a whole new code concept, we like to give students a few ways to process them in hopes that one will resonate and stick around in their brains. Explain to students that you are going to put the grocery list aside for a moment and think about arrays in a different way.

Think of variables and arrays like buildings. Let’s say you want to count the number of people on each floor of a building. If the building only has one floor, it’s easy, right? You can just say “The building has 30 people in it.” But if we’re thinking about the Empire State Building, it’s harder than that. You need to find a way to talk about the number of people on each floor of the Empire State Building.

So how would you say that in real life? You’d probably say something like “There are 20 people on the first floor, 30 people on the second floor, 32 people on the third floor…” and so on. And we all know you’re talking about the same building, the Empire State Building, you’re just referring to each floor separately.

So you can think of an array as something similar. It’s a bunch of different values, but with the same name. And we write it in a similar way as we would talk about buildings with floors. If we had a variable that held the number of people on the ground floor of a single-story building, the declaration might look something like this: var building = 30;. But if we’re talking about a building with many floors, our array might look like this: building\[0] = 25; building\[1] = 40, building\[2] = 30;.

Notice the ‘\[ ]’ after the name of our variable? That’s where we put the index, or number, of the element, or specific value within the array, that we want to access or change.

![Image of simplified building with floor numbers labeled and people on each floor.](<../.gitbook/assets/Screen Shot 2021-12-15 at 11.31.21 AM.png>)

Using the syntax, and assuming this is the building we’re talking about, what would building\[3] be equal to? What about building\[1]?

You may have noticed something weird. When I was declaring values in the array, I started with building\[0]. Why did I do that, and not start with building\[1]? Because in p5, arrays are zero-indexed, which means they start at zero. Think of it like a building that counts the ground floor as zero and starts counting at one after you’ve gone up a floor.

If we wanted to make an array that held the amount of people per building floor, it might look like this:

```
var buildingPop = [50,0,20,40,10]
```

...and we could then call those numbers in our program to control whatever we wanted!

### Color in Arrays && Practice

After all of those examples, it's time to see one last application of arrays - this time instead of numbers or strings, let's try putting colors into an array. For this activity, we are going to imagine we are making a color palette for a design project (something that graphic artists, fashion designers, and even event planners have to do often) using [Adobe Color Picker](https://color.adobe.com/create/color-wheel).

[Share students on this starter code](https://editor.p5js.org/cmorgantywls/sketches/tBzRpplfn). Then demonstrate Adobe Color Picker and select a palette of your choosing. With students, show them how they could create and use an array of colors via the following code along. Note: the color() feature is p5.js specific (it is essentially creating a color object) and so this array, while the variable still needs to be declared globally, above setup, must be given values _inside_ the setup function for the colors to register. Creating the array would look like this:

```
var palette1;

function setup(){
 createCanvas(400,400)
 
 palette1 = [color(252,214,202), color(217,138,124), 
 color(240,101,89), color(219,117,116), color(255,28,82)]
}
```

You would then use the colors as we have called other items in the array. Students will need to choose primary and secondary/accent colors based on the palette they create:

```
fill(pallete1[2])
rect(10,50,200,50)
```

### Wrap Up

Ask students to post their project links in a forum such as Slack or the Google Classroom. Then, have them view and comment on two other projects, leaving a glow and grow for each

Guiding questions:

1. How are arrays useful?&#x20;
2. Describe how to can an array be used on p5.js?
