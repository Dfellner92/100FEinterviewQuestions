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


