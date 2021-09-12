### Javascript Data Types

In terms of Data types, you have the primative data types, 
which consist of the boolean (true, false,) numbers - which could be
any type (floating point, whole,) null, which is an empty value that is 
assigned, undefined, which has no value, and strings. Then there are
non primitives, which include arrays and objects, (yes, arrays are objects 
but they operate and are manipulated differently.) Maps and Sets would be
said to be objects if used ```typeof``` but they are also distinct data
structures, if not data types. 

### Const && let vs var

Variables declared with ```var``` adhere to lexical scope. This means that should a var be declared in a falsy statement (inside an if block for example) then it would render ```undefined```. The reason for this is that in lexical scope, the variable gets hoisted as if it was declared at the top of the function. 

```let``` adheres to block scope, where it is limited to the code block it is declared in (so it doesnt get hoisted.) let can also be reassigned just like var. However, const cannot be reassigned, and it can't be manipulated as far as its primitive types. However, non primitives like arrays can be manipulated.

### Pass by reference vs Pass by value

When we're passing by value, we're taking one variable with a given primitive data type assigned, and assigning the variable by name to another variable. The second variable now has the value of the first variable at the time of assigning. If we were to then increment the second variable and log both variables, the second variable's value would be equal to the first plus the incremented amount

When working with non primitive types like arrays and objects, we are passing the value by reference. If you were to assign a variable name that was declared as an empty array to a new variable, both variables would be empty arrays. Additionally, if you were to push or pop from the second array, the changes would also be reflected in the original array. The way around this is to set the second variable to a new array with the original array destructured inside using the spread operator. This way, an entirely new array is created. 

### map() vs filter() vs reduce()

Map is used to create a new array and potentially modify its value. Filter is used to return the values that pass when compared against a boolean statement.

Reduce allows for more specificity than map and filter in that it can return a single value, but also any values. The reduce method takes in the accumulator argument, which is set to an initial value that must be given in the function, and the value, which is the current value within the array. The accumulator also needs to be returned or else it will be reset to the given value in the function.

### Falsy Values

Falsy values are values that equate to false in a logical statement, such as
that used in an ```if``` statement. These values include false, null, 
undefined, NaN, and 0, and and empty string. The 0 falsy value is particcularly
useful because it makes a comparison statement easily evaluate if a variable has value or not. 

### Global Variables

Typically, JS doesnt have global variables, but the Document Object Model does (such as the window object or the DOM object.) Using globals in programming is one of the worst standards; they're easily manipulated, they can be affected by anything, and it's risky. People try to make variables global because it's easy, but most of the time it's unnecessary. 

### this

The ```this``` keyword allows us to access our current context (for intstance, in the js document itself, the context is the window object). this is typically used in object oriented programming to access properties and methods, and properties within methods. If you wanted to access a property of an object within the object, you'd do so by using ```this.``` because it specificies the scope the property is in. It is worth noting that methods defined with arrow functions don't access the scope the same way (values will likely return undefined).

### == vs ===

== is a quality operator where only the value is checked for equivalency. The === operator (strictly equals) checks the value and the data type, which is essentially what the == (double equals) does for most other programming languages. I prefer the strictly equals operator because stricter settings in the code typically yields better
production with the elimination of bugs. ESLint and TSLint (tools for identifying problematic code,) use === for this reason.

### coersion 

Coersion has two types essentially, implicit and explicit. Say you were to add 
```javascript 2 + 3 + '7'```, the returned value would be 57 as a string, because it would add the number types and then concatinate the number and character string into a string value. Explicit coersion occurs if we were to use the Number or String object to yield the data type differently than how it was defined, or at least passed in to the object as an argument. Example would be ```console.log(typeof String(5));```
which would yield string, because the value is now ```'5'``` despite being passed to the object as ```5```

### typeof

will check the data value of the type you're passing. ```22``` will give number, ```'22'``` will give string. Arrays will give objects. To check if the object is specifically an array you need to use the isArray method in the Array prototype. Another 'trip up' would be if you checked the typeof null it would yield an object but if you used the ```instanceof``` operator it would yield false. 

### delete

The delete keyword allows for the deletion of a property of an object (the value of the property and the property itself). The delete keyword is typically not best practice to use because by needing to use it, it shows that the application is fragile

### object notation

The two notations to access objects are dot and bracket notations. If we had an object ```identity``` that had a property of ```firstName```, we could access the value by storing ```identity.firstName``` in a variable. Additionally, you could access it with bracket notation, but this wouldn't be advised, as bracket notation is best used for passing in a variable, for instance, if you were to loop through and check the values in an object (object.property would return undefined because it would be looking for a property called property.) Lints (ES and TS) both prefer dot notation as it is stricter.

### Strict mode

Helps enforce best standards and practices, but overall has been deprecated by linters. To use strict mode, ```'use strict'``` must be at the top of the javascript document. Strict mode prevents global variables from being assigned, and prevents deleting keys and duplicate names from parameters

### anonymous functions

anonymous functions are functions that are stored in a variable and don't have their own name. They can still be called just like normally defined functions.

### callbacks

Callbacks (aka higher order functions) are functions that are passed and are called back to at a later time. For instance, a callback is passed into the map method that takes in the individual elements of the array being mapped. The purpose of the callback function is to then manipulate each element. Alternatively, you could pass in a function that was written into the map method which can do what the typical callback inside the map method would do, and this also works as a callback.

### closures 

Closures are a way of manipulating a variable without storing it in a global context. Say we have an anonymous function defined with a variable ```count``` defined within it. 
```javascript
const add = (() => {
    let count = 0;
})
```
by returning another function that increments the count and returns the count, all within the initial function, upon calling the inital function, the incremented account will be returned. 
```javascript
const add = (() => {
  let count = 0;
  return function () {
    count++;
    return count;
  }
})();

console.log(add()); // 1
console.log(add()); // 2
```
it should also be noted that if the inital function is defined using an arrow, it should be wrapped inside parenthesis, and that a second set of parenthesis are needed to invoke the function when it is called later.

### naming & standards

Variables should typically be named in camelCase. Booleans should also begin with the "is-" or "has-" prefix. For function calls that return something, it makes sense to being it with a verb (update, get.) It could be worth noting that Hungarian casing (naming prefix is the data type) is very outdated, typescript and js intellisense takes care of these. For CSS, try to add as few selectors as possible, dashes are common practice, as are using block element modifiers, which are classes extended with a -- that can alter the behavior of the element and the child element classes.

For naming a returned number, say a ```function factorialize(num)``` existed that took in a number and returned its factorial. you might want the return variable to be factorialTotal or factorialProduct. For a date, if you were returning a new Date object you might call it todaysDate. On the other hand, if you were to name keys in a class, you'd want them to be very direct (name, age, date).

For numbers, you want to avoid passing in magic numbers (specific values with no context). This might be a good time to use camelcase to assign the number to a constant.

### empty arrays

Theres the easy way to reassign the array to an empty array. But if you had to modify it (such as if the array was assigned to a const). In that case you could use a while loop ```while (arr.length > 0)```, set the array.length to 0, or use ```arr.splice(0, arr.length)```. To empty the array without reassigning the value would be to use the while loop and either pop or shift;

### create arrays

One way you don't want to create an array is to use the Array constructor ```new Array```, you can override properties and methods that are associated with the prototype. 

Better ways include assigning a variable to two brackets, or using a higher order function (map, filter, reduce) to store the manipulated version of one array into a new variable. 

### undefined vs null

Undefined is the value of a variable that has no value, where as null is an empty value assigned to a variable. Typically, an undefined value will be yielded if logic is faulty, where null is specifically assigned to a variable with the purpose it to have that empty value. It should be noted that an undeclared value is one that tries to access a variable that hasn't been declared and doesn't exist.

### 0.2 + 0.1

adding these floating point numbers in javascript won't return 0.3 as expected. Instead, there will be a series of zeros after the 3 and eventually there will be a 4. This is one of the weird behaviors of javascript math which is definitely imperfect. You can use the toFixed method from the Math object and pass 1 to get 0.3 exactly.

### instanceof

The ```instanceof``` operator can be used to check if an object created is an instance of a particular prototype. If you checked if something was an instance of an object it would always return true, though it may also be also be an instance of another class.

### IIFE

### Maintaining state and local storage

Local storage is a means of maintaining state in between browswer sessions by sending data to the browswer for storage. LocalStorage can use getItem, setItem, and the clear methods to manipulate the local storage properties. Should you wish to set JSON data in local storage as an object value, you'd need to use JSON.stringify to set and JSON.parse to retrieve. Worth mentioning other storage methods like session storage, cookies, and cache storage.

### HTML APIs 

### Destructuring arrays and objects

Destructuring allows for code to be easier to read and shortens the code length. One way to destructure an array is to define a constant as an array, with each element named appropriately for the indexed element it corresponds with. These new array elements can be interpolated from strings, used in template literals, etc. 

The same prinicple can be used to have a seperate object destructure the original; you can pull out key names into the new object so you dont have to use dot or bracket notation later. Additionally, you could assign aliases to the destructured keys like ```{ firstName: fn }```

### Rest and Spread Operator

The rest operator doesnt have too many uses. It can turn a series of numbers that are passed into a function as an argument into an array by using three dots before the argument in the function parentheses. Much more commonly used is the spread operator, which can unpack arrays and objects. If you called a function that took in one argument as a variable,  should you be passing in an object where the function is called, you could then assign the variable passed into the objects definition to a new variable, and by using the spread operator before it you will have the original object that was argued in the call. 

### Arrow function

Arrow functions are ES6 functions that allow you to simplify the syntax. They're very easy to use as callbacks, particularly within higher order functions. Issues with arrow functions include binding, or lack there of, using the this keyword within an object.

### NaN

NaN means one of two things: you tried to parse something that wasn't a number, or an operation occured that the programming language couldn't handle ( 0/0). If you were to check the typeof NaN, it would return number so you'd have to use the ```isNaN``` method.

###