# TypeScript Cheat Sheet

## What is TypeScript?

<p>TypeScript is JavaScript with added syntax for types. TypeScript is a statically typed superset of JavaScript developed by Microsoft, designed to improve the development experience of large-scale JavaScript applications. It adds optional static typing, interfaces, classes, decorators, and modules to JavaScript, allowing developers to write more robust and maintainable code. TypeScript compiles to plain JavaScript and is widely used in popular JavaScript frameworks and libraries, providing improved tooling and type checking for JavaScript development.</p>

## => Key features of TypeScript:

- Static Typing:
  TypeScript introduces static typing through a system of types. This allows developers to catch errors related to variable types at compile-time rather than runtime.

- Object-Oriented Programming (OOP): TypeScript supports object-oriented programming concepts such as classes, interfaces, inheritance, and modules, making it easier to organize and structure code.

- Type Inference: TypeScript's compiler can often infer the types of variables and expressions without explicit type annotations. This helps reduce the amount of boilerplate code needed while still providing the benefits of static typing.

- Enhanced Tooling: TypeScript works well with modern development tools and IDEs, providing features like autocompletion, code navigation, and refactoring support. This can lead to a more productive development experience.

- Compatibility with JavaScript: Since TypeScript is a superset of JavaScript, existing JavaScript code can be gradually migrated to TypeScript. Developers can choose to adopt TypeScript features incrementally in their projects.

- Compilation: TypeScript code is transpiled (converted) to JavaScript before execution. This means that TypeScript code can run in any environment that supports JavaScript.

- Community and Ecosystem: TypeScript has gained popularity, and many popular JavaScript libraries and frameworks provide TypeScript definitions. The TypeScript community actively contributes to the development of the language, and its popularity has led to broader support in the development ecosystem.

---

<br/>
<p>Overall, TypeScript is designed to improve the development experience by adding static typing and other features while maintaining compatibility with JavaScript, making it a powerful tool for building scalable and maintainable web applications.</p>
<br/>

# TypeScript’s commonly used syntax and concepts:

### 1) Variable Declarations:

- TypeScript is an extension of JavaScript. Therefore, TypeScript inherently supports var, let, and const. However, caution should be exercised when using var in TypeScript. Additionally, when declaring a variable in TypeScript, it is necessary to explicitly specify its type.

### Example:

<pre><code>
let num: number = 42;
let str: string = 'Hello';
let bool: boolean = true;
let arr: number[] = [1, 2, 3];
let tuple: [string, number] = ['foo', 42];
let obj: { name: string, age: number } = { name: 'John', age: 30 };
</code></pre>
<br/>

### 2) Type Annotations:

- In TypeScript, type annotations are used to explicitly specify the type of a variable, parameter, or return value. Type annotations help TypeScript developers catch and prevent type-related errors during development. They provide additional information to the TypeScript compiler about the expected types in your code.

### Example:

<pre><code>
function greet(name: string): string { // function with type annotations for parameters and return value
  return "Hello, " + name;
}
</code></pre>

<br/>

### 3) Static Typing:

- TypeScript’s static typing allows you to catch type-related errors at compile time rather than runtime. This can help you write more reliable code and catch errors early on in the development process. TypeScript allows you to specify the types of variables, function parameters, and return values.

### Example:

<pre><code>
let firstName: string = 'John';
let age: number = 30;
function add(a: number, b: number): number {
  return a + b;
}
</code></pre>

<br/>

### 4) Interfaces:

- Interfaces define the structure of an object, but they don’t provide an implementation. They’re a way to describe the expected shape of an object, which can help ensure that your code works as expected. Interfaces define the shape of an object and can be used to ensure that an object adheres to a certain structure.

### Example:

<pre><code>
interface Person {
  firstName: string;
  lastName: string;
  age: number;
}

let person: Person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 30,
};
</code></pre>

<br/>

### 5) Classes:

* Classes in TypeScript are similar to classes in other object-oriented programming languages like Java and C#. They allow you to define properties and methods for a particular type of object, and they support inheritance and encapsulation. TypeScript supports object-oriented programming features like classes and inheritance.

### Example:
<pre><code>
class Animal {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  speak(): void {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name: string) {
    super(name);
  }

  speak(): void {
    console.log(`${this.name} barks.`);
  }
}

let dog = new Dog('Rex');
dog.speak();
</code></pre>

<br/>

### 6) Enums: 
* Enums are a way to define a set of named constants. They make your code more readable by giving names to values that would otherwise be hard to understand.

### Example:
<pre><code>
enum Color {
  Red,
  Green,
  Blue,
}

let c: Color = Color.Green;
console.log(c); 
// Output: 1
</code></pre>

<br/>

### 7) Generics: 
* Generics allow you to write reusable code that works with a variety of types. They allow you to create functions, classes, and interfaces that can work with any type, rather than being tied to a specific type.

### Example:
<pre><code>
function identity<T>(arg: T): T { // generic function
  return arg;
}
const num: number = identity(5); // T is inferred as number
const str: string = identity("hello"); // T is inferred as string
</code></pre>

<br/>

### 8) Union and Intersection Types: 
* Union types allow you to specify that a variable can have one of several possible types. This can be useful when you’re working with data that could be of more than one type.

### Example:

<pre><code>
type NumberOrString = number | string; // union type

function printNumberOrString(value: NumberOrString): void {
  console.log(value);
}
type PersonWithAddress = Person & { address: string }; // intersection type
const personWithAddress: PersonWithAddress = {
  name: "Bob",
  age: 25,
  address: "123 Main St"
};
</code></pre>

<br/>

### 9) Optional Chaining:
* Optional chaining allows you to access nested properties safely, similar to JavaScript. It permits you to handle null or undefined values, preventing errors. It is useful when working with data that may be incomplete, helping to guard against runtime errors.

### Example:

<pre><code>
interface Person {
  firstName: string;
  lastName?: string;
}

let person: Person = {
  firstName: 'John',
};

console.log(person.lastName?.toUpperCase()); // Output: undefined
</code></pre>

<br />

### 10) Type Assertion:

* In TypeScript, there is a special type known as 'any.' You can use it when you want to handle type-checking errors for a particular value. It is advisable to use it when you are unsure about the type of your data, as it can help you avoid errors.

### Example:

<pre><code>
const someValue: any = "hello";
const strLength: number = (someValue as string).length;
</code></pre>