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
```
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