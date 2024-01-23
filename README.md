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

<br />

### 11) Empty interface:

* An empty interface is not commonly used in TypeScript. Any non-null value can be assigned to an empty {}. Creating an empty interface is often an indication of a programmer error, leading to mistakes in filling it correctly.

### Example:

<pre><code>
const someValue: any = "hello";
const strLength: number = (someValue as string).length;
</code></pre>

<br />
<br />

# Function Components:

* This is simple function like jsx. But that function take a props argument and return a JSX element.
### Example:

<pre><code>
// Declaring type of props "Function Component Props"

type AppProps = {
  message: string;
};  // use interface

// Easiest way to declare a Function Component; return type is inferred.

const App = ({ message }: AppProps) => <span><</> div>{message}<span><</> /div>;

// you can choose annotate the return type so an error is raised if you accidentally return some other type

const App = ({ message }: AppProps): React.JSX.Element => <span><</> div>{message}<span><</> /div>;

// you can also inline the type declaration; eliminates naming the prop types, but looks repetitive

const App = ({ message }: { message: string }) => <span><</span>div>{message}<span><</span>/div>;

</code></pre>

<br />

# Class Components:

* Within TypeScript, class Component is a generic type (That's means React.Component<PropType, StateType>), so you want to provide it with (optional) prop and state type parameters.
### Example:

<pre><code>
// Declaring type of props "Class Component Props"

type MyProps = {

  message: string;
};  // use interface

type MyState = {
  count: number; // like this
};
class App extends React.Component<MyProps, MyState> {
  state: MyState = {
    count: 0, // optional second annotation for better type inference
  };
  render() {
    return (
      <span></span>div>
        {this.props.message} {this.state.count}
      <span></span>/div>
    );
  }
}

</code></pre>

<br />

 ### 1) Class Methods:
 * Do it like normal, but remember that any arguments for your functions need to be declared with these arguments typed.

### Example:

<pre><code>
class App extends React.Component<{ message: string }, { count: number }> {
  state = { count: 0 };
  render() {
    return (
      <span><</span>div onClick={() => this.increment(1)}>
        {this.props.message} {this.state.count}
      <span><</span>/div>
    );
  }
  increment = (amt: number) => {
    // like this
    this.setState((state) => ({
      count: state.count + amt,
    }));
  };
}
</code></pre>

<br />


### Class Properties: 
* If you need to declare class properties for later use, just declare it like state, but without assignment:

### Example:

<pre><code>
class App extends React.Component<{
  message: string;
}> {
  pointer: number; // like this
  componentDidMount() {
    this.pointer = 3;
  }
  render() {
    return (
      <span><</span>div>
        {this.props.message} and {this.pointer}
      <span><</span>/div>
    );
  }
}
</code></pre>

<br />

# Error Boundaries:
* <code>NPM</code> provide an <code>error-boundary-react</code> package with <code>TypeScript</code>, that captures and logs errors wherever they occur in the child component tree. Additionally, a fallback UI can be displayed through this error.

<br/>



* <strong> If we want, we can create a custom error boundary component.</strong>

### Example:

<pre><code>
import React, { Component, ErrorInfo, ReactNode } from "react";

interface Props {
  children?: ReactNode;
}

interface State {
  hasError: boolean;
}

class ErrorBoundary extends Component<Props, State> {
  public state: State = {
    hasError: false
  };

  public static getDerivedStateFromError(_: Error): State {
    
    return { hasError: true };   // Update state so the next render will show the fallback UI.
  }

  public componentDidCatch(error: Error, errorInfo: ErrorInfo) {
    console.error("Uncaught error:", error, errorInfo);
  }

  public render() {
    if (this.state.hasError) {
      return <span><</span>h1>Sorry.. there was an error<span><</span>/h1>;
    }

    return this.props.children;
  }
}

export default ErrorBoundary;

</code></pre>

<br />

# Troubleshooting

### Operators

* <code>typeof</code> and <code>instanceof</code>: Used for refinement of type query. [More here.](https://www.typescriptlang.org/docs/handbook/2/typeof-types.html)

* <code>keyof</code>: To get the <code>keys of</code> an object, <code>keyof T</code> is an operator that informs you which values of <code>k</code> can be used for <code>obj[k]</code>.  [More here.](https://www.typescriptlang.org/docs/handbook/2/keyof-types.html)

* <code>[K in O]</code>: It is used to check for mapped types.

* <code>+</code> or <code>-</code> or <code>?</code> : Addition and subtraction and readonly and optional modifiers.  [More here.](https://www.geeksforgeeks.org/typescript-operators/)

* <code>readonly</code> : The properties of the constructed type are not reassignable, meaning those properties cannot be reassigned. [More here.](https://medium.com/totally-typescript/how-to-use-readonly-in-typescript-a902574d9e18)

* <code>x ? Y : Z</code> : It is used to conditional types for generic types, type aliases, function parameter types. [More here.](https://www.geeksforgeeks.org/typescript-operators/)
* <code>!</code> : Non-null assertion for nullable types. [More here.](https://www.geeksforgeeks.org/typescript-operators/)

* <code>=</code> : Generic type parameter default for generic types. [More here.](https://www.geeksforgeeks.org/typescript-operators/)

* <code>as</code> : type assertion. [More here.](https://www.typescriptlang.org/docs/handbook/advanced-types.html)

* <code>is</code> : type guard for function return types. [More here.](https://www.spguides.com/is-keyword-in-typescript/)