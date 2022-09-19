## JS Basics

1. [Introduction to JS](https://www.coursera.org/learn/html-css-javascript-for-web-developers/home/week/4)

> It's hard for me to say anything about this course, since I'm already familiar with JS. In any case, for people who are new to JS, this is good information for beginners.

<details>
    <summary>Result</summary>
    <img src="https://github.com/Marionetko/kottans-frontend/blob/main/task_js_basics/Screenshot_1.jpg">
</details>

2. FreeCodeCamp exercises 

- [Basic JavaScript](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-javascript/)

<details>
    <summary>Result</summary>
    <img src="https://github.com/Marionetko/kottans-frontend/blob/main/task_js_basics/Screenshot_2.jpg">
</details>

> I went through this part quite a long time ago. It was a great pleasure to rerun it all over again.

- [ES6 Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-javascript/) - JS ES6 features. Perform 17 exercises

<details>
    <summary>Result</summary>
    <img src="https://github.com/Marionetko/kottans-frontend/blob/main/task_js_basics/Screenshot_3.jpg">
</details>

>I was already somewhat familiar with ES6 syntax, but this part of the tasks I found something new. I learned about Destructuring Assignment, Rest Parameter, Spread Operator. I learned how and where to apply them and for what purpose. I will keep some cheat sheets for the future.

**Prevent Object Mutation**
```js
let obj = {
  name:"FreeCodeCamp",
  review:"Awesome"
};
Object.freeze(obj);
obj.review = "bad";
obj.newProp = "Test";
console.log(obj);
```
`Object.freeze();` - to prevent data mutation.

**Arrow function syntax**

```js
const myFunc = () => {
  const myVar = "value";
  return myVar;
}
```

When there is no function body, and only a return value, arrow function syntax allows you to omit the keyword return as well as the brackets surrounding the code.

```js
const myFunc = () => "value";
```

It is possible to pass more than one argument into an arrow function.

```js
const multiplier = (item, multi) => item * multi;
multiplier(4, 2);
```

**Set Default Parameters for Functions**

```js
const greeting = (name = "Anonymous") => "Hello " + name;

console.log(greeting("John"));
console.log(greeting());
```

**Use the Rest Parameter**

With the rest parameter, you can create functions that take a variable number of arguments. These arguments are stored in an array that can be accessed later from inside the function.

```js
function howMany(...args) {
  return "You have passed " + args.length + " arguments.";
}
console.log(howMany(0, 1, 2));
console.log(howMany("string", null, [1, 2, 3], { }));
```

**Use the Spread Operator to Evaluate Arrays In-Place**

```js
const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr);
```

Spread and Rest - allow to simply combine several arrays into one or pass values of individual array elements as function arguments. Interestingly, both of these operators look exactly the same in appearance - a ternary `(...)`, but are used in different cases, not only for arrays, but also for objects.

**Destructuring Assignment**

- Extract Values from Objects

```js
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

const {today, tomorrow} = HIGH_TEMPERATURES;
```

- Assign Variables from Objects

```js
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};
  
const { today : highToday, tomorrow : highTomorrow } = HIGH_TEMPERATURES;
```

- Assign Variables from Nested Objects

```js
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

const { today : {low : lowToday, high : highToday}} = LOCAL_FORECAST;
```

- Assign Variables from Arrays

Destructuring an array lets us do exactly that:

```js
const [a, b] = [1, 2, 3, 4, 5, 6];
console.log(a, b);
```
The console will display the values of `a` and `b` as `1`, `2`.

The variable `a` is assigned the first value of the array, and `b` is assigned the second value of the array. We can also access the value at any index in an array with destructuring by using commas to reach the desired index:

```js
const [a, b,,, c] = [1, 2, 3, 4, 5, 6];
console.log(a, b, c);
```
The console will display the values of `a`, `b`, and `c` as `1`, `2`, `5`.

- Reassign Array Elements with the Rest Parameter

```js
const [a, b, ...arr] = [1, 2, 3, 4, 5, 7];
console.log(a, b);
console.log(arr);
```

The console would display the values `1`, `2` and `[3, 4, 5, 7]`.

Variables `a` and `b` take the first and second values from the array. After that, because of the rest parameter's presence, `arr` gets the rest of the values in the form of an array. 

- Pass an Object as a Function's Parameters

In some cases, you can destructure the object in a function argument itself.

```js
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};

const half = ({max, min}) => (max + min) / 2.0; 
```

**Create Strings using Template Literals**

```js
const person = {
  name: "Zodiac Hasbro",
  age: 56
};

const greeting = `Hello, my name is ${person.name}! I am ${person.age} years old.`;

console.log(greeting);
```

- Object Literal Declarations Using Object Property Shorthand

```js
const getMousePosition = (x, y) => ({ x, y });
```

- Concise Declarative Functions

With ES6, we can remove the `function` keyword and colon altogether when defining functions in objects. Here's an example of this syntax:

```js
const person = {
  name: "Taylor",
  sayHello() {
    return `Hello! My name is ${this.name}.`;
  }
};
```

- [Basic Data Structures](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures/)

<details>
    <summary>Result</summary>
    <img src="https://github.com/Marionetko/kottans-frontend/blob/main/task_js_basics/Screenshot_4.jpg">
</details>

> In this Basic Data Structures course, I learned more about the differences between arrays and objects and which ones to use in different situations. I also learned how to use useful JS methods like splice() and Object.keys() to access and manipulate data. I'll also leave a little cheat sheet here.

`.push()` - adds elements to the end of an array.

`.pop()` - removes an element from the end of an array.

`.unshift()` - adds elements to the beginning of an array.

`.shift()` - removes an element from the beginning of an array.

`.splice()` - remove or add any number of consecutive elements from anywhere in an array.

`.slice()` - copies or extracts a given number of elements to a new array, leaving the array it is called upon untouched.

`.indexOf()` - allows us to quickly and easily check for the presence of an element on an array.

-[Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/)

<details>
    <summary>Result</summary>
    <img src="https://github.com/Marionetko/kottans-frontend/blob/main/task_js_basics/Screenshot_5.jpg">
</details>

>Very interesting and simple tasks to understand the structures of algorithms. Of course, some tasks took some time to think about, but in general all the tasks were solved pretty quickly.


