# Constructors, Prototypes and _this_

## JavaScript Fundamentals

## Objectives

- explain the four principles of the 'this' keyword and demonstrate each explanation with an example of their uses
Answer:
1. Whenever a function is contained in the global scope, the value of this inside of that function will be the window object.
Example:

function greeting(name) {
    console.log('Hello ' + name);
    console.log(this);
}

greeting('Rafiullah');

2. Whenever a function is called by a preceding dot, the object before that dot is this.
Example:
var greetMe = {
    greeting: 'Hello ',
    speak: function(name) {
        console.log(this.greeting + name);
        console.log(this);
    }
}

greetMe.speak('Rafiullah');
3. Whenever a constructor function is used, this refers to the specific instance of the object that is created and returned by the constructor function.
Example:
function GreetMe(name) {
    this.greeting = 'Hello ';
    this.name = name;
    this.speak = function() {
        console.log(this.greeting + this.name);
        console.log(this);
    }
};

var greetJohn = new GreetMe('John');
var greetJane = new GreetMe('Jane');

greetJohn.speak();
greetJane.speak();
4. Whenever JavaScript’s call or apply method is used, this is explicitly defined.

- describe, and use prototypes, constructor functions the new keyword, and pseudo-classical inheritance to build objects
Answer:
A prototype is an existing inbuilt functionality in JavaScript. Whenever we create a JavaScript function, JavaScript adds a prototype property to that function
This keyword is simply refer to object when we call on it. 
A constructor is any function which is used as a constructor. The language doesn’t make a distinction. A function can be written to be used as a constructor or to be called as a normal function, or to be used either way.


## Introduction

In order to complete these tasks you will need your newly aquired knowledge of constructor functions, prototypes, and the `this` keyword.

## Instructions

### Task 1 - Set up Project

Two options are included below.

<details>
  <summary>1. Using Code Sandbox</summary>

  * Launch the sandbox using the link below.
  * Sign into Code Sandbox.
  * Fork the sandbox.
  * See your tests running on the "Browser" tab (NOT the "Tests" tab).
  * The way you'll submit your work will be by pasting a link to your fork into the submission form.

  [LAUNCH ON CODESANDBOX 🚀](https://codesandbox.io/s/github/LambdaSchool/JS-Exercise-Prototype?previewwindow=browser)

  <img alt='instructions Code Sandbox' src='./instructionsCodeSandbox.png'>
</details>

<details>
  <summary>2. Using VSCode and the Command Line</summary>

  1. Fork repo and add TL as collaborator on Github.
  1. Clone _your_ fork (not Lambda's repo by mistake!).
  1. `cd` into your newly cloned repository.
  1. Create a new branch by typing `git checkout -b <firstName-lastName>`.
  1. Install dependencies by typing `npm install`.
  1. Run tests by typing `npm run test:watch`.
  1. Work on your branch, push commits and create PR as usual.
  1. Make sure to commit often!!

  <img alt='instructions VSCode' src='./instructionsVScode.png'>
</details>

### Task 2a - MVP

Find the file `index.js` and complete tasks 1, 2 and 3 until all of your tests pass.
There is an additional task 4 which requires written explanations and has no tests.

If you run into trouble while coding, fight the good fight for 20 minutes and then get on the help channel. __Remember to formulate your help request in a professional manner__ - like you would at the job - by including error messages, screenshots, and any other pertinent information about the problem, as well as what things you have attempted already while trying to solve it.

### Task 2b - Exit Ticket

Once you begin, you will have 15 minutes to answer the questions [here](https://app.codesignal.com/public-test/bvaz9NW52Asuc8DGZ/LK7SEZ9FcLpjgj).

The completion of these questions is mandatory for MVP. However, passing the quiz doesn't affect your standing as a Lambda School student whatsoever. This is Lambda School testing itself! Please answer honestly and to the best of your ability without using external references.

### Task 3 - Stretch 

There are stretch goals found throughout `index.js`. Do not start work on these until you have finished MVP. 

## Submission format

Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your team lead as a reviewer on the pull-request
- [ ] Your team lead will count the project as complete by merging the branch back into master.
