# Typescript
## Table of Contents
-   [Typescript](#typescript)
-   [Type Inference](#type-inference)
-   [Any](#any)
-   [Variable Type Annotation](#variable-type-annotations)
-   [Optional Parameters](#optional-parameters)
-   [Complex Types](#complex-types)
-   [Object Types](#object-types)
-   [Type Aliases](#type-aliases)
-   [Function Types](#function-types)
-   [Generic Types](#generic-types)
-   [Generic Functions](#generic-functions)
-   [Unions](#unions)
-   [Type Narrowing](#type-narrowing)
-   [Using `in` with type guards](#using-in-with-type-guards)
-   [Unions with literal types](#unions-with-literal-types)
-   [Using interface keyward to define a type](#using-interface-keyword-to-define-a-type)
-   [Interfaces and Classes](#interfaces-and-classes)
-   [Extending Interfaces](#extending-interfaces)

## Typescript

TypeScript is a programming language that adds types to JavaScript. It allows us to write JavaScript with a set of tools called a type system that can spot potential bugs in, clarify the structure of, and help refactor our code.

-   First, we write TypeScript code in files with the extension .ts.
-   Next, we run our code through the TypeScript transpiler. The transpiler will check that the code adheres to TypeScript’s standards, and it will display errors when it does not.
-   If the TypeScript code can be converted into working JavaScript, the transpiler will output a JavaScript version of the file (.js).
-   TypeScript code is a superset of JavaScript code—it has all the features of traditional JavaScript but adds some new features.

<sub>[back to top](#table-of-contents)</sub>


## Type inference  
Type of the variable cann't changed once it is initialized.
Example: Below code through an error.

```
let order = 'first';

order = 1;
```

<sub>[back to top](#table-of-contents)</sub>


## Any
There are some places where TypeScript will not try to infer what type something is—generally when a variable is declared without being assigned an initial value. In situations where it isn’t able to infer a type, TypeScript will consider a variable to be of type any.

Variables of type any can be assigned to any value and TypeScript won’t give an error if they’re reassigned to a different type later on.
```
let onOrOff;

onOrOff = 1;
onOrOff = false;
```

<sub>[back to top](#table-of-contents)</sub>

## Variable Type Annotations
Variables can have type annotations (also known as type declarations) added just after their names. We provide a type annotation by appending a variable with a colon (:) and the type (e.g., number, string, or any).
```
let mustBeAString : string;
mustBeAString = 'Catdog';

mustBeAString = 1337;
// Error: Type 'number' is not assignable to type 'string'
```

<sub>[back to top](#table-of-contents)</sub>

## Optional Parameters
```
function greet(name?: string) {
  console.log(`Hello, ${name|| 'Anonymous'}!`);
}

greet(); // Prints: Hello, Anonymous!
```

<sub>[back to top](#table-of-contents)</sub>

## Complex Types

### Creating Enum and Using it for type safety.

```
enum Pet {
  Hamster,
  Rat,
  Chinchilla,
  Tarantula
}

let petOnSale : Pet = Pet.Chinchilla

let ordersArray: [Pet, number][] = [
  [Pet.Rat, 2], 
  [Pet.Chinchilla, 1], 
  [Pet.Hamster, 2], 
  [Pet.Chinchilla, 50]
];
```

<sub>[back to top](#table-of-contents)</sub>

## Object Types

```
let aPerson: {name: string, age: number};

// Type error: age property has the wrong type.
aPerson = {name: 'Aisle Nevertell', age: "wouldn't you like to know"}; 

// Type error: no age property.
aPerson = {name: 'Kushim', yearsOld: 5000};  

// Valid code. 
aPerson = {name: 'User McCodecad', age: 22}; 
```

<sub>[back to top](#table-of-contents)</sub>


## Type Aliases
Instead of writing long complex type of objects every time, use alias for it.

Example:
```
// Add your type alias below:
type Coord = [number, number, string, number, number, string]


let codecademyCoordinates: Coord = [40, 43.2, 'N', 73, 59.8, 'W'];
let bermudaTCoordinates: Coord = [25, 0 , 'N' , 71, 0, 'W'];
```

<sub>[back to top](#table-of-contents)</sub>


## Function Types

```
type StringsToNumberFunction = (arg0: string, arg1: string) => number;

let myFunc: StringsToNumberFunction;
myFunc = function(firstName: string, lastName: string) {
  return firstName.length + lastName.length;
};
```
There’s something important to remember here. We must never be tempted to omit the parameter names or the parentheses around the parameters in a function type annotation, even if there is only one parameter. This code will not run!


<sub>[back to top](#table-of-contents)</sub>

## Generic Types
TypeScript’s generics are ways to create collections of types (and typed functions, and more) that share certain formal similarities. These collections are parameterized by one or more type variables.

Example: 
Defining Generic Type
```
type Family<T> = {
  parents: [T, T], mate: T, children: T[]
};
```

Using Generic Type.
```
let aStringFamily: Family<string> = {
  parents: ['stern string', 'nice string'],
  mate: 'string next door', 
  children: ['stringy', 'stringo', 'stringina', 'stringolio']
}; 
```

<sub>[back to top](#table-of-contents)</sub>

## Generic Functions

```
//Generic Function Declaration
function getFilledArray<T>(value: T, n: number): T[] {
  return Array(n).fill(value);
}

//Type alias
type Person =  {name: string, age: number};
type Coord = [number, number];

//Variable declaration
let stringArray: string[];
let numberArray: number[];
let personArray: Person[];
let coordinateArray: Coord[];

// Generic Function Calling:
stringArray = getFilledArray<string>('hi', 6);
numberArray = getFilledArray<number>(9, 6);
personArray = getFilledArray<Person>({name:'J. Dean',age: 24}, 6);
coordinateArray = getFilledArray<Coord>([3,4], 6);
```

<sub>[back to top](#table-of-contents)</sub>

## Unions

`string or number = string | number`

<sub>[back to top](#table-of-contents)</sub>


## Type Narrowing
Type narrowing is when TypeScript can figure out what type a variable can be at a given point in our code.
Example:
```
function formatValue(value: string | number) {
  if(typeof value==='string'){
    console.log(value.toLowerCase());
  }else if(typeof value==='number'){
    console.log(value.toFixed(2))
  }
}

formatValue('Hiya');
formatValue(42);
```

<sub>[back to top](#table-of-contents)</sub>

## Using `in` with Type Guards
The in operator checks if a property exists on an object itself or anywhere within its prototype chain.

```
type Tennis = {
  serve: () => void;
}

type Soccer = {
  kick: () => void;
}

function play(sport: Tennis | Soccer) {
  if ('serve' in sport) {
    return sport.serve();
  }

  if ('kick' in sport) {
    return sport.kick();
  }
}
```

<sub>[back to top](#table-of-contents)</sub>

## Unions with Literal Types
```
type Status = 'idle' | 'downloading' | 'complete'

function downloadStatus(status: Status)
{
  if(status==='idle')
      console.log('Download');
  if(status==='downloading')
      console.log('Downloading...');
  if(status==='complete')
    console.log('Your download is complete!');
}
downloadStatus('idle')
//Throw error because argument is not and type `Status`
downloadStatus('Stop')
```

<sub>[back to top](#table-of-contents)</sub>

## Using `interface` keyword to define a type.
```
// Write an interface here
interface Run{
  miles: number;
}

function updateRunGoal(run: Run) {
  console.log(`
Miles left:       ${50 - run.miles}
Percent of goal:  ${(run.miles / 50) * 100}% complete
  `)
}

updateRunGoal({
  miles: 5,
})
```


<sub>[back to top](#table-of-contents)</sub>

## Interfaces and Classes

TypeScript gives us the ability to apply a type to an object/class with the implements keyword, like this:
```
interface Robot {
  identify: (id: number) => void;
}

class OneSeries implements Robot {
  identify(id: number) {
    console.log(`beep! I'm ${id.toFixed(2)}.`);
  }

  answerQuestion() {
    console.log('42!');
  }
}

```


<sub>[back to top](#table-of-contents)</sub>

## Extending Interfaces
```
interface Shape {
  color: string;
}

interface Square extends Shape {
  sideLength: number;
}

const mySquare: Square = { sideLength: 10, color: 'blue' };
```

<sub>[back to top](#table-of-contents)</sub>


## Readonly Properties
```
type User = {
    name : string,
    readonly email: string,
}
let user = {
    name: "kaushal",
    email: "abc@gmail.com"
}

//It will raise an error because email is readonly property.
user.email = 'xyz@gmail.com'
```

## Intersection Type
A way to combine multiple types.

```
type Person = {
    name: string,
    age: number
}

type Employee = {
    id: number,
    title: string
}

type PersonAndEmployee = Person & Employee

const alice: PersonAndEmployee = {
    name: 'alice',
    age: 27,
    id: 123,
    title: "Manager"
}
```
