# Quiz #1

## Instructions

1. Fork this repo
2. Clone your fork
3. Fill in your answers by writing in the appropriate area, or placing an 'x' in
the square brackets (for multiple-choice questions).
4. Add/Commit/Push your changes to Github.
5. Open a pull request.

## CSS

### Question #1

Describe the purpose of a clearfix in CSS, and give an example of how to do it.

Your Answer:
```text
Non-floated elements can't 'feel' floated elements. As such, when we have the
two types near each other, we may experience 'bugs' in our layout. Examples:
* a non-floated container with a border will not adjust its height correctly to
  surround floated elements inside of it. (i.e the border will collapse)

A common clear fix is:

.clearfix {
  overflow: auto;
}
```

### Question #2

What does the following selector do?  `ul.dropdown > li`?

Select 1:
```
[x] Selects all li's which are directly inside a ul of class dropdown (children)
[] Selects all li's which are anywhere inside a ul of class dropdown (any descendant)
[] Selects all ul's of class dropdown, as well as the children elements that are li's
[] Selects all ul's of class dropdown, only if their children are exclusively li's
```

See here: [css selector references](http://www.w3schools.com/cssref/css_selectors.asp)

## Scope/Context/Closures

### Question #3

Describe the rules of scope in JavaScript.

Your Answer:
```text
Variables created without the var keyword, no matter where in a program, are placed in the global scope.
Variables created with the var keyword are created in the current local scope.
All functions (and only functions) create a new local scope.
The current scope includes all outer (enclosing) scopes.
```


### Question #4

Define an object and store it in a variable `pizza`. The object should have 2
properties: a temperature (set to 70), and a method called `bake`. When called,
this method should set the pizza's temperature to be 300. Note: you may not use
the variable pizza inside your method.

Your Answer:
```js
// write code here
var pizza = {
  temperature: 70,
  bake: function() {
    this.temperature = 300;
  }
};
```

## Callbacks

### Question #5

**Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, thing to do should invoke the function given as an
argument. Finally, demonstrate calling `doSomething` with a function.**

Your Answer:
```js
// write code here
function doSomething(thingToDo) {
  thingToDo(); // call the function passed in, using parenthesis
}
```

### Question #6

**What is the difference between synchronous and asynchronous program execution?**

Select all that apply:
```
[] Synchronous code runs at an even pace, asynchronous code runs with uneven pacing.
[] Synchronous code runs all at the same time, asynchronous code runs completely randomly
[x] Synchronous code runs in order (as appears in the source), asynchronous code may run at a later time.
```

Common examples include `setTimeout` and `setInterval`, or event listeners,
where the code runs a set amount of time later, or, in the case of event
listeners, when an event happens (like a user clicks a button).

## Git

### Question #7

Which of the following represents a correct workflow for submitting a PR on a non-master branch?
(ignore the lack of commit messages)

Select 1:
```
[x] fork on github; git clone <fork_url>; git checkout -b <charlie_solution>; git add <files>; git commit; git push; create pull request
[] fork on github; git clone <ga_dc_url>; git checkout -b <charlie_solution>; git add <files>; git commit; git push; create pull request
[] git clone <ga_dc_url>; git branch <charlie_solution>; git add <files>; git commit; git push; create pull request
[] fork on github; git clone <fork_url>; git checkout -b <charlie_solution>; git add <files>; git commit; git pull; create pull request
```

Option #2 is wrong because it clones the wrong url.
Option #3 is wrong because it doesn't involve forking.
Option #4 is wrong because it pulls instead of pushing.


## jQuery

### Question #8

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[x] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`
[x] `$(".post").html()`
[x] `document.getElementsByClassName("post")[0].innerHTML`
[] `document.getElementsByClassName("post").innerHTML`
```

Option #2 mixes jQuery elements and vanilla JS methods (innerHTML)
Option #5 fails because the selector returns an array, and you can't call innerHTML on an array


### Question #9

Using jQuery, add an event listener for clicks on the button with the id
'greeting'. When the event happens, the code should append a paragraph to the
body, that says "hello".

Your Answer:
```js
// your code here
$('#greeting').on("click", function() {
  $('body').append("<p>hello</p>");
});

// ORRRRR

function addParagraph() {
  $('body').append("<p>hello</p>");
}

$('#greeting').on("click", addParagraph);

```

## Software Development Processes

### Question #10

Create a repo for project 1. (You don't need to fork, just create a brand new repo).

Create a readme.md in that repo. In the readme, write out five (5) user stories for your first project. Be sure to include a
role, goal, and reason for each.

Finally, link to your repo on github in the space below.

Your Answer:
```text
Example user stories for tic tac toe:

* As a user, I want to click squares and see my letter, so I can play.
* As a user, I want to switch turns, so I can play with another person next to me
* As a user, I want to see a notification when I click on a square that's already taken, so I know if I clicked in the wrong place
* As a user, I want to be told when a user has won, so I know when to stop playing.
* As a user, I want to reset my game (new game state), so I can play again.
```
