---
title: "Closures, Scope and All the Good Stuff About Javascript"
date: 2020-09-05T21:05:11+02:00
draft: false
tags: ["interview-prep", "javascript"]
---

## Objectives

This article was written to help explain a topic which is an interview staple for Javascript developers.
Based on the assumption that the reader is a total newbie to the topic, we will start from the very basics and incrementally build up on our knowledge. Hopefully by the end of this article you will have a solid understanding of closures.

## Prerequisites
 - <a src="https://nodejs.org/en/download/" class="article-link">Nodejs</a> installed locally.
 - Text editor of your choice.

## Key Concepts

### Variable

A variable in Javascript is an entity that is used to refer to data stored in memory. You declare a variable in your script by giving it a name, which is preceded by a mandatory keyword which can either be _let_, _const_ or _var_ and assigning it a value. Assigning an initial value is optional for any variable preceded by keyword _let_. All _var_ and _let_ variables can be reassigned values whereas _const_ variables are immutable once declared and initialized.

 <img src="https://res.cloudinary.com/di70zcupa/image/upload/v1599441833/js-closures-tut/Defining_variables_in_JS_1_uom50u.png" alt="Defining variables in Javascript">

_To learn more about variable declaration, initialization,  data types and hoisting check out this <a href="https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables" class="article-link" target="_blank">link</a>. It contains resources published by <a href="https://developer.mozilla.org/en-US/" class="article-link" target="_blank">mozilla (MDN)</a>._

### Block

A block (_or compound statement in other programming languages_) is used to group statements in javascript. The boundaries of a block statement is a pair of curly brackets.

<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1599461896/js-closures-tut/Block-Syntax_1_waqhf3.png" alt="Block Syntax">

On that basis of the given definition of a block, it follows that _functions_, _if statements_, _loops_ all have block statements.

### Local and Global Variables

 In Javascript variables are either declared inside a block or independent of a block. When a variable is declared inside a block it is _local_ in reference to that block. A global variable is one whose scope is global.


## What then is scope ?

In Javascript scope denotes the reach or range or accessibility of Javascript variables. So, whenever a javascript variable is declared it automatically has scope associated with it.

The scope of a variable is determined by:
-  where a variable is declared within a script and,
-  its type i.e _let_, _const_ and _var_.


### Types of scope

1. Global scope: globally scoped variables are accessible throughout the window object or globally within your script.

2. Block scope: block scoped variables are variables that when declared inside of a block are only accessible within that block. The block referenced to, being a _generic block_ or a block which is part of a _loop_ or an _if statement_ or a _function_. So essentially _const_ and _let_ variables can either be _globally scoped_ if declared outside of a block or _block scoped_ when declared inside of a block. When _var_ variables are declared in blocks which aren't functions, their scope is global.

In the screenshot below I declared a couple of variables, I suggest you go to your text editor and create a _main.js_ file and copy the contents of the screenshot and modify them to your liking.
<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1599466095/js-closures-tut/scope-example_ghtmaq.png" alt="Illustrating scope in Javascript">
Now to execute _main.js_ file, type the command below in your terminal:

```
node main.js
```
The expected results are shown in the screenshot below:
<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1599467585/js-closures-tut/scope-terminal_result_o3dz6n.png" alt="Results on the terminal">
The variables _name_, _lastName_ and _isSoftwareDeveloper_ are declared independent of a block. These are known as global variables and they have global scope. 
Variables _hobbies_ and _countryOfResidence_ are local to a block in which they were declared but, although _hobbies_ has global scope  _countryOfResidence_ is block scoped.



3. Functional Scope: functionally scoped variables are variables that when declared inside of a function they are only accessible within that function, if the same variable was declared in any other block e.g. an _if statement_ and it was accessible only within that block as well. Its scope is then described as being block scoped. So essentially _functional scope_ is a special type of _block scope_ used to describe the scope of _var_ variables declared inside functions. A _var_ variable is always globally scoped otherwise it is _functionally scoped_ if declared inside of a function.

<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1600108316/js-closures-tut/functional_scope_wflflh.png" alt="Functional scope examples">

4. Lexical Scope: given a scenario where we have a group of nested functions, lexical scope means that the inner functions have access to the variables and/or resources of the outer function even after the outer function is returned.

<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1600118955/js-closures-tut/lexical_scope_c8rcm4.png" alt="Lexical scope example">

## Finally, what then are closures ?
To truly understand closures we need to have a basic understanding of how the Javascript engine executes functions. So, whenever a function is invoked an execution context associated with the function is created. An execution context contains meta data about the function and all its associated variables. Upon execution of the function all the meta data associated with the function is then removed from the memory, what is often refereed to as garbage collection.

>Closures are functions which have references to variables in their lexical environment.

Let's reconsider the screenshot provided above, when the file is executed internally what happens is that, the javascript engine parses _main.js_ line by line. When it reaches the point in the script where the _outer_ function is invoked it creates a context associated with it. When the javascript engine eventually executes the _inner_ function is creates an execution context associated with it as well. Now as it was verified above, the variables of the _outer_ function are always accessible inside the _inner_ function, even when the outer function's execution context has been removed from memory. Let's see how that is possible:

<img src="https://res.cloudinary.com/di70zcupa/image/upload/v1600121543/js-closures-tut/closures_bdxhjn.png" alt="Closures example">

So, we have seen that when the _inner_ function (which is a closure) is invoked its execution context's contains a reference to the _outer_ function's variables, despite the fact that the _outer_ function has already been returned.

_It is my hope that this article has helped you understand closures in javascript._

_Happy Coding  😉!!!_