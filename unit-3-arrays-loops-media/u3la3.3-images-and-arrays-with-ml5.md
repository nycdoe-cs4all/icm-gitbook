# U3LA3.3: Images and Arrays with ml5

### Overview && Teacher Feedback

In this learning activity, students will use p5 and ml5 to put images into an array and apply that array to a machine learning model. Training models from scratch is well above the scope of this course, so most of that is given in a code along - students will then have a chance to form a hypothesis about their model and test it with images of their own. While this lesson can take place in the p5 editor, more powerful IDEs such as repl.it have slightly faster response times.

This project uses p5 and continues in Javascript, but also uses a new library called **ml5.** **ml5 is a machine learning library that has been built from Tensorflow.js so that it’s easier for newbies to use, like you and your students!** This can work right in the p5 editor, although we have found that the programs run _slightly_ faster on a more powerful IDE, such as repl.it. If you'd like to expose students to a new working tool, this would be a great time.

repl.it offers support in many languages and also allows students to code together in one project simultaneously (similar to how they would work in a Google Doc or similar). Students may have used this site in previous classes, or to work in other languages.

This project can be made much longer or shorter depending on your personal preferences. In the shortest version of this lesson, students should gain a basic understanding of machine learning, complete the code along, and then form and test a hypothesis about the model. In a longer form, take a detour with your students to give them more background on machine learning and some of the bias that exists within it by exploring some articles/videos to give them a better understanding. It’s important students understand that machine learning itself is not inherently evil or bad, but because the people training the models come with their own bias, it passes along to the AI.

* _Two periods would involve moving very quickly through the ml5 process and creating the p5 program & hypothesis._&#x20;
* _Four periods would allow you to devote more time to the social implications of machine learning._

### Objectives

**Students will be able to:**

* Use an array to store images&#x20;
* Understand the basics of machine learning&#x20;
* Create a program that will select and identify an image using MobileNet

### **Suggested Duration**

2-4 45 minute periods

### **Blueprint Foundations Student Outcomes**

#### **Algorithms**

* Explain the positive and negative impacts of an algorithm’s design on my family or my community.&#x20;
* Describe how instructions can have different outputs depending on inputs.

**Prototype**

* Experiment with the commands of a programming language.

### **Vocabulary**

* Machine learning - an application of artificial intelligence (AI) that provides systems the ability to automatically learn and improve from experience without being explicitly programmed&#x20;
* Artificial intelligence (AI) - training a computer to do something humans would identify as thinking&#x20;
* Bias - prejudice in favor of or against one thing, person, or group compared with another, usually in a way considered to be unfair. Bias can be personal or a part of great social systems of power and oppression.

### **Planning Notes**

|                                                                                         Planning Notes                                                                                        |                                              Materials Needed                                             |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------: |
| <p>Familiarize yourself with the code in advance, and select which editor you would like to use!<br><br><strong></strong>You might also want to play around with various examples in ml5.</p> | Optionally: copies of select articles on machine learning, or determine strategy to distribute digitally. |

### Resources

#### [ml5js ](https://ml5js.org)- a simplified machine learning library in javascript

* [Image Classification](https://ml5js.org/docs/image-classification-example) - the ml5 example this lesson is adapted from. It works heavily with HTML - we’ve transitioned the HTML elements to p5 to match course knowledge and make the classifier more interactive.

#### Starter Code

* p5 Editor: [Completed Code](https://editor.p5js.org/cmorgantywls/sketches/eLJZwn4k1) | [Pre-Code Along](https://editor.p5js.org/cmorgantywls/sketches/Z-4B-hysn)
* repl.it: [Completed Code](u3la3.3-images-and-arrays-with-ml5.md#overview-and-and-teacher-feedback) | [Pre-Code Along](https://replit.com/@cmorgantywls/u3la33-images-and-arrays-with-ml5-Pre-Code-Along#sketch.js) (If you'd like to try repl.it but are unfamiliar with the site, you can [learn more here.](https://repl.it/site/docs/misc/free-features))

**Lesson Resources**

* [Google Duplex Schedules a Hair Appointment ](https://soundcloud.com/alexismadrigal/google-duplex-calling-a-restaurant)- a great brain starter!
* [How Machines Learn](https://youtu.be/R9OHn5ZF4Uo) (Youtube Video)
* [Hypothesis Note Catcher](https://docs.google.com/document/d/1jA3hVbwyYhSE4WCoci72dkoBg9WU9MYKHP2WgGdtKDc/copy) (Google Doc)

**Additional Readings on Machine Learning && Bias**

**NB:** _These articles were selected when this lesson was originally written, but machine learning is being used in new technologies developed every day. If you choose to extend this lesson to a deeper discussion of machine learning and algorithmic bias, it is worth doing some light googling to try and find contemporary articles that point out the benefits and harms of this technology._

_If you notice yourself getting paywalled by any of these (or just need to print a neat, clean version) consider typing 'outline.com/' before the URL. This will remove many ads and payblockers for easy printing/reading. If you are still troubled by a paywall, consider temporarily disabling JavaScript for a webpage by clicking the lock next to the URL, followed by site settings, and then disabling JavaScript._

* [Algorithmic Justice League ](https://www.ajlunited.org)
* [Machine Bias ](https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing)- software used across the country to predict future criminals is racist.&#x20;
* [Man Against Machine: AI is better at diagnosing skin cancer than dermatologist ](https://www.sciencedaily.com/releases/2018/05/180528190839.htm)
* [AI Could Worsen Health Disparities ](https://www.nytimes.com/2019/01/31/opinion/ai-bias-healthcare.html)
* [Can Computer Problems Be Racist and Sexist? ](https://www.npr.org/sections/alltechconsidered/2016/03/15/470422089/can-computer-programs-be-racist-and-sexist)
* [Tay Chatbot becomes racist ](https://www.theguardian.com/technology/2016/mar/24/tay-microsofts-ai-chatbot-gets-a-crash-course-in-racism-from-twitter)
* [Artificial Intelligence and Racism ](https://techcrunch.com/2016/04/15/artificial-intelligence-and-racist/)
* [Experts are trying to make machines be “moral”](https://alumni.berkeley.edu/california-magazine/just-in/2015-06-08/good-bad-and-robot-experts-are-trying-make-machines-be-moral)

### Assessments

Machine Learning Hypothesis & Justification

### Do-Now/Warm-Up (5 minutes)

Ask students to:

Listen to [this recording](https://soundcloud.com/alexismadrigal/google-duplex-calling-a-restaurant) and tell me what you think is happening.

_Be sure not to display the title for students - play it without any context, then ask students to share their thoughts. After they share, reveal that while this was someone scheduling a hair appointment with a salon, that someone was actually a robot. Ask students to explain how they think someone could teach a robot to do this (look for answers beyond saying ‘code’ or ‘they programmed it’)_

### What is Machine Learning & How do Machines Learn?

Introduce students to the idea of machine learning as an important part of AI - it’s AI with the goal of getting computers to learn and adapt based on information they are fed through a model and training sets given by a programmer.

From there, watch [this video](u3la3.3-images-and-arrays-with-ml5.md#undefined) as a class.

Be sure that students understand that machine learning does not mean you are creating an all-knowing being, especially because you the model created by the programmer may be flawed.

You may want to act out an example with students; ask a student to imagine that you are teaching them, the computer, to recognize images. Show them a few images of an animal and each time purposefully say the wrong thing, like 'toad' when you are looking at a butterfly. Ask the class: what is student going to call this (display butterfly) whenever they see one? Why? (Remind students that while this is true of computer learning, it's also true of how children learn - if we could lock a kid in a room where no one could change their mind and teach them that butterflies are called toads, that's what they would call them, too!)

### Where We See Machine Learning (\~25 - 35 minutes)

**NB:** _If you are choosing to shorten this lesson, this is a lengthy activity that can be shortened to a brief discussion. The brief discussion would involve you summarizing some of the article material (rather than having students read) and bypassing the Chalktalk protocol - it's up to you based on your own pacing needs and the needs of your classroom!_

Break students into groups and give them each a different article on machine learning. Ask them read (or skim - some are length) to summarize and then pull out key points from the article. Then have students complete a Chalk Talk activity where they circulate the room (silently!) and respond to questions posted on chart paper by writing on the chart paper or post-its. Students can respond to each others’ writing with more writing, and then at the end, will come together to share out what they thought and noticed from reading the responses.

Some ideas for questions:

* What are some flaws we see in machine learning and AI?&#x20;
* Why do we think machine learning has a bias? What could be done to improve machine learning models?&#x20;
* Has biased machine learning models impacted your life? How?&#x20;
* If no one addresses the issues in machine learning and AI, what effects could it have on our future?&#x20;
* What questions do we still have in regards to machine learning?

### Using a Basic Machine Learning Model (\~10 - 20 minutes)

This is the moment that really teaches a coding skill - and there are a few different ways to do that!  The big code-skill takeaway from this lesson is to teach students that images can be placed in arrays, but that's not actually a terribly difficult or far removed skill from what they were doing before, so they will not miss anything with either option. Choose the one that _you_ are most comfortable delivering and you think will best hold your students attention! Additionally, please make sure by this point you have made a decision about if you will be continuing in the p5 editor or swapping to repl.it for this lesson.

#### Option 1: Distribute Completed Code

Ask students to duplicate ([p5 editor version](https://editor.p5js.org/cmorgantywls/sketches/eLJZwn4k1)) or fork ([repl.it version](https://replit.com/@cmorgantywls/u3la33-images-and-arrays-with-ml5-Complete-Starter-Code#index.html)) the completed image classifier code. Even though this is finished code, it's important to stress to students that reading code is still an important way to learn.

Begin by having students take 3-5 minutes to silently read through the code in the sketch.js file (and also in the index.html, if you think it will be helpful) and leave comments on as many lines as possible. The comments can be noticings, wonderings, or responses to the following questions:

1. What is familiar about this code?
2. What looks new?
3. Where do you see images being loaded and used?
4. How are arrays being used here?

Once they have had enough time to meaningfully engage with the project, do a few rounds of sharing as you point out pieces on the screen. Be sure the following have been covered:

* The images are all placed in an array by their name, and loaded in the setup (and mouseReleased)
* mouseReleased allows the image to reset whenever you are done dragging the slider.
* The image call in places takes from the array of images, sometimes with slider value, and sometimes with a hard coded value.
* There are a lot of similarities to past projects we've done, and some new things from ml5, but none of this should like too scary.

#### Option 2: Code Along

Ask students to duplicate ([p5 editor version](https://editor.p5js.org/cmorgantywls/sketches/Z-4B-hysn)) or fork ([repl.it version](https://replit.com/@cmorgantywls/u3la33-images-and-arrays-with-ml5-Pre-Code-Along#sketch.js)) the pre-code-along starter code.

From here, you are essentially working to make this version look like the completed version by doing the following with the class:

1. Create an array that can hold your images
2. Select from the array, first manually by changing the code, and then by using the slider.
3. Adjust slider value to be based on the length of the array
4. Review the code in mouseReleased to allow the slider to choose the image

Rather than provide answers here, please reference the completed version to determine what the final product should look like once these four tasks are addressed. (This is also a good litmus test for which option you should do with your students - if this feels overwhelming, best off with option 1!)

### Hypothesize on the Model (15 - 30 minutes)

Explain to students that their Image Classifier is built-in ml5 and running the MobileNet model. MobileNet is a simple model that has been trained off of tons of free and open-source pictures so that we can use it for educational projects like this.

Now, there are scholarly articles out there explaining exactly how MobileNet was trained and what it's good at; but rather than search through those, we are going to let the model itself demonstrate to us by testing it with more images. With what students have seen in the example, and what they know about AI, ask students to form a hypothesis with their partner about the model. This could be about what it will or will not be able to identify, the type of language it will use, or the confidence it will have identifying certain things in images. Some examples are:

* “I predict that people with green hair will be identified as trees by the model in 10 out of 15 trials.”&#x20;
* “I predict that the model will correctly identify birds with a 20% higher rate of confidence than dogs.”&#x20;
* “I predict that, based on the data it has seen, the model will not be able to correctly identify mice with more than 30% accuracy.”

Once students have decided on a hypothesis, they should find numerous images that serve as examples and counterexamples to load into their program, put into the program and array, and test, test, test! If it is useful, [consider using this note catcher worksheet. ](https://docs.google.com/document/d/1jA3hVbwyYhSE4WCoci72dkoBg9WU9MYKHP2WgGdtKDc/copy)

To test your hypothesis, you will need to find multiple images that you will load into your program and put into the array. You will probably want to find examples and non-examples for your model - if we are testing if the model is better at recognizing birds than at recognizing dogs, I will want to find images of both.

Remember, the model likes things without a busy background, so keep that in mind for accurate results.

It's also important to note for students that they are not being graded on if their hypothesis is correct or not. Even a hypothesis that goes entirely wrong (for example, a model that does not recognize BTS or Charlie D'Amelio) can still give them information about what the model _doesn't_ do, which is just as valuable as what the model DOES do.

Once you’ve updated your program and tested your model, answer the following:

* Summarize your results!&#x20;
* Was your hypothesis accurate? Why do you think this? (Use data from your predictions to back up your answer!)&#x20;
* How could this model be retrained to give better results?

### Wrap Up

Students will hopefully come to some interesting conclusions and should be given the opportunity to share.

It’s the teacher’s choice if this share out is informal or formal (a presentation, a poster, a program, etc), but encourage students to back up their answers with data from the program.

### Extensions

Ask students to reach out to organizations that have biased machine learning algorithms and express their opinions about it!



