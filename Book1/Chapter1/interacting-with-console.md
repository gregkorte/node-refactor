# User Interaction in the Console

Learning Objectives:
1. `console.log()` and `readline`
1. declaring variables with strong types
1. string interpolation
## Hello, World!
Take a look at the code that was created by the template:
```ts
console.log("Hello, World!");
```

When we ran this code in the last chapter, the program printed "Hello, World!" to the terminal and ended the program (console and terminal mean the same thing for these purposes). You've interacted with the console in your browser when you ran JS code in it, and this is the same, but your terminal is the console for this program, because the program is running in your terminal, not in the browser.

1. Change the program so that it prints "Welcome to Thrown for a Loop!" to the terminal instead of "Hello, World!".

1. Use another `console.log()` to write a second line to the terminal that says "Please choose an option: ", and run the program again.

## Declaring and initializing variables
Because JS is a _dynamically_ typed language, one variable can hold many data type values. Therefore, this code is perfectly valid:
``` js
let theMeaningOfLife = 42
theMeaningOfLife = 'forty-two'
console.log(theMeaningOfLife)
```

`theMeaningOfLife` is _declared_ with the `let` keyword, and then _initialized_ with a value of `42`. This code says "create a changeable variable called `theMeaningOfLife` and give it an initial value of `42`. Then, change the value of `theMeaningOfLife` to `'forty-two'`, and print that to the console." Javascript does not care that the first value of `theMeaningOfLife` was a number, but was changed to be a string.
<br>

Let's look at some similar TypeScript code:
```ts
const theMeaningOfLife: string = "forty-two");
console.log(theMeaningOfLife);
```

What's different? We still use `let` or `const`, but we also declare a variable with a type - in this case, string. This tells the compiler that theMeaningOfLife will only ever hold string values, or undefined (the default value for a string - more about default values later). As a result, we cannot reassign theMeaningOfLife with a value of 42, because 42 is a number. This is what it means for TypeScript to be strongly typed. Variables are assigned a type when they are declared, and that type does not change.
```ts
let theMeaningOfLife: number = 42;
theMeaningOfLife = 'forty-two'; // Error: Argument of type 'string' is not assignable to parameter of type 'number'.
console.log(theMeaningOfLife);

```

Add a line at the top of `index.js` that stores the program greeting in a variable. Then, _reference_ that variable in the call to `console.log()`:
```ts
const greeting: string = "Welcome to Thrown For a Loop";
console.log(greeting);
```

## Making our program interactive
If we want to make a multi-line string, we can use backticks (`). This is called a template literal, and its other features are not important right now.

Let's make our greeting a bit more descriptive:
```ts
const greeting: string = `Welcome to Thrown For a Loop
Your one-stop shop for used sporting equipment`;
console.log(greeting);
console.log("Please enter a product name: ");

```

### `readline`

We've asked the user to provide input, but we haven't collected any yet. To do that, we can use `readline`, but we must import it first. The `readline` module is a built-in module, which means it comes pre-installed with Node.js itself. Therefore, you don't need to install it separately using npm.

To use the readline module in your Node.js application, you can simply import it using the `require` function.

Add this line at the top of `index.js`.

```javascript
const readline = require('readline');
```

### Create the `readline` interface
Next, we need to create a readline interface `rl` using `readline.createInterface()`. This interface is configured to read input from the `process.stdin` stream (standard input, i.e., user input from the terminal) and write output to the `process.stdout` stream (standard output, i.e., output displayed in the terminal).

```javascript
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});
```

### Processing user input
Then we use `rl.question` to prompt the user with the message _'Please enter a product name: '_. The function takes a callback function as its second argument, which will be executed when the user enters input and presses `Enter`. The `response` will be passed as an argument to this callback function.

Inside the callback function, we log the user's input to the console using `console.log()`. You can perform any further processing of the user input within this callback function. Finally, we call `rl.close()` to close the readline interface, allowing the program to exit gracefully.

```javascript
rl.question('Please enter a product name: ', (response) => {
  console.log(`You chose: ${response}`);

  // Add any further processing of the user input here

  rl.close();
});

```

Run the program to see what it does! You'll notice that the program stops and waits for your input. You can type whatever you want at that point and press `Enter`, and after that the program continues until it is done.

It is possible to use the backticks and `$` symbols together to make a multi-line interpolated string, like this:

```javascript
console.log(`You chose: ${response}.
Thank you for your input!`);
```

Try that as well, and see how it works by running the program.

## ✍️ Reflections
1. A number of terms related to variables were reviewed here, included _declare_, _initialize_, and _reference_. What does it mean to declare a variable? What does it mean to initialize it with a value? What does it mean to make a reference to a variable? Write down some answers to these questions. If you're unsure of your understanding, ask a teammate or an instructor. These are key concepts for your progress as a software developer.
1. In our code, `console.log()` is fairly straightforward, as it simply logs the provided message to the console. However, the `readline` module introduces a different way of interacting with user input. We've reviewed the idea of a method (a special kind of function) returning a value. What does it mean for a function to return a value, and how does that concept apply in our code when we use `rl.question()` to prompt the user for input and `process.stdin` and `process.stdout` to read and write to the terminal?
How do these concepts of returning values and streams play a role in our code, and how do they differ from the simple logging action of `console.log()`? If you're unsure of your understanding, feel free to discuss it with a teammate or instructor.

Up Next: [Conditionals and Loops](./conditionals-and-loops.md)