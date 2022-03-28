---
description: How can I abstract processes for clarity and reuse?
---

# U5LA2.3: Functions with Purpose

### Overview & Teacher Feedback

**This lesson could, if necessary, be considered optional, as it does not build onto the p5.js library, but rather focuses on fundamental JavaScript skills in building functions. Time permitting, we strongly recommend you give it a go with students to stretch their logic muscles and give them a shot at something new!**

All of the sample prompts come from a website called CodeWars where we recommend students practice their code (and submit answers to you by copy/pasting into a Google Form). If you cannot handle using another platform in your class, this could be all done in the p5 editor or any other IDE, but it would lack the benefit of having the sample testing for students to know if they were correct or not.

### Objectives

Students will be able to…

* Write algorithms to define a function given a prompt&#x20;
* Collaborate with peers to create algorithms&#x20;
* Test and edit their algorithms until a correct answer is reached

### Suggested Duration

45 minutes - 90 minutes (1 - 2 class periods)

The time for this is dependent on how much you would like students to practice and dig into this content. One period is enough for them to solve 1 or 2 challenges, generally.

### NYS Standards

**9-12.CT.4** Implement a program using a combination of student-defined and third-party functions to organize the computation.

**9-12.CT.5** Modify a function or procedure in a program to perform its computation in a different way over the same inputs, while preserving the result of the overall program.

**9-12-CT.9** Systematically test and refine programs using a range of test cases, based on anticipating common errors and user behavior.

**9-12.DL.1** Type proficiently on a keyboard.

**9-12.DL.2** Communicate and work collaboratively with others using digital tools to support individual learning and contribute to the learning of others.

### Blueprint Foundation Student Outcomes

**Abstraction, Decomposition**: Ideas, problems, or projects are broken down into component parts to set the stage for deeper analysis.

**Abstraction, Pattern Recognition:** Decomposed component parts are examined to find patterns like similarities, repetition, conditional relationships, or nested relationships.

**Abstraction, Generalization and Detail Removal:** Component parts are grouped by general characteristics, and unnecessary details filtered out.

### Vocabulary

_No new vocabulary words introduced in this lesson._

### Planning Notes

|                                                                            Planning Notes                                                                            |                   Materials Needed                   |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------: |
| This lesson uses a new platform - please familiarize yourself with it before the start of the lesson so you are aware of how it works on the student side of things! | <p>CodeWars Worksheet (Digital) </p><p>Computers</p> |

### Resources

* [CodeWars Worksheet](https://docs.google.com/document/d/1QmK9lk1sl4DiIpL33qtauk6C6lFki-XpGXSXY3hAGes/copy) (Google Doc)&#x20;
* [CodeWars Website](https://www.codewars.com)

### Assessments

CodeWars Worksheet

### Do Now/Warm Up (\~3-5 Minutes)

**Display on board:** Functions are often used for repeated processes that may have many different inputs and slightly different outputs. Think about technology you use regularly - what is a repeated process that could be controlled by a procedural abstraction like a function? What are the inputs and outputs of this function? What is happening behind the scenes?

_Offer a quick discussion before beginning the lesson_

### CodeWars Demo and Tutorial (\~10-15 minutes)

Ask students to open up their copy of the CodeWars Functions Worksheet. They will need to make an account on CodeWars to start - I recommend doing this as a whole class. Many students will realize the error with the function is it is not returning any values, and can achieve a solution quickly and then create their account.

For students who may struggle, ask them to select the language - which is JavaScript - and then fix the issue in the puzzle they are given:

![Select a language on the CodeWars website](<../.gitbook/assets/Screen Shot 2022-03-18 at 10.07.58 AM.png>) ![Solve the simple puzzle](<../.gitbook/assets/Screen Shot 2022-03-18 at 10.08.25 AM.png>)

The solution just involves putting 'return' in front of a\*b. (Or alternately, saving a\*b to a variable and returning the variable.)

You will walk through the problem under ‘Whole Group Work’ together as a code along. You will notice there are instructions on what the function should do, as well as space to code. They will all see at the start something like:

```
function updateLight(current) {

}
```

Model with students how to plan their code with comments, and then come to a solution together that should look something like this:

```
function updateLight(current) {
  
  if(current=="green"){
    return "yellow"
  }
  else if(current=="yellow"){
    return "red"
  }
  else if(current=="red"){
    return "green"
  }

}
```

Demonstrate that they can test their solution by hitting the 'test' button, which will call it which a bunch of different test cases to see if it works as intended. If it works as intended - all green checks - have them copy/paste their code over to the worksheet and then hit 'attempt.' This will use even more test cases to tell them if they passed or not, and then will direct them on to a congratulations page!

**NB**: _They can retrieve their work after attempting and submitting, but it’s just a slightly more annoying process of clicking around. They will get to see different solutions submitted by other programmers around the world, and there will be a small button where they can just see 'My Solutions.'_

Students may be confused as to why they are coding on this platform. Make sure they understand that this is an IDE just like the p5.js editor, but it is specifically built with all of these test cases that we don’t see. When you solve a problem and hit ‘attempt,’ it runs those many, many tests to make sure your function works in all situations.

### Code Wars Challenges (\~20 - 60 minutes)

After completing the whole group activity, allow students to work with partners or a small group to try to complete as many of the challenge problems as possible. They can select the level they would like to work at and should be encouraged to skip around as needed. (EX: If mild feels very simple, instead of doing both, they should move up to medium.) You can determine the best structures to encourage collaborative work in your classroom!

This section can either last for one class or multiple, depending on how much time you would like to devote to these challenges.

### Wrap Up

At the end of class, consider having students share a solution they are most proud of. Alternatively, you can ask student pairs/groups to create a poster of their prompt/solution (if printers are available) and ask them to answer the following:

* Annotate your solution to explain your reasoning&#x20;
* What are you proud of in this problem?&#x20;
* What gave you trouble in this problem?&#x20;
* Can you think of any alternate solutions, or pieces of code that may be useful in an alternate solution?

Ask students to complete posters have completing a certain number of challenges and then complete a classroom gallery walk.

### Extensions

**This activity is leveled and self-scaffolding.** For students who may race far ahead, ask them to explore CodeWars on their own and find other interesting challenges. For students struggling, encourage them to try writing pseudocode notes that you can look at even if they are not sure how to fully code a solution.
