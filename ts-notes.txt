TypeScript Notes:-

1. What is TypeScript?
TypeScript is a superset of JavaScript developed by Microsoft.
It adds optional static typing to JavaScript, making it easier to catch errors before runtime.
TypeScript code is transpiled into JavaScript, which means it can run in any JavaScript environment.

2. Basic Types
TypeScript supports all JavaScript primitive types: number, string, boolean, null, undefined.
Additional types include object, array, tuple, enum, any, and void.

3. Type Annotations
Type annotations allow you to declare the type of a variable.
Syntax: let variableName: type = value;
Example: let age: number = 25;

4. Interfaces
Interfaces define the structure of an object.
They specify which properties and methods an object must have.
Example:
typescript
Copy code
interface Person {
  name: string;
  age: number;
}

5. Functions
Functions can have typed parameters and return types.
Example:
typescript
Copy code
function greet(name: string): void {
  console.log("Hello, " + name);
}

6. Arrays
Arrays can be typed using square brackets.
Example: let numbers: number[] = [1, 2, 3, 4, 5];

7. Union Types
Union types allow a variable to have multiple types.
Example: let result: number | string = 10;

8. Type Inference
TypeScript can infer types based on the assigned value.
Example: let num = 5; // TypeScript infers num as type number

9. Generics
Generics allow the creation of reusable components.
Example:
typescript
Copy code
function identity<T>(arg: T): T {
  return arg;
}

10. Modules
TypeScript supports modules to organize code into reusable units.
Modules can be imported and exported using import and export keywords.
Example:
typescript
Copy code
// math.ts
export function add(x: number, y: number): number {
  return x + y;
}

// app.ts
import { add } from "./math";

11. TypeScript Compiler (tsc)
TypeScript files are transpiled into JavaScript using the TypeScript compiler (tsc).
The tsc command compiles TypeScript files into JavaScript files.

12. tsconfig.json
The tsconfig.json file is used to configure TypeScript compiler options.
It specifies compiler options, project files, and compile targets.

13. Type Guards
Type guards are used to narrow down the type of a variable within a conditional block.
They help in type inference and type safety.
Example:
typescript
Copy code
function isString(val: any): val is string {
  return typeof val === "string";
}

14. Type Assertions
Type assertions allow you to manually override TypeScript's type inference.
They are useful when you know more about a value than TypeScript does.
Example: let strLength: number = (val as string).length;

15. Decorators
Decorators provide a way to add annotations and metadata to classes, methods, or properties.
They are experimental features and are commonly used in frameworks like Angular.
Example:
typescript
Copy code
function log(target: any, key: string) {
  console.log(`Method ${key} is invoked`);
}

class MyClass {
  @log
  myMethod() {
    // Method implementation
  }
}

Conclusion
These notes cover the foundational concepts of TypeScript. By understanding these concepts, you can write more maintainable, readable, and type-safe code in TypeScript.

