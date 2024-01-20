# TypeScript Cheat Sheet
## What is TypeScript?
<p>TypeScript is JavaScript with added syntax for types. TypeScript is a statically typed superset of JavaScript developed by Microsoft, designed to improve the development experience of large-scale JavaScript applications. It adds optional static typing, interfaces, classes, decorators, and modules to JavaScript, allowing developers to write more robust and maintainable code. TypeScript compiles to plain JavaScript and is widely used in popular JavaScript frameworks and libraries, providing improved tooling and type checking for JavaScript development.</p>

## > Key features of TypeScript:


* Static Typing: 
TypeScript introduces static typing through a system of types. This allows developers to catch errors related to variable types at compile-time rather than runtime.

* Object-Oriented Programming (OOP): TypeScript supports object-oriented programming concepts such as classes, interfaces, inheritance, and modules, making it easier to organize and structure code.

* Type Inference: TypeScript's compiler can often infer the types of variables and expressions without explicit type annotations. This helps reduce the amount of boilerplate code needed while still providing the benefits of static typing.

* Enhanced Tooling: TypeScript works well with modern development tools and IDEs, providing features like autocompletion, code navigation, and refactoring support. This can lead to a more productive development experience.

* Compatibility with JavaScript: Since TypeScript is a superset of JavaScript, existing JavaScript code can be gradually migrated to TypeScript. Developers can choose to adopt TypeScript features incrementally in their projects.

* Compilation: TypeScript code is transpiled (converted) to JavaScript before execution. This means that TypeScript code can run in any environment that supports JavaScript.

* Community and Ecosystem: TypeScript has gained popularity, and many popular JavaScript libraries and frameworks provide TypeScript definitions. The TypeScript community actively contributes to the development of the language, and its popularity has led to broader support in the development ecosystem.

-------------------------------------------------------------
<br/>
<p>Overall, TypeScript is designed to improve the development experience by adding static typing and other features while maintaining compatibility with JavaScript, making it a powerful tool for building scalable and maintainable web applications.</p>
<br/>

# TypeScript’s commonly used syntax and concepts:

### 1) Variable Declarations: 
* TypeScript is an extension of JavaScript. Therefore, TypeScript inherently supports var, let, and const. However, caution should be exercised when using var in TypeScript. Additionally, when declaring a variable in TypeScript, it is necessary to explicitly specify its type.

### Example:

<pre><code>
let num: number = 42;
let str: string = 'Hello';
let bool: boolean = true;
let arr: number[] = [1, 2, 3];
let tuple: [string, number] = ['foo', 42];
let obj: { name: string, age: number } = { name: 'John', age: 30 };
</code></pre>


### 2) Type Annotations:
* In TypeScript, type annotations are used to explicitly specify the type of a variable, parameter, or return value. Type annotations help TypeScript developers catch and prevent type-related errors during development. They provide additional information to the TypeScript compiler about the expected types in your code.

### Example:
<pre><code>
function greet(name: string): string { // function with type annotations for parameters and return value
  return "Hello, " + name;
}
</code></pre>

### 3) Static Typing:
* TypeScript’s static typing allows you to catch type-related errors at compile time rather than runtime. This can help you write more reliable code and catch errors early on in the development process. TypeScript allows you to specify the types of variables, function parameters, and return values.

### Example:
<pre><code>
let firstName: string = 'John';
let age: number = 30;
function add(a: number, b: number): number {
  return a + b;
}
</code></pre>