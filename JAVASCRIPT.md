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

###