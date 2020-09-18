# Roadmap

## About

This is my personal roadmap for learning web development — specifically the **front-end**. This guide started out as notes I was taking on the [Web Developer Roadmap](https://github.com/kamranahmedse/developer-roadmap) and [Front-end Interview Questions](https://github.com/h5bp/Front-end-Developer-Interview-Questions) while self-learning web development. I'm trying to combine (and expand) them into as comprehensive and inclusive a guide as possible for newbies and anyone interested in learning more about development in-depth. This is definitely a **work-in-progress**, and more will be added to these concepts as time allows.

If you're interested in adding anything, feel free to submit a Pull Request.

## Contents [](#Contents)

1. [Introduction](#Introduction)
   - [Web Development: Front, Back, and Full-Stack](#WebDev)
   - [Web Development Basics](#Basics)
2. [HTML](#HTML)
   - [Semantic Structure & Accessibility](#Semantic)
3. [CSS](#CSS)
4. [JavaScript](#JavaScript)
5. [Git](#Git)
6. [CLI](#CLI)
7. [Frameworks, Libraries, Preprocessors, Compilers](#Frameworks)
8. [CS Fundamentals](#CSFundamentals)

## Introduction [](#Introduction)

### Web Development: Front, Back, and Full-Stack [](#WebDev)

There are a lot of terms that get thrown around in relation to people who write code that involves the Internet — Developer, Engineer, Architect, Specialist, etc. — and like a lot of the tech industry, the roles of these positions varies across organizations. Typically though, you can think of there being three _main_ (not exhaustive) areas:

- **Front-end**: This typically involves UI/UX (User Interfaces/User Experiences) that heavily involves the visual and interactive parts of the web. This might be building (and sometimes designing) websites, creating web apps, and any number of tasks related to the "front" facing parts of the web. **This guide focuses on the Front-end**.

- **Back-end**: ...

- **Full-stack**: ...

### Web Development Basics [](#Basics)

- ...

[Back to Contents](#Contents)

## HTML [](#HTML)

### Semantic Structure & Accessibility [](#Semantic)

- ...

### Study Concepts

#### What does a `doctype` do

All HTML documents must start with a <!DOCTYPE > declaration. The declaration is not an HTML tag. It
is an "information" to the browser about what document type to expect.

#### How do you serve a page with content in multiple languages

Language can be set/prioritized through http request headers, with more prioritized languages given
greater “weight”. This can also be set with the “lang” attributes: 1 Define a primary language with
the lang attribute, and then call out the secondary language(s) with lang attributes on elements in
the document 2 Define lang in the specific sections of the document as needed

#### What kind of things must you be wary of when designing or developing for multilingual sites

- Always use the `lang` and the `dir` attributes in all your HTML
- Avoid talking about "right side" and "left side"
- Don't ever concatenate translated strings. Ex: `"The date today is " + date`
- Rather add parameter support to your messages and do something like:

```javascript
messages.date = "The date today is %date"... and then:msg( 'messages.date' );
```

#### What are `data-` attributes good for

Data that should be associated with a particular element but need not have any defined meaning. Ex:

```html
<!-- HTML - Extra Info about “#electric-cars” -->
<article id="electric-cars" data-columns="3" data-index-number="12314" data-parent="cars"></article>
```

```javascript
// JavaScript Access
const article = document.querySelector("#electric-cars");
// Can get and/or set
article.dataset.columns; // "3"
article.dataset.indexNumber; // "12314"
article.dataset.parent; // "cars"
```

```css
/* CSS Access */
article::before {
  content: attr(data-parent);
}

article[data-columns="3"] {
  width: 400px;
}
article[data-columns="4"] {
  width: 600px;
}
```

#### Consider HTML5 as an open web platform. What are the building blocks of HTML5

- **Semantics**: allowing you to describe more precisely what your content is.
- **Connectivity**: allowing
  you to communicate with the server in new and innovative ways.
- **Offline Storage**: allowing
  webpages to store data on the client-side locally and operate offline more efficiently.
- **Multimedia**: making video and audio first-class citizens in the Open Web.
- **2D/3D Graphics and
  Effects**: allowing a much more diverse range of presentation options.
- **Performance and Integration**:
  providing greater speed optimization and better usage of computer hardware.
- **Device Access**: allowing for the usage of various input and output devices.
- **Styling**: letting authors write more
  sophisticated themes.

#### Describe the difference between a `cookie`, `sessionStorage` and `localStorage`

- `localStorage`, `sessionStorage`, and `cookies` are all client storage solutions.
- **`localStorage`**: ...
- **`sessionStorage`**: ...
- **`cookies`**: ...

#### Describe the difference between `<script>`, `<script async>` and `<script defer>`

- **`<script>`**: ...
- **`<script aync>`**: ...
- **`<script defer>`**: ...

#### Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions

- ...

#### What is progressive rendering

- ...

#### Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute

- ...

#### Have you used different HTML templating languages before

- ...

[Back to Contents](#Contents)

## [CSS](#CSS)

### Flexbox

### Grid

### Hierarchy & Inheritance

[Back to Contents](#Contents)

## [JavaScript](#JavaScript)

### Study Concepts

#### Explain event delegation

#### Explain how `this` works in JavaScript

#### Can you give an example of one of the ways that working with `this` has changed in ES6

#### Explain how prototypal inheritance works

#### What's the difference between a variable that is: `null`, `undefined` or undeclared

#### How would you go about checking for any of these states

#### What is a closure, and how/why would you use one

#### What language constructions do you use for iterating over object properties and array items

#### Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other

#### What's a typical use case for anonymous functions

#### What's the difference between host objects and native objects

#### Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`

#### Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

#### Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two

#### Explain `Function.prototype.bind`

#### What's the difference between feature detection, feature inference, and using the UA string

#### Explain "hoisting"

#### Describe event bubbling

#### Describe event capturing

#### What's the difference between an "attribute" and a "property"

#### What are the pros and cons of extending built-in JavaScript objects

#### What is the difference between `==` and `===`

#### Explain the same-origin policy with regards to JavaScript

#### Why is it called a Ternary operator, what does the word "Ternary" indicate

#### What is strict mode? What are some of the advantages/disadvantages of using it

#### What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript

#### What tools and techniques do you use debugging JavaScript code

#### Explain the difference between mutable and immutable objects

- What is an example of an immutable object in JavaScript?
- What are the pros and cons of immutability?
- How can you achieve immutability in your own code?

#### Explain the difference between synchronous and asynchronous functions

#### What is event loop

#### What is the difference between call stack and task queue

#### What are the differences between variables created using `let`, `var` or `const`

#### What are the differences between ES6 class and ES5 function constructors

#### Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions

#### What advantage is there for using the arrow syntax for a method in a constructor

#### What is the definition of a higher-order function

#### Can you give an example for destructuring an object or an array

#### Can you give an example of generating a string with ES6 Template Literals

#### Can you give an example of a curry function and why this syntax offers an advantage

#### What are the benefits of using `spread syntax` and how is it different from `rest syntax`

#### How can you share code between files

#### Why you might want to create static class members

#### What is the difference between `while` and `do-while` loops in JavaScript

[Back to Contents](#Contents)

## [Git](#Git)

### Study Concepts

[Back to Contents](#Contents)

## [CLI (Command Line Interface)](#CLI)

### Study Concepts

[Back to Contents](#Contents)

## [Frameworks, Libraries, Preprocessors, Compilers](#Frameworks)

### JS Frameworks

#### jQuery

#### React

#### Vue

#### Angular

#### Node

### CSS Libraries

#### Materialize

#### Skeleton

#### Bootstrap

### CSS Preprocessors

#### LESS

#### SASS/SCSS

[Back to Contents](#Contents)

## [CS Fundamentals](#CSFundamentals)

### Algorithms & Data Structures

## [Back to Contents](#Contents)

---

_To Do:_

- Test Build process for gh-pages deployment
- Create main page with checked/unchecked boxes to track progress
- Create documentation
