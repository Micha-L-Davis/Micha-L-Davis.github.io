# Code 401 Reading Notes

1. [Introduction to SQL](code-401.md#introduction-to-sql)
2. [Practice in the Terminal](code-401.md#practice-in-the-terminal)
3. [Get Ready for 401](code-401.md#get-ready-for-401)

---

# Introduction to SQL

In general, relational databases organize data into column-major tables.  These tables can include a column (or several) of unique KEY values. By creating a relationship between the keys on tables we can store related data accross many tables to compartmentalize information for efficient storage. In this way, one can more easily access only the relevant information without having to sort through all the information related to a given key.

The method of querying, creating, modifying and deleting elements of a relational database or its data is SQL, a language that uses plain and simple language to construct potentially complex queries without a heap of technical knowledge.

<img src="exercise1.png" width="200">
<img src="exercise2.png" width="200">
<img src="exercise3.png" width="200">
<img src="exercise4.png" width="200">
<img src="exercise5.png" width="200">
<img src="exercise6.png" width="200">
<img src="exercise13.png" width="200">
<img src="exercise14.png" width="200">
<img src="exercise15.png" width="200">
<img src="exercise16.png" width="200">
<img src="exercise17.png" width="200">
<img src="exercise18.png" width="200">

---

# Practice in the Terminal

The [Bash tutorials](https://ryanstutorials.net/linuxtutorial/) were a good refresher on useful commands for the terminal. I've been using Linux/Unix and Bash on and off for much of my professional career, and before that the first operating system I'd ever used was command-line DOS. So I feel pretty comfortable overall using the terminal to crawl through file and directory trees and do what I need to do.  One thing I noticed that I don't think I've ever had occasion to use is `CTRL + Z`, which I wonder if it might be useful when I want to use the CLI while I'm hosting a server from a terminal rather than killing the server session with `CTRL + C` and then restarting it after I do whatever it is I needed to do.

Also, I appreciate that there's a way to handle spaces in file names but... why would you? Sounds like an invitation to disaster if you ask me.

---

# Get Ready for 401

## Solving Problems

The author of [this article](https://simpleprogrammer.com/solving-problems-breaking-it-down/) suggests a seven-step approach to breaking a problem down and solving it.  Those seven steps are:

1. Read the problem completely twice.  Maybe even 3 or 4 times. Understand the problem before moving forward.
3. Solve the problem manually with 3 sets of sample data. Don't forget to look out for edge-cases and corner-cases along the way.
4. Optimize the manual steps. Find an easier solution, if possible.
5. Write the manual steps as comments or pseudo-code. If you feel you have a handle on the problem, possibly skip this step.
6. Replace the comments or pseudo-code with real code.
7. Optimize the real code, if necessary.

## Act like you make $1000/hr

[ERROR 410 - The Author Deleted this Story](https://medium.com/swlh/pretend-your-time-is-worth-1-000-hour-and-youll-become-100x-more-productive-f04628bb3e6d)

## How to think like a programmer

In [this article](https://www.freecodecamp.org/news/how-to-think-like-a-programmer-lessons-in-problem-solving-d1d8bf1de7d2) the author suggests there are four elements to thinking like a programmer--i.e. focusing on problem solving.  The four elements are:

1. Understand. Like above, the key to solving a problem begins with understanding the essence of the problem in simple terms.
2. Plan. Again, the author suggests that making a plan before you code is the preferred course. This involves modeling inputs and outputs through an algorithm.
3. Divide. Break the problem into sub-problems. By solving each sub-problem you invariably arrive at the solution for the whole problem.
4. Debug/Reassess/Research. If you get stuck, these three approaches can help get past the blocker. Search for flaws in your instructions, check the problem from a new perspective, or get out there and Google up a solution.

## The 5 Whys

The [5 Whys](https://www.mindtools.com/pages/article/newTMC_5W.htm) is a problem discovery technique which is designed to explore the possible causes of a problem and thus lead to potential mitigating counter-measures for any causes that can be mitigated. This technique was developred by Sakichi Toyoda, of Toyota Industries fame, in the 1930's.  It focuses on simplicity, flexibility, and getting first-hand data.

The steps of the process are:

1. Assemble a Team - people with direct knowledge of the issue
2. Define the Problem - make sure there is a concrete understanding of the issue at hand
3. Ask the First "Why?" - discover one or more potential causal factors driving the issue
4. Ask "Why?" Four More Times - drill down with greater specificity following each causal chain to its root cause
5. Know When to Stop - when further questions do not produce useful responses, stop
6. Address the Root Cause(s) - implement the counter-measures
7. Monitor your Measures - guage the effectiveness of counter-measures and refine as necessary

## What the heck is the event loop anyway

The event loop is a system that maintains a queue of asynchronous callback functions requested by the user, and calls those functions into the stack when appropriate. The event loop allows the normal call stack to continue running without becoming blocked by instructions which take a long time to execute.  The event loop queue only dequeues the first callback if the stack is clear, ensuring smooth operation of asynchronous code.

## The Super Mario Effect

The Super Mario Effect refers to the gamification of complicated tasks to enhance learning and retention.  The eponymous example, Super Mario, ultimately boils down to pressing a series of buttons in an exact sequence at the appropriate time--stripped of all other context, this task sounds mind-numbingly boring. But, dressed up as a game with colorful cartoon graphics and loads of positive reinforcement the task becomes highly engaging and the skills are easier to retain.  The presenter demonstrates that this approach to learning can make a large difference in a person's willingness to re-attempt a task after a failure.
