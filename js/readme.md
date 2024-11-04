
## Commonly Used Method:
`Math.random()` - Generating float number between 0 (inclusive) and 1(exclusive);  
`Math.floor(Math.random()*max)` - Generating Integer between 0 and max-1  
`name = name.toLowerCase()`  
`name = name.toUpperCase()` 


## Data Types
In JavaScript, there are eight fundamental data types:

-   `Number`: Any number, including numbers with decimals: 4, 8, 1516, 23.42.
-   BigInt: Any number, greater than 253-1 or less than -(253-1), with n appended to the number: 1234567890123456n.
-   `String`: Any grouping of characters on your keyboard (letters, numbers, spaces, symbols, etc.) surrounded by single quotes: ' ... ' or double quotes " ... ", though we prefer single quotes. Some people like to think of string as a fancy word for text.
-   `Boolean`: This data type only has two possible values— either true or false (without quotes). It’s helpful to think of booleans as on and off switches or as the answers to a “yes” or “no” question.
-   `Null`: This data type represents the intentional absence of a value, and is represented by the keyword null (without quotes).
-   `Undefined`: This data type is denoted by the keyword undefined (without quotes). It also represents the absence of a value though it has a different use than null. undefined means that a given value does not exist.
-   `Symbol`: A newer feature to the language, symbols are unique identifiers, useful in more complex coding.
-   `Object`: Collections of related data.

### The list of falsy values includes:

-   `0`  
-   Empty strings like `""` or `''`  
-   `null` which represent when there is no value at all  
-   `undefined` which represent when a declared variable lacks a value  
-   `NaN`, or Not a Number  
 
## [Hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)  
Hoisting feature in JavaScript which allows access to function declarations before they’re defined.
```
greetWorld(); // Output: Hello, World!

function greetWorld() {
  console.log('Hello, World!');
}
```
Notice how hoisting allowed greetWorld() to be called before the greetWorld() function was defined! Since hoisting isn’t considered good practice.

## Function Expression

Another way to define a function is to use a function expression. To define a function inside an expression, we can use the function keyword. In a function expression, the function name is usually omitted. A function with no name is called an anonymous function. A function expression is often stored in a variable in order to refer to it.

```
const caluculateArea = function(width, height){
    const area = width * height;
    return area;
}
```

Unlike function declarations, function expressions are not hoisted so they cannot be called before they are defined.

## Arrow Functions
ES6 introduced arrow function syntax, a shorter way to write functions by using the special “fat arrow” () => notation.

Arrow functions
remove the need to type out the keyword function every time you need to create a function. Instead, you first include the parameters inside the ( ) and then add an arrow => that points to the function body surrounded in { } like this:

```
const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
};
```


## Scope
- `Scope` refers to where variables can be accessed throughout the program, and is determined by where and how they are declared.
- `Blocks` are statements that exist within curly braces {}.
- `Global scope `refers to the context within which variables are accessible to every part of the program.
- `Global variables` are variables that exist within global scope.
- `Block scope` refers to the context within which variables are accessible only within the block they are defined.
- `Local variables` are variables that exist within block scope.
- `Global namespace` is the space in our code that contains globally scoped information.
- `Scope pollution` is when too many variables exist in a namespace or variable names are reused.


## Array methods

`push(ele)` - from end  
`pop()` - from end  
`shift()` - from start  
`unshift(ele)` - from start   
`slice(start_index, end_index)` - creating sublist   
`indexOf` : index of particular element ex: groceryList.indexOf('pasta');  
`splice`: To replace subarray with another array.

Array is pass-by-reference in JS.

## Function

In JavaScript, functions are first class objects. This means that, like other 
objects you’ve encountered, JavaScript functions can have properties and methods.

Since functions are a type of object, they have properties such as .length and .name, and methods such as .toString()


## Higher Order Function 
A higher-order function is a function that either accepts functions as parameters, returns a function, or both! We call functions that get passed in as parameters callback functions. Callback functions get invoked during the execution of the higher-order function.

```
const higherOrderFunc = param => {
  param();
  return `I just invoked ${param.name} as a callback function!`
}
 
const anotherFunc = () => {
  return 'I\'m being invoked by the higher-order function!';
}

higherOrderFunc(anotherFunc);
```

`.forEach` - loop through the array.  
`.map` - create new array with a new element as per given condition in callback function  
`.filter` - filter the array as per given condition in callback function.   
`.findIndex` - return index of first match.  
`.reduce` -  reduce an array to single value as per given condition in callback function.  
`.some` -  Check whether at least one element in the array passes the test.  
`.every` -  Check whether all element in the array passes the test.


## Arrow Functions and this
```
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet: () => {
    console.log(this.dietType);
  }
};

goat.diet(); // Prints undefined
```

Arrow functions inherently bind, or tie, an already defined this value to the function itself that is NOT the calling object. In the code snippet above, the value of this is the global object, or an object that exists in the global scope, which doesn’t have a dietType property and therefore returns undefined.

`The key takeaway from the example above is to avoid using arrow functions when using this in a method!`


## Getters
Getters are methods that get and return the internal properties of an object.

```
const person = {
  _firstName: 'John',
  _lastName: 'Doe',
  get fullName() {
    if (this._firstName && this._lastName){
      return `${this._firstName} ${this._lastName}`;
    } else {
      return 'Missing a first name or a last name.';
    }
  }
}

// To call the getter method: 
person.fullName; // 'John Doe'
```

## Setter

Along with getter methods, we can also create setter methods which reassign values of existing properties within an object.

```
const person = {
  _age: 37,
  set age(newAge){
    if (typeof newAge === 'number'){
      this._age = newAge;
    } else {
      console.log('You must assign a number to age');
    }
  }
};
```

## Property Value Shorthand

Destructuring technique, called property value shorthand, to save ourselves some keystrokes.
```
const monsterFactory = (name, age) => {
  return { 
    name,
    age 
  }
};
```

## Destructured Assignment
In destructured assignment we create a variable with the name of an object’s key that is wrapped in curly braces { } and assign to it the object.
```
const vampire = {
  name: 'Dracula',
  residence: 'Transylvania',
  preferences: {
    day: 'stay inside',
    night: 'satisfy appetite'
  }
};

const { residence } = vampire; 
console.log(residence); // Prints 'Transylvania'

```

## Clases

- Classes are templates for objects.  
- JavaScript calls a constructor method when we create a new instance of a class.  
- Inheritance is when we create a parent class with properties and methods that we can extend to child classes.  
- We use the extends keyword to create a subclass.
- The super keyword calls the constructor() of a parent class.
- Static methods are called on the class, but not on instances of the class.

`Parent Class`
```
class HospitalEmployee {
  //Constructor
  constructor(name) {
    this._name = name; //private properties using prefix '_'
    this._remainingVacationDays = 20;
  }

  //Static Method
  static generatePassword(){
    return Math.floor(Math.random()*10000)    
  }
  
  //Getter Method
  get name() {
    return this._name;
  }
  
  //Getter Method
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  
  //Class Method
  takeVacationDays(daysOff) {
    this._remainingVacationDays -= daysOff;
  }
}
```

`Child Class`
```
//using extend keyword for inheriting parent class.
class Nurse extends HospitalEmployee {
  
  constructor(name, certifications) {
    //invoking super method for calling parent class constructor
    super(name);
    this._certifications = certifications;
  } 
  
  get certifications() {
    return this._certifications;
  }
  
  addCertification(newCertification) {
    this.certifications.push(newCertification);
  }
}
```

`Driver Code`
```
//Creating object of Nurse class.
const nurseOlynyk = new Nurse('Olynyk', ['Trauma','Pediatrics']);

//invoking method present inside parent class i.e HospitalEmployee.
nurseOlynyk.takeVacationDays(5);

//invoking getter function.
console.log(nurseOlynyk.remainingVacationDays);

//invoking function present in child class i.e Nurse.
nurseOlynyk.addCertification('Genetics');
console.log(nurseOlynyk.certifications);
```