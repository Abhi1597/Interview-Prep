# Javascript Basics - 1

1) Primitive Data Types: [Primitive- MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
    - JavaScript is a loosely typed or a dynamic language.
    - The latest ECMAScript standard defines eight data types:
    - Seven data types that are primitives:
        1) [Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean)
            - A Boolean is a logical data type that can have only the values true or false.
        2) [Null](https://developer.mozilla.org/en-US/docs/Glossary/Null)
            - In computer science, a null value represents a reference that points, generally intentionally, to a nonexistent or invalid object or address. 
        3) [Undefined](https://developer.mozilla.org/en-US/docs/Glossary/Undefined)
            - undefined is a primitive value automatically assigned to variables that have just been declared, or to formal arguments for which there are no actual arguments.
        4) [Number](https://developer.mozilla.org/en-US/docs/Glossary/Number)
            - In JavaScript, Number is a numeric data type in the double-precision 64-bit floating point format (IEEE 754). 
        5) [BigInt](https://developer.mozilla.org/en-US/docs/Glossary/BigInt)
            - In JavaScript, BigInt is a numeric data type that can represent integers in the arbitrary precision format.
        6) [String](https://developer.mozilla.org/en-US/docs/Glossary/String)
            - In any computer programming language, a string is a sequence of characters used to represent text.
            - JavaScript's String type is used to represent textual data. It is a set of "elements" of 16-bit unsigned integer values. 
            - JavaScript strings are immutable. This means that once a string is created, it is not possible to modify it.
            - However, it is still possible to create another string based on an operation on the original string. For example: String.substr(), String.concat().
        7) [Symbol](https://developer.mozilla.org/en-US/docs/Glossary/Symbol)
            - A value having the data type Symbol can be referred to as a "Symbol value".  In a JavaScript runtime environment, a symbol value is created by invoking the function Symbol, which dynamically produces an anonymous, unique value. A symbol may be used as an object property.
        8) [Object](https://developer.mozilla.org/en-US/docs/Glossary/Object)
            - In computer science, an object is a value in memory which is possibly referenced by an identifier.
            In JavaScript, objects can be seen as a collection of properties.
            Properties are identified using key values. 
            A JavaScript object is a mapping between keys and values. Keys are strings, and values can be anything. 

### Extra
* **[Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)**
    - var declarations, wherever they occur, are processed before any code is executed. This is called **hoisting**.
    - The scope of a variable declared with var is its current execution context, which is either the enclosing function or, for variables declared outside any function, global. If you re-declare a JavaScript variable, it will not lose its value.
    - The differences between declared and undeclared variables are:
        1) **Declared variables are constrained in the execution context in which they are declared.** Undeclared variables are always global.
        2) **Declared variables are created before any code is executed.** Undeclared variables do not exist until the code assigning to them is executed.
        3) **Declared variables are a non-configurable property of their execution context (function or global).** Undeclared variables are configurable (e.g. can be deleted).

* **[Hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)**
    - Because variable declarations (and declarations in general) are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. This also means that a variable can appear to be used before it's declared. This behavior is called "hoisting", as it appears that the variable declaration is moved to the top of the function or global code.

* **[NaN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN)**
    - The initial value of NaN is Not-A-Number.
    - It is the returned value when Math functions fail (Math.sqrt(-1)) or when a function trying to parse a number fails (parseInt("blabla")).
    - NaN compares unequal (via ==, !=, ===, and !==) to any other value -- including to another NaN value.
        1) **[isNan()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/isNaN)**
            - The isNaN() function determines whether a value is NaN or not. 
        2) **[Number.isNan()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN)**
            - The Number.isNaN() method determines whether the passed value is NaN and its type is Number.
    - However, do note the difference between isNaN() and Number.isNaN(): the former will return true if the value is currently NaN, or if it is going to be NaN after it is coerced to a number, while the latter will return true only if the value is currently NaN:

* **[JSON](https://developer.mozilla.org/en-US/docs/Glossary/JSON)** 
    - (JavaScript Object Notation) is a lightweight data-interchange format, derived from JavaScript, but used by many programming languages. JSON builds universal data structures.



