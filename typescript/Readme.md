# Typescript
TypeScript is a programming language that adds types to JavaScript. It allows us to write JavaScript with a set of tools called a type system that can spot potential bugs in, clarify the structure of, and help refactor our code.

-   First, we write TypeScript code in files with the extension .ts.
-   Next, we run our code through the TypeScript transpiler. The transpiler will check that the code adheres to TypeScript’s standards, and it will display errors when it does not.
-   If the TypeScript code can be converted into working JavaScript, the transpiler will output a JavaScript version of the file (.js).
-   TypeScript code is a superset of JavaScript code—it has all the features of traditional JavaScript but adds some new features.


## Type inference  
Type of the variable cann't changed once it is initialized.
Example: Below code through an error.

```
let order = 'first';

order = 1;
```

## Any
There are some places where TypeScript will not try to infer what type something is—generally when a variable is declared without being assigned an initial value. In situations where it isn’t able to infer a type, TypeScript will consider a variable to be of type any.

Variables of type any can be assigned to any value and TypeScript won’t give an error if they’re reassigned to a different type later on.
```
let onOrOff;

onOrOff = 1;
onOrOff = false;
```

## Variable Type Annotations
Variables can have type annotations (also known as type declarations) added just after their names. We provide a type annotation by appending a variable with a colon (:) and the type (e.g., number, string, or any).
```
let mustBeAString : string;
mustBeAString = 'Catdog';

mustBeAString = 1337;
// Error: Type 'number' is not assignable to type 'string'
```

Optional Parameters
```
function greet(name?: string) {
  console.log(`Hello, ${name|| 'Anonymous'}!`);
}

greet(); // Prints: Hello, Anonymous!
```

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

## Type Aliases
Instead of writing long complex type of objects every time, use alias for it.

Example:
```
// Add your type alias below:
type Coord = [number, number, string, number, number, string]


let codecademyCoordinates: Coord = [40, 43.2, 'N', 73, 59.8, 'W'];
let bermudaTCoordinates: Coord = [25, 0 , 'N' , 71, 0, 'W'];
```


## Function Types

```
type StringsToNumberFunction = (arg0: string, arg1: string) => number;

let myFunc: StringsToNumberFunction;
myFunc = function(firstName: string, lastName: string) {
  return firstName.length + lastName.length;
};
```
There’s something important to remember here. We must never be tempted to omit the parameter names or the parentheses around the parameters in a function type annotation, even if there is only one parameter. This code will not run!


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

## Unions

`string or number = string | number`

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